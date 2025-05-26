#### AMPLIACIÓN DEL RETO: CAMPAÑA DE MARKETING DIGITAL PARA FERIA VALENCIA

### 2. Análisis y Planificación de la Campaña

#### 2.1. Análisis de Requerimientos
- **Público Objetivo:** El público que se orienta este trabajo es para los amantes del motociclismo o gente joven de 12 a 35 años en general.

#### 2.2. Análisis DAFO y Competencia
- **DAFO de la Campaña:** Identificación de Debilidades, Amenazas, Fortalezas y Oportunidades. 

  **DEBILIDADES**
  - Contraste: El botón de llamada a la acción podría destacar más.
  
  **AMENAZAS**
  - Redes Sociales: Enlace de YouTube inactivo y enlaces a redes sociales incorrectos.
  - Versión MJML: Uso de versión antigua, considerar la más reciente.
  - Saturación del usuario: Riesgo de que el correo sea ignorado o marcado como spam.
  - Problemas de compatibilidad: Visualización inconsistente del correo en diferentes clientes de correo (especialmente Outlook) o dispositivos.
  - Ciberseguridad: Riesgo de intentos de phishing o suplantación de identidad que dañen la confianza en la marca.

  **FORTALEZAS**
  - Uso de MJML: Permite un diseño responsive robusto y optimizado para email.
  - Integración Tecnológica: Capacidad para automatizar envíos con AWS EC2, Node.js y bases de datos MySQL.
  - Personalización Avanzada: Posibilidad de crear correos altamente personalizados usando datos de suscriptores.
  - Control de Versiones: Uso de GitHub para un desarrollo colaborativo y organizado.

  **OPORTUNIDADES**
  - Expansión de Audiencia: Utilizar la integración con redes sociales para alcanzar nuevos segmentos y amplificar el mensaje.
  - Análisis y Optimización: Emplear el feedback del test con usuarios para mejorar continuamente la efectividad de las campañas.
  - Diferenciación: Destacar frente a la competencia con un diseño responsive avanzado y una experiencia de usuario cuidada.

- **Análisis de la Competencia:** He visto unas cuantas newsletters y la verdad que en cuanto a diseño el resto las he visto más estéticas y bonitas, pero la mía, en mi opinión, atrae más la atención del público.

#### 2.3. Objetivos de la Campaña
- **Definición de objetivos:** Que vean la newsletter y cuando vean la frase principal de sorteo de MotoGP, que se paren a leer un poco y les den ganas de darle al botón de participar.

### 3. Diseño de la Campaña

#### 3.1. Concepto y Creatividad
- **Innovación y Creatividad:** Los colores y la manera de llamar la atención del público.

#### 3.2. Mockup (Figma)
- **Representación Visual Previa:** [ENLACE FIGMA]
- **Justificación del Diseño:**
  - **Audiencia:** Amantes de los vehículos a dos ruedas y gente joven.
  - **Motivación:** Porque me gusta bastante la competición de automóviles.
  - **Elementos Visuales Clave:** Las cosas más relevantes de este código serían el color degradado, el botón añadiéndole curva con `border-radius` y también el `mj-divider` para separar contenido.
  - **Jerarquía Visual:** Primero ves el título relevante, luego pasas a las imágenes, después al texto explicativo y por último al botón de acceso a la web.

#### 3.3. Diseño Responsive Avanzado con MJML
- **Implementación de Media Queries:** Detalle de las 3 media queries utilizadas.
- **Personalización por Dispositivo:** Explicación de cómo el diseño cambia o los elementos se ocultan según el tamaño de la pantalla.

### 4. Test con Usuarios

#### 4.1. Metodología y Selección de Muestra
- **Participantes:** Descripción de la muestra (al menos 10 personas reales: profesores, compañeros, familiares).
- **Herramienta:** Indicar la herramienta usada para el formulario (Microsoft Forms, Google Forms o similar).

#### 4.2. Feedback y Análisis
- **Recogida de Datos:** Proceso para recolectar las respuestas de la encuesta.
- **Análisis de Resultados:** Presentación de los resultados de la encuesta, incluyendo gráficos y conclusiones clave.

#### 4.3. Rediseño (si aplica)
- **Iteración del Diseño:** He mejorado más la apariencia en general y también le he puesto más contenido haciendo publicidad a la feria.

### 5. Desarrollo y Envío de Correos

#### 5.1. Configuración del Entorno
- **Tecnologías:** AWS EC2, MJML, Node.js (JavaScript).

#### 5.2. Automatización del Envío
- **Lectura de Datos:** Proceso para leer datos de clientes.
- **Integración de Envío:** Descripción de la automatización del envío de correos utilizando Gmail u O365.

### 6. Integración con Redes Sociales

#### 6.1. Estrategias de Integración
- **Compartir Contenido:** Cómo se compartirá la newsletter como enlace en plataformas como Telegram o LinkedIn.
- **Contenido Visual:** Descripción de la creación de Reels, carruseles de imágenes, vídeos cortos para TikTok/Reels o capturas para Stories de Instagram, basándose en el contenido del correo.

### 7. Control de Versiones con GitHub

#### 7.1. Configuración del Repositorio
- **Repositorio:** [ENLACE AL REPOSITORIO DE (GitHub)]
- **Integración en VS Code:** Utilice la extensión de MJML para desarrollar la newsletter.

#### 7.2. Gestión del Proyecto
- **Commits Regulares:** [ENLACE COMMITS DE (GitHub)]
- **Uso de Ramas:** Estoy utilizando directamente la rama master porque si hay cambios que no me gustan, hago un `git reset` para eliminar el commit o `git commit --amend` para modificarlo.

### 8. Gestión de Datos

#### 8.1. Estructura de Datos
- **Lectura de CSV:** Proceso para leer datos de suscriptores desde un archivo CSV.
- **Base de Datos (MySQL en AWS):** Configuración y uso.

#### 8.2. Diseño de Esquema de Base de Datos
- **Descripción de Estructura:** Justificación de la estructura para el reto seleccionado.
- **Modelado ER:** Diagrama Entidad-Relación.
- **Normalización a Tablas:**
  - **suscriptores:** nombre, email, empresa, idioma, fecha_registro, ...
  - **historial_envios:** suscriptor_id, fecha_envio, asunto, estado_envio, ...
  - **Otras tablas consideradas necesarias** (ej: newsletter, campañas, sorteos).
- **Inserción de Datos:** Detalles de la inserción de datos ficticios o reales para pruebas.
- **Documentación:** Comentarios y justificaciones en cada paso del diseño de la base de datos.

### 9. Personalización del Correo MJML

#### 9.1. Implementación de Variables
- **Uso de Variables:** Cómo se utilizan variables (nombre, empresa, idioma, etc.) para personalizar el correo.

#### 9.2. Impacto de la Personalización
- **Análisis del Test:** Evaluación del impacto de los correos personalizados vs. genéricos en el test con usuarios.

### 10. Verificación de Compatibilidad con Clientes de Correo

#### 10.1. Pruebas de Compatibilidad
- **Enfoque en Outlook:** Detalle de las pruebas realizadas para asegurar la correcta visualización en diferentes clientes, con especial atención a Outlook.

### 11. Documentación Final

#### 11.1. Guía de Usuario
- **Instrucciones:** Cómo modificar, enviar y adaptar la campaña.

#### 11.2. Informe Final del Proyecto
- **Objetivos del Proyecto:** Resumen de los objetivos iniciales.
- **Análisis y Público Objetivo:** Recap de las fases de análisis.
- **Diseño y Justificación:** Descripción del diseño y sus motivos.
- **Solución Técnica:** Detalle de las herramientas y el desarrollo implementado.
- **Test de Usuarios:** Resultados de las encuestas, gráficos y feedback.
- **Integración con Redes:** Descripción de las estrategias y resultados de la integración.
- **Conclusiones y Posibles Mejoras:** Reflexiones finales y sugerencias para futuras iteraciones.

### 12. Entrega y Defensa del Proyecto

#### 12.1. Plazos de Entrega
- **Entrega Digital:** GitHub y web de Feria Valencia (hasta el 6 de junio).

#### 12.2. Presentación (9–10 de junio)
- **Breve Presentación:** Contenido clave a destacar en los 5 minutos.
- **Demostración Funcional:** Versión web del correo y envío real.
- **Resultados Test:** Presentación de los resultados obtenidos con los usuarios.
- **Proceso de Desarrollo:** Explicación de las herramientas y el flujo de trabajo.
- **Conclusión y Mejoras:** Cierre del proyecto y futuras propuestas.
