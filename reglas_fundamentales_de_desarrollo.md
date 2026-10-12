# REGLAS INQUEBRANTABLES DE DESARROLLO (PORTAFOLIO LOCAL)

El siguiente conjunto de reglas establece los límites técnicos y de diseño que **deben cumplirse obligatoriamente** durante la ejecución del plan de desarrollo local del portafolio. Aunque el código es susceptible a mejoras iterativas, estas directrices son el núcleo del dictamen del proyecto y no pueden ser evadidas.

## 1. Reglas de Arquitectura y Entorno
*   **1.1. Naturaleza Estática (Local-First):** El proyecto se construirá **única y exclusivamente** con tecnologías frontend (HTML5, CSS3 y JavaScript nativo/Vanilla JS). 
*   **1.2. Cero Backend:** Queda estrictamente prohibido el uso de servidores locales (como XAMPP, Node.js, Python Flask) para renderizar vistas, así como el uso de bases de datos relacionales o no relacionales (MySQL, MongoDB, etc.). Toda la información debe estar en el código o consumida vía integraciones en la nube (iframes/APIs web).
*   **1.3. Portabilidad:** El proyecto completo debe poder ejecutarse haciendo simple "doble clic" en el archivo `index.html` desde cualquier explorador de archivos local en Windows, macOS o Linux, sin necesidad de configuraciones previas.

## 2. Reglas de Rendimiento (Performance)
*   **2.1. Límite de Peso de Imágenes:** Ninguna imagen (JPG, PNG, WebP, GIF) alojada en la carpeta del proyecto podrá superar los **150 KB** de peso.
*   **2.2. Límite de Peso por Página:** El peso total de descarga de cualquier vista completa (HTML + CSS + Imágenes + JS) no deberá exceder los **2.5 MB**.
*   **2.3. Tiempo de Carga (LCP):** El *Largest Contentful Paint* (tiempo que tarda en renderizarse el elemento más grande de la pantalla) debe mantenerse siempre por debajo de **1.0 segundo** en un entorno local.

## 3. Reglas de Accesibilidad y Diseño (UI/UX)
*   **3.1. Cumplimiento WCAG 2.1 AA:** Todo el sitio debe apegarse a las directrices de accesibilidad web nivel AA.
*   **3.2. Contraste Obligatorio:** Los colores de texto y botones deben garantizar una legibilidad perfecta (ratio de contraste superior a 4.5:1) específicamente sobre la paleta de color azul pastel base del proyecto: `#E2EFF5`.
*   **3.3. Etiquetas Semánticas y 'alt':** Absolutamente todas las etiquetas `<img>` deben contener el atributo `alt="..."` describiendo su contenido para los lectores de pantalla. Se exigirá el uso de HTML5 semántico (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).
*   **3.4. Navegación por Teclado:** El sitio entero (botones, enlaces, tarjetas, formularios) debe poder navegarse de principio a fin utilizando únicamente la tecla `Tab` y la tecla `Enter`.
*   **3.5. Responsividad Absoluta:** Ningún elemento visual debe desbordarse, ocultarse erróneamente o romper el layout al redimensionar la ventana del navegador desde resoluciones móviles (320px) hasta pantallas ultra anchas (1920px+).

## 4. Reglas de Integración y Seguridad
*   **4.1. Enlaces Externos Seguros:** Cualquier enlace (`<a>`) que apunte fuera del entorno local (por ejemplo, a GitHub, LinkedIn, o Google Drive) DEBE incluir forzosamente los atributos: `target="_blank"` y `rel="noopener noreferrer"`.
*   **4.2. Uso de Iframes:** Las herramientas dinámicas deben estar aisladas. El formulario de contacto se hará mediante *Google Forms embebido*, los videos mediante *YouTube embebido*, y los mapas con *Google Maps embebido*. No se programarán desde cero estas soluciones.
*   **4.3. Descargas Nativas Nube:** El Curriculum Vitae y los certificados no vivirán en la carpeta local, sino que se enlazarán hacia Google Drive configurados en modo "Cualquier persona con el enlace puede ver/descargar" para simular la nube real.

## 5. Reglas de Código y Mantenibilidad
*   **5.1. Nomenclatura Descriptiva:** Los nombres de clases CSS, variables JS, identificadores de archivos e IDs deben ser claros, en minúsculas y separados por guiones (kebab-case). Ejemplo: `tarjeta-proyecto-software`, no `tps1`.
*   **5.2. Componentización CSS:** Se evitará el uso excesivo de estilos en línea (`style="..."` dentro del HTML). Todo el diseño principal vivirá en un archivo (o archivos modulares) `.css`.
*   **5.3. Registro de Cambios (Changelog):** Todo avance o corrección de bugs identificada durante el salto de la iteración T14 a la T10BLAS deberá quedar documentada para futuras auditorías académicas.