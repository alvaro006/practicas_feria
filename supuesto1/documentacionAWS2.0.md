alvaro murillo  
alvaromurillopuchalt06@gmail.com  
May 29, 2025


# Preparando tu Servidor Web en AWS: ¡Apache al Rescate!

Para que tus imágenes cobren vida en la web, primero necesitamos un servidor web que las sirva. Aquí te explicamos cómo instalar y configurar Apache en tu instancia EC2 de AWS:
## 1. Instalación de Apache

Empezamos actualizando la lista de paquetes para asegurarnos de que tenemos las últimas versiones disponibles, y luego instalamos Apache2, el popular servidor web.

    - sudo apt update -y: Este comando actualiza la lista de paquetes disponibles en tu sistema. El -y al final significa que aceptas automáticamente cualquier pregunta que se te haga durante el proceso.
    - sudo apt install -y apache2: Con este comando, instalamos el servidor web Apache2. Una vez más, el -y lo hace todo automático.

Después de la instalación, es crucial que Apache esté funcionando y se inicie cada vez que tu servidor se reinicie:

    - sudo systemctl start apache2: Este comando inicia el servicio de Apache. ¡Es como encenderlo!
    - sudo systemctl enable apache2: Este comando habilita el servicio de Apache para que se inicie automáticamente cada vez que tu instancia EC2 se encienda. Esto asegura que tu servidor web siempre esté disponible.

## 2. Comprobación de Seguridad en AWS

En tu Consola de Administración de AWS, ve a tu instancia EC2. Es fundamental que el grupo de seguridad asociado a esa instancia tenga una regla que permita el tráfico HTTP (puerto 80). Si no está abierta, el navegador no podrá conectarse a tu servidor.

    Servicio HTTP y Puerto 80: Asegúrate de que tu instancia EC2 tenga esta regla de entrada configurada en su grupo de seguridad para permitir conexiones a tu servidor web.

## 3. Creación de la Ruta y Permisos

Dentro de tu servidor, necesitas una carpeta específica donde guardarás todas las imágenes que quieres mostrar.

    mkdir -p /var/www/html/images/mjml/imagenes_general: Este comando crea la estructura de directorios que necesitas. La opción -p es muy útil porque crea todos los directorios intermedios si no existen.

    chmod 777 /var/www/html/images/mjml/imagenes_general: Este comando otorga permisos completos (777 significa leer, escribir y ejecutar para todos) a la carpeta que acabas de crear. Esto es crucial para que Apache pueda acceder y servir las imágenes, y para que tú puedas subir archivos a ella más tarde.

## 4. Subida de Imágenes con SCP

Desde tu línea de comandos local (CMD o Terminal), usarás el comando scp (Secure Copy Protocol) para transferir tus imágenes de forma segura a tu instancia EC2.

    scp -i .RutaLlave -r RutaCarpetaImagenes ubuntu@IpInstanciaAWS:UbicaciónRutaDondeQuieroSubirImagenes
        scp: El comando para copiar archivos de forma segura.
        -i .RutaLlave: Especifica la ruta a tu archivo de llave (.pem) que usaste para conectarte a tu instancia EC2. Es esencial para la autenticación.
        -r: La opción -r es para copiar directorios recursivamente, lo que significa que copiará la carpeta y todo su contenido.
        RutaCarpetaImagenes: Esta es la ruta completa de la carpeta en tu computadora local donde tienes las imágenes.
        ubuntu@IpInstanciaAWS: Aquí indicas el usuario (ubuntu es el predeterminado para las AMI de Ubuntu en AWS) y la dirección IP pública de tu instancia EC2.
        :UbicaciónRutaDondeQuieroSubirImagenes: Después de los dos puntos, especificas la ruta completa en tu servidor donde quieres que se suban las imágenes. ¡Esta es la carpeta que creaste en el paso anterior!

## 5. Actualizando los Enlaces en MJML

En tu código MJML, donde tengas las etiquetas <img> o cualquier otra que haga referencia a una imagen, cambiarás la URL para que apunte a tu servidor.

    http://IpInstancia/images/mjml/imagenes_general/imagen.png: Aquí, IpInstancia es la dirección IP pública de tu instancia EC2.

