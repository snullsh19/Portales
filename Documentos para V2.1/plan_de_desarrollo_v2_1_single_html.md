# ESPECIFICACIONES PARA LA EJECUCIÓN DEL PLAN DEL SITIO WEB PORTAFOLIO (VERSIÓN 2.1 - ARCHIVO ÚNICO LOCAL)

## 1. Contexto y Objetivo del Plan
Este documento define el plan estratégico y técnico para la **versión 2.1** del portafolio web profesional de Shuha Emilio Blas Santos. El objetivo central es ejecutar el plan para terminar el sitio al 100% y utilizarlo estrictamente de manera local, con una nueva restricción arquitectónica: **todo el proyecto debe estar contenido en un único archivo HTML**.

## 2. Diagnóstico del Sistema Actual
El análisis preliminar de la Línea Base estableció cuatro apartados visuales. Sin embargo, para esta versión 2.1, se ha detectado que la gestión de múltiples archivos puede entorpecer la portabilidad en entornos estrictamente locales. Por ello, se transiciona a un modelo de un solo documento que consolide la información profunda (perfil dual, proyectos y contacto) sin perder la estructura de navegación.

## 3. Arquitectura y Restricciones del Entorno Local (Single-File)
Para compilar la versión 2.1 de manera local respetando la arquitectura requerida:
* **Maquetación Monolítica (Un solo HTML):** Todo el proyecto (HTML, CSS y JS) vivirá dentro de un único archivo llamado `index.html`.
* **Navegación Interna (SPA Estática):** El menú superior redirigirá a secciones dentro del mismo documento (mediante anclas `#id` o manipulando la visibilidad con JavaScript) para simular el cambio de página sin recargar.
* **Componentes de Red Embebidos:** La interactividad y gestión de datos se apoyará nativamente mediante etiquetas `<iframe>` o llamadas a la nube (Google Drive, Forms, YouTube, GitHub).
* **Rendimiento:** Todas las imágenes integradas localmente deben estar comprimidas (< 150 KB) o, idealmente, consumidas desde rutas absolutas (nube) si se desea que el archivo HTML sea 100% independiente de carpetas locales.

## 4. Especificaciones Funcionales por Sección (Antes Módulos)
El archivo único compartirá de forma persistente un menú superior (*Navbar*) con botones para redirigir entre las siguientes **secciones internas**, finalizando con un *Footer* institucional.

### 4.1. Sección "Inicio" (`<section id="inicio">`)
* **Identidad Jerárquica:** Letrero principal (H1) que indique "Hola!, Soy Shuha Emilio".
* **Subtítulo:** Texto "Desarrollar de software y proyectos mecatrónicos" (H2).
* **Multimedia:** Dos fotografías estáticas (software e impresión 3D/mecatrónica).
* **Llamadas a la Acción (CTA):** Botones enlazados internamente a `#proyectos` y externamente hacia Google Drive (CV).

### 4.2. Sección "Mi Información" (`<section id="informacion">`)
* **Perfil Dual:** Estructura de dos columnas (fotografía personal y texto del perfil dual Técnico/Ingeniero).
* **Matriz de Habilidades:** Cuadrícula visual dividiendo el stack tecnológico (Software vs Mecatrónica).
* **Visualización Dinámica:** Carrusel de proyectos (controlado por JS nativo dentro del mismo archivo).
* **Descarga de CV:** Botón interactivo a Drive.
* **Trayectoria y Certificaciones:** Línea cronológica (2024-2026) con enlaces a certificados en Drive.

### 4.3. Sección "Mis Proyectos" (`<section id="proyectos">`)
* **Segmentación Independiente:** Catálogo visual dividido en 'Software' y 'Mecatrónica'.
* **Tarjetas Modulares:** Elementos de interfaz (Cards) con miniatura, título y descripción.
* **Vista Detallada (Modales):** Al estar en un solo HTML, los detalles técnicos, etiquetas, visores PDF o iframes de YouTube se abrirán preferentemente en ventanas modales (Pop-ups creados con HTML/CSS/JS) sobre la misma interfaz. Redirección a GitHub.

### 4.4. Sección "Mis Contactos" (`<section id="contactos">`)
* **Formulario Seguro Embebido:** Uso de `<iframe>` apuntando a Google Forms.
* **Accesos y Redes:** Botones hacia LinkedIn, GitHub y correo.
* **Interactividad Extra:** "Insignia de Disponibilidad" (status badge), vCard (Código QR) y mapa de Google Maps (UAEM Tianguistenco) vía iframe.

## 5. Especificaciones No Funcionales
* **Diseño Responsivo:** CSS fluido adaptativo a móviles, tablets y escritorio.
* **Accesibilidad (WCAG 2.1 AA):** Contraste válido sobre `#E2EFF5`, etiquetas `alt` y navegación completa por teclado (Tabulación).
* **Peso Total (Single-File):** El archivo `index.html` junto con sus recursos locales cargados no debe superar los 2.5 MB.
* **Seguridad:** Enlaces externos con `target="_blank"` y `rel="noopener noreferrer"`.

## 6. Cronograma de Ejecución (Plan de Sprints Ágiles v2.1)
1. **Sprint 0 (Esqueleto de Archivo Único):** Creación del `index.html` con `<style>` y `<script>` integrados. Configuración del Navbar persistente y las 4 secciones principales (`#inicio`, `#informacion`, `#proyectos`, `#contactos`) con funcionalidad de navegación interna.
2. **Sprint 1 (Información Personal):** Maquetación de la sección `#informacion` (perfil dual, matriz de habilidades, carrusel con JS nativo).
3. **Sprint 2 (Catálogo de Proyectos):** Codificación de la sección `#proyectos` (tarjetas e implementación de modales para detalles sin salir del archivo).
4. **Sprint 3 (Medios de Contacto):** Integración de iframes (Forms, Maps) y botones sociales en la sección `#contactos`.
5. **Sprint 4 (Refinamiento CSS y JS):** Optimización del código CSS dentro de `<style>`, verificación de contraste, inserción de `alt` y mejora de la lógica de navegación por teclado.
6. **Sprint 5 (Elementos Especiales):** Agregado del QR (vCard), botón de copiar al portapapeles y línea de tiempo académica.
7. **Sprint 6 (Auditoría Final v2.1):** Prueba de portabilidad (abrir el archivo en distintos equipos sin carpetas externas que lo rompan), verificación de peso < 2.5MB y documentación.