# Guía de Configuración y Ejecución

## 1. Preparación de la Clave SSH y Conexión al Servidor

- **`chmod 400 /ruta/a/tu/archivo/mi-key-pair.pem`**: Asegura la clave SSH. Cambia permisos del archivo de clave privada a 400 (solo lectura para el propietario) por seguridad.

- **`ssh -i ./Descargas/llave.pem ubuntu@””IP””`**: Conecta al servidor remoto. Inicia sesión SSH usando la clave (-i), el usuario ubuntu y la IP del servidor.

## 2. Configuración de Node.js

- **`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`**: Instala NVM (Node Version Manager). Descarga y ejecuta el script de instalación de NVM.

- **`exit`**: Cierra la sesión SSH. Necesario para que los cambios de NVM se apliquen en una nueva sesión.

- **`nvm install --lts`**: Instala la versión LTS de Node.js. NVM descarga e instala la última versión de soporte a largo plazo de Node.js.

- **`nvm use --lts`**: Activa la versión LTS de Node.js. Establece la versión LTS como la activa para la sesión.

- **`node -v`**: Verifica la versión de Node.js. Muestra la versión activa de Node.js.

- **`npm -v`**: Verifica la versión de NPM. Muestra la versión activa de NPM.

## 3. Gestión y Limpieza de MySQL (Preparación)

- **`sudo apt update`**: Actualiza la lista de paquetes. Sincroniza índices de paquetes de repositorios.

- **`sudo apt install mysql-client-core-8.0`**: Instala el cliente MySQL. Instala el cliente básico para interactuar con bases de datos MySQL.

- **`sudo apt update && sudo apt upgrade -y`**: Actualiza el sistema. Actualiza todos los paquetes instalados.

- **`sudo apt autoremove --purge 'mysql*' 'mariadb*' -y`**: Elimina instalaciones previas de MySQL/MariaDB. Desinstala y purga completamente cualquier rastro anterior.

- **`sudo apt autoclean && sudo apt clean`**: Limpia el caché de paquetes. Elimina paquetes descargados innecesarios.

- **`sudo rm -rf /etc/mysql /var/lib/mysql /var/log/mysql /var/run/mysqld`**: Elimina directorios de configuración y datos de MySQL. Borra forzadamente directorios para una instalación limpia.

- **`sudo rm -rf /etc/mysql/conf.d`**: Elimina el directorio de configuraciones adicionales de MySQL.

## 4. Instalación del Servidor MySQL

- **`sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y`**: Actualiza el sistema (de nuevo). Asegura que el sistema esté completamente actualizado.

- **`sudo apt install mysql-server -y`**: Instala el servidor MySQL. Descarga e instala el software del servidor de base de datos.

- **`sudo systemctl status mysql`**: Verifica el estado del servidor MySQL. Muestra si el servicio MySQL está en ejecución.

- **`sudo mysql_secure_installation`**: Configura la seguridad de MySQL. Ejecuta un script interactivo para mejorar la seguridad (contraseña root, eliminar usuarios anónimos, etc.).

## 5. Interacción con la Base de Datos

- **`sudo mysql -u root -p`**: Accede a MySQL como usuario root. Inicia sesión en la consola de MySQL como root.

- **`mysql -u newsletter_user -p newsletter_db`**: Accede a una base de datos específica. Conecta a la base de datos `newsletter_db` con el usuario `newsletter_user`.

- **`CREATE TABLE clients ( id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255) NOT NULL, email VARCHAR(255) NOT NULL UNIQUE, created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP );`**: Crea la tabla `clients`. Define la estructura de una tabla para clientes con ID, nombre, email y fecha de creación.

- **`INSERT INTO clients (name, email) VALUES ('roberto', 'robertomoramoreno3@gmail.com'), ('alvaro', 'alvaromurillopuchalt06@gmail.com');`**: Inserta datos de ejemplo. Añade dos registros de clientes a la tabla `clients`.

- **`EXIT;`**: Sale de la consola de MySQL.

## 6. Configuración de Variables de Entorno

- **`nano .env`**: Edita el archivo de variables de entorno. Abre el editor para crear/modificar el archivo `.env`.

- **`DB_HOST=localhost ... EMAIL_PASSWORD=nxlu clhi hbqp pzlc`**: Define variables de entorno. Configura credenciales de base de datos y correo electrónico en `.env`.

## 7. Configuración del Proyecto Node.js

- **`mkdir newsletter-sender`**: Crea el directorio del proyecto. Crea una nueva carpeta para la aplicación.

- **`cd newsletter-sender/`**: Navega al directorio del proyecto.

- **`npm init -y`**: Inicializa el proyecto Node.js. Crea un archivo `package.json` con valores predeterminados.

- **`npm install mjml mysql2 nodemailer dotenv`**: Instala dependencias. Descarga e instala las librerías necesarias (`mjml`, `mysql2`, `nodemailer`, `dotenv`).

## 8. Creación de la Plantilla de Correo

- **`nano mjml-template.mjml`**: Crea la plantilla de correo MJML. Abre el editor para escribir el código de la plantilla de email en formato MJML.

- **Código del MJML**: Contenido de la plantilla MJML. Placeholder para el diseño y estructura del correo electrónico.

## 9. Desarrollo del Script de Envío de Correos (`index.js`)

- **`nano index.js`**: Crea el script principal de la aplicación. Abre el editor para escribir el código JavaScript.

- **`require('dotenv').config();`**: Carga variables de entorno. Carga las variables de `.env` al inicio del script.

- **`const mjml2html = require('mjml'); ...`**: Importa módulos. Carga las librerías necesarias para la aplicación.

- **`async function main() { ... }`**: Función principal asíncrona. Contiene la lógica central.

    - **Conexión a la Base de Datos MySQL**: Establece conexión con la base de datos usando credenciales de `.env`.

    - **Lectura de datos de clientes**: Consulta la tabla `clients` para obtener nombres y correos.

    - **Cargar y compilar la plantilla MJML**: Lee `mjml-template.mjml`, lo compila a HTML y maneja errores.

    - **Configurar Nodemailer**: Crea un "transportador" de correo electrónico con credenciales de `.env`.

    - **Enviar correos a cada cliente**: Itera sobre clientes, personaliza el HTML con el nombre y envía el email, manejando errores individuales.

    - **Manejo de Errores y Cierre**: Captura errores generales y asegura el cierre de la conexión a MySQL.

- **`main();`**: Ejecuta la función principal. Inicia la ejecución del script.

## 10. Ejecución del Script

- **`node index.js`**: Ejecuta la aplicación Node.js. Inicia el script `index.js` para realizar todas las operaciones.
