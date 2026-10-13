# REGLAS INQUEBRANTABLES DE DESARROLLO (PORTAFOLIO LOCAL V2.1)

El siguiente conjunto de reglas establece los límites técnicos y de diseño que **deben cumplirse obligatoriamente** durante la ejecución del plan de desarrollo local del portafolio en su versión 2.1. 

## 1. Reglas de Arquitectura y Entorno (Single-File)

* **1.1. Naturaleza Monolítica (El Mandato del Archivo Único):** El proyecto v2.1 se construirá en un **ÚNICO archivo `index.html`**. 
* **1.2. Inclusión de Estilos y Lógica:** Queda prohibida la creación de archivos `.css` o `.js` externos. Todo el diseño debe estar dentro de la etiqueta `<style>` en el `<head>`, y toda la lógica de interactividad dentro de la etiqueta `<script>` al final del `<body>`.
* **1.3. Cero Backend:** Prohibido el uso de servidores locales o bases de datos. Todo es procesado por el navegador o integrado vía iframes (nube).
* **1.4. Navegación Interna:** Las "páginas" (Inicio, Información, Proyectos, Contactos) deben ser implementadas como `<section>` dentro del mismo documento, navegables mediante anclas (Hash IDs) o mediante manipulación del DOM (JS) para simular el enrutamiento.

## 2. Reglas de Rendimiento (Performance)

* **2.1. Límite de Peso de Imágenes:** Ninguna imagen local superará los **150 KB**. Se priorizará el uso de URLs absolutas (imágenes alojadas en la nube) para reducir la dependencia de carpetas locales y maximizar la portabilidad del archivo `.html`.
* **2.2. Límite de Peso del Documento:** El peso del archivo `index.html` renderizado en el navegador (incluyendo medios) no excederá los **2.5 MB**.
* **2.3. Tiempo de Carga (LCP):** El renderizado del elemento más grande debe ser inmediato, siempre inferior a **1.0 segundo**.

## 3. Reglas de Accesibilidad y Diseño (UI/UX)

* **3.1. Cumplimiento WCAG 2.1 AA:** Todo el sitio debe apegarse a las directrices de accesibilidad web.
* **3.2. Contraste Obligatorio:** Legibilidad perfecta con un ratio de contraste superior a 4.5:1 sobre la paleta de color azul pastel base: `#E2EFF5`.
* **3.3. Etiquetas Semánticas y 'alt':** Uso estricto de HTML5 semántico (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`). Todas las etiquetas `<img>` deben incluir `alt="..."`.
* **3.4. Navegación por Teclado:** El archivo completo debe ser navegable usando solo `Tab` y `Enter`. Si se usan ventanas modales (Pop-ups) para los proyectos, el foco del teclado debe atraparse dentro del modal mientras esté abierto.
* **3.5. Responsividad Absoluta:** CSS adaptativo (media queries dentro del `<style>`) para pantallas desde 320px hasta 1920px+.

## 4. Reglas de Integración y Seguridad

* **4.1. Enlaces Externos Seguros:** Cualquier enlace (`<a>`) externo DEBE incluir: `target="_blank"` y `rel="noopener noreferrer"`.
* **4.2. Uso de Iframes Centralizados:** Se embeberá código para Google Forms (contacto), YouTube (videos) y Google Maps (ubicación). 
* **4.3. Descargas Nativas Nube:** CV y certificados serán enlaces a Google Drive con permisos públicos de visualización.

## 5. Reglas de Código y Mantenibilidad Interna

* **5.1. Nomenclatura Descriptiva:** Clases CSS e IDs en kebab-case (ej. `seccion-proyectos`).
* **5.2. Limpieza del Etiquetado:** Aunque el CSS viva en el mismo archivo, se **prohíbe el uso de estilos en línea** (`style="..."`) directamente en las etiquetas HTML, a menos que sean calculados dinámicamente por JS. Todo el CSS debe estar ordenado estructuralmente en la etiqueta `<style>`.
* **5.3. Comentarios Estructurales:** Debido a que el HTML, CSS y JS convivirán en el mismo archivo, es obligatorio el uso de comentarios extensos y separadores visuales en el código (ej. `/* --- SECCIÓN MIS PROYECTOS --- */`) para garantizar la mantenibilidad.