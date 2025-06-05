#### AMPLIACIÓN DEL RETO: CAMPAÑA DE MARKETING DIGITAL PARA FERIA VALENCIA

# Índice

1. [AMPLIACIÓN DEL RETO: CAMPAÑA DE MARKETING DIGITAL PARA FERIA VALENCIA](#ampliación-del-reto-campaña-de-marketing-digital-para-feria-valencia)
2. [Análisis y Planificación de la Campaña](#2-análisis-y-planificación-de-la-campaña)
   - [Análisis de Requerimientos](#21-análisis-de-requerimientos)
   - [Análisis DAFO y Competencia](#22-análisis-dafo-y-competencia)
   - [Objetivos de la Campaña](#23-objetivos-de-la-campaña)
3. [Diseño de la Campaña](#3-diseño-de-la-campaña)
   - [Concepto y Creatividad](#31-concepto-y-creatividad)
   - [Mockup (Figma)](#32-mockup-figma)
   - [Diseño Responsive Avanzado con MJML](#33-diseño-responsive-avanzado-con-mjml)
4. [Test con Usuarios](#4-test-con-usuarios)
   - [Metodología y Selección de Muestra](#41-metodología-y-selección-de-muestra)
   - [Feedback y Análisis](#42-feedback-y-análisis)
   - [Rediseño (si aplica)](#43-rediseño-si-aplica)
5. [Desarrollo y Envío de Correos](#5-desarrollo-y-envío-de-correos)
   - [Configuración del Entorno](#51-configuración-del-entorno)
   - [Automatización del Envío](#52-automatización-del-envío)
6. [Integración con Redes Sociales](#6-integración-con-redes-sociales)
7. [Control de Versiones con GitHub](#7-control-de-versiones-con-github)
   - [Configuración del Repositorio](#71-configuración-del-repositorio)
   - [Gestión del Proyecto](#72-gestión-del-proyecto)
8. [Gestión de Datos](#8-gestión-de-datos)
   - [Estructura de Datos](#81-estructura-de-datos)
   - [Diseño de Esquema de Base de Datos](#82-diseño-de-esquema-de-base-de-datos)
9. [Personalización del Correo MJML](#9-personalización-del-correo-mjml)
   - [Implementación de Variables](#91-implementación-de-variables)
   - [Impacto de la Personalización](#92-impacto-de-la-personalización)
10. [Verificación de Compatibilidad con Clientes de Correo](#10-verificación-de-compatibilidad-con-clientes-de-correo)
    - [Pruebas de Compatibilidad](#101-pruebas-de-compatibilidad)
11. [Documentación Final](#11-documentación-final)
    - [Guía de Usuario](#111-guía-de-usuario)
    - [Informe Final del Proyecto](#112-informe-final-del-proyecto)
12. [Entrega y Defensa del Proyecto](#12-entrega-y-defensa-del-proyecto)
    - [Plazos de Entrega](#121-plazos-de-entrega)
    - [Presentación (9–10 de junio)](#122-presentación-9–10-de-junio)


### 2. Análisis y Planificación de la Campaña

#### 2.1. Análisis de Requerimientos
- **Público Objetivo:** Es el punto de encuentro anual de toda la industria cerámica, el baño y la piedra natural. Organizada por Feria Valencia, es una cita internacional referente que se convierte en pasarela de tendencias y novedades sectoriales y foro de conocimiento e innovación para los profesionales.

#### 2.2. Análisis DAFO y Competencia
- **DAFO de la Campaña:** Identificación de Debilidades, Amenazas, Fortalezas y Oportunidades. 

  **DEBILIDADES**
  - Contraste de colores
  - Posibles Problemas de Compatibilidad de Fuentes Personalizadas
  
  **AMENAZAS**
  - Filtros de Spam
  - Competencia de Otros Eventos
  - Saturación del usuario: Riesgo de que el correo sea ignorado o marcado como spam.

  **FORTALEZAS**
  - Diseño Visual Atractivo y Empresarial.
  - Estructura Clara y Jerárquica.
  - Elementos Interactivos y Llamadas a la Acción (CTAs)
  - Inclusión de Redes Sociales

  **OPORTUNIDADES**
  - Contenido Dinámico
  - Patrocinios/Colaboraciones
  - Segmentación y Personalización

- **Análisis de la Competencia:** He visto unas cuantas newsletters y la verdad que en cuanto a diseño el resto las he visto más estéticas y bonitas, pero la mía, en mi opinión, atrae más la atención del público empresarial.

#### 2.3. Objetivos de la Campaña

- **Definición de objetivos:** Que vean la newsletter y cuando vean la frase principal de Potenciamos tu negocio, que se paren a leer un poco y les den ganas de darle al botón de participar.

### 3. Diseño de la Campaña

#### 3.1. Concepto y Creatividad
- **Innovación y Creatividad:** Los colores y la manera de llamar la atención del público.

#### 3.2. Mockup (Figma)
- **Representación Visual Previa:** [ENLACE FIGMA](https://www.figma.com/design/QKgsSzZl3QFsdNSkp4NFeF/Untitled?node-id=0-1&t=t4bWppePv70JkaPo-1)
- **Justificación del Diseño:**
  - **Audiencia:** Gente que quiere hacer crecer su empresa y conseguir contactos.
  - **Motivación:** Porque me gusta bastante el mundo empresarial
  - **Elementos Visuales Clave:** Las imagenes atraen bastante la atencion
  - **Jerarquía Visual:** Primero ves el título relevante, luego pasas a las imágenes, después al texto explicativo y por último al botón de acceso a la web.


### 4. Test con Usuarios

#### 4.1. [ENLACE FORMULARIO GOOGLE FORMS](https://docs.google.com/forms/d/e/1FAIpQLSfGSO_K2KzLAyvUH52GzwNddG9pGBTl-v7diAU57eO5INwKCQ/viewform?usp=dialog)
#### 4.2. [Feedback y Análisis](https://docs.google.com/spreadsheets/d/1iZfOAwaGqzh3IPDsNMY9SJmjt-9UL-VZYpJGR9SLvqI/edit?usp=sharing)


#### 4.3. Rediseño (si aplica)
- **Iteración del Diseño:** He mejorado más la apariencia en general y también le he puesto más contenido haciendo publicidad a la feria.

### 5. Desarrollo y Envío de Correos

#### 5.1. Configuración del Entorno
- **Tecnologías:** AWS EC2, MJML, Node.js (JavaScript).

#### 5.2 [Documentacion AWS proceso entero](https://github.com/alvaro006/practicas_feria/blob/master/supuesto1/documentacion%20AWS.md)

### 6. Integración con Redes Sociales

- **Compartir Contenido:** Cómo se compartirá la newsletter como enlace en plataformas como Telegram o LinkedIn.
- **Contenido Visual:** Descripción de la creación de Reels, carruseles de imágenes, vídeos cortos para TikTok/Reels o capturas para Stories de Instagram, basándose en el contenido del correo.

### 7. Control de Versiones con GitHub

#### 7.1. Configuración del Repositorio
- **Repositorio:** [ENLACE AL REPOSITORIO DE (GitHub)](https://github.com/alvaro006/practicas_feria.git)
- **Integración en VS Code:** Utilice la extensión de MJML para desarrollar la newsletter.

#### 7.2. Gestión del Proyecto
- **Commits Regulares:** [ENLACE COMMITS DE (GitHub)](http://github.com/alvaro006/practicas_feria/commits/master/)
- **Uso de Ramas:** Estoy utilizando directamente la rama master porque si hay cambios que no me gustan, hago un `git reset` para eliminar el commit o `git commit --amend` para modificarlo.

### 8. Gestión de Datos

#### 8.1. Estructura de Datos
- **Base de Datos (MySQL en AWS):** Configuración y uso.

#### 8.2. Diseño de Esquema de Base de Datos
- **Descripción de Estructura:** Justificación de la estructura para el reto seleccionado.
- **Modelado ER:** Diagrama Entidad-Relación.
- **Normalización a Tablas:**
- **suscriptores:** nombre, email, fecha_registro, ...

### 9. Personalización del Correo MJML
 
#### 9.1. Implementación de Variables
- **Uso de Variables:** Cómo se utilizan variables (nombre, empresa, idioma, etc.) para personalizar el correo.

### 10. Verificación de  Compatibilidad con Clientes de Correo

#### 10.1. Pruebas de Compatibilidad
- **Enfoque en Outlook:** Detalle de las pruebas realizadas para asegurar la correcta visualización en diferentes clientes, con especial atención a Outlook.

### 11. Documentación Final

#### 11.1. Guía de Usuario
- **Instrucciones:** Cómo modificar, enviar y adaptar la campaña.