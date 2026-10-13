\*\*\*

\# ESPECIFICACIONES PARA LA EJECUCIÓN DEL PLAN DEL SITIO WEB PORTAFOLIO (VERSIÓN 100% LOCAL)

\#\# 1\. Contexto y Objetivo del Plan  
Este documento define el plan estratégico y técnico para finalizar la creación y mejora de la segunda versión del portafolio web profesional de Shuha Emilio Blas Santos. El objetivo central es ejecutar el plan para terminar el sitio al 100% y \*\*utilizarlo estrictamente de manera local\*\*. Esto permitirá revisar el código y la presentación offline, probar las implementaciones y experimentar con mejoras iterativas previas a una publicación futura en plataformas alojadas.

\#\# 2\. Diagnóstico del Sistema Actual  
El análisis preliminar revela que la primera versión (Línea Base) configuró satisfactoriamente una estructura visual y de navegación basada en cuatro apartados (Inicio, Mi Información, Mis Proyectos y Mis Contactos). Sin embargo, se identificaron limitaciones críticas para un producto terminado:  
\*   \*\*Contenido insuficiente:\*\* Las secciones carecen de información profunda. Especialmente en el rubro de proyectos, se omiten trabajos relevantes que demuestran la dualidad técnica entre el desarrollo de software (Java, Python, C, SQL) y la mecatrónica (PIC18F4550, Arduino, CNC, impresión 3D).  
\*   \*\*Contacto y validación curricular básica:\*\* Falta un formulario funcional e interactivo y opciones de descarga directa de un Curriculum Vitae que facilite a los reclutadores el contacto directo y profesional.  
\*   \*\*Experiencia de uso:\*\* Es necesario optimizar el rendimiento, asegurar la accesibilidad y enriquecer el recorrido del usuario para fortalecer la presentación académica y profesional.

\#\# 3\. Arquitectura y Restricciones del Entorno Local  
Para compilar la versión 100% completa de manera local respetando la arquitectura técnica requerida por el dictamen del proyecto, se aplicarán las siguientes directrices (según T10BLAS.xlsx y los requerimientos funcionales):  
\*   \*\*Maquetación Estática Estricta:\*\* El entorno local constará exclusivamente de archivos estáticos (HTML/CSS). Queda prohibido el uso de servidores backend locales, cargas dinámicas o conexión a bases de datos relacionales propias.  
\*   \*\*Componentes de Red Embebidos:\*\* La interactividad y gestión de datos se apoyará nativamente mediante etiquetas \`\<iframe\>\` o llamadas API externas hacia servicios en la nube: Google Drive (visualización de CV y certificados), Google Forms/Sheets (recolección de mensajes), YouTube (videos de máquinas) y GitHub (código fuente) (según arquitectura T10BLAS.xlsx).  
\*   \*\*Rendimiento Ligero (LCP \< 1.0s):\*\* Todas las imágenes integradas a la carpeta local del proyecto deben estar fuertemente comprimidas sin exceder los 150 KB de peso individual, garantizando fluidez de carga.

\#\# 4\. Especificaciones Funcionales por Módulo (Requerimientos)  
El proyecto local deberá contar con cuatro archivos raíz, los cuales compartirán de forma persistente un menú superior (\*Navbar\*) con botones para redirigir entre vistas internas y un \*Footer\* (pie de página) institucional con derechos de autor.

\#\#\# 4.1. Módulo "Inicio" (\`index.html\` / Portada)  
\*   \*\*Identidad Jerárquica:\*\* Mostrar un letrero principal (H1) que indique exactamente "Hola\!, Soy Shuha Emilio".  
\*   \*\*Subtítulo:\*\* Renderizar debajo el texto "Desarrollar de software y proyectos mecatrónicos" (H2).  
\*   \*\*Multimedia:\*\* Mostrar dos fotografías rectangulares estáticas en la sección central inferior (una que simbolice código/software y otra ilustrando impresión 3D/mecatrónica).  
\*   \*\*Llamadas a la Acción (CTA):\*\* Implementar dos botones principales: uno de navegación hacia los proyectos y otro enlazando hacia Google Drive para ver/descargar el CV (especificado en los wireframes de T10BLAS.xlsx).

\#\#\# 4.2. Módulo "Mi Información" (\`informacion.html\`)  
\*   \*\*Perfil Dual:\*\* Diseñar una estructura en dos columnas. La columna izquierda mostrará una fotografía personal formal del autor, y la columna adyacente albergará texto narrando la trayectoria dual técnica en Ingeniería de Software y Mecatrónica.  
\*   \*\*Matriz de Habilidades:\*\* Agregar una cuadrícula divisoria clara que separe explícitamente el stack tecnológico en Software y en hardware/Mecatrónica.  
\*   \*\*Visualización Dinámica:\*\* Incorporar un carrusel dinámico interactivo, inmediatamente debajo del perfil, que cicle imágenes de los proyectos realizados.  
\*   \*\*Descarga de CV:\*\* Integrar un botón interactivo (sin necesidad de logueo o credenciales) configurado para la descarga del PDF del Curriculum Vitae.  
\*   \*\*Trayectoria y Certificaciones:\*\* Desplegar una línea cronológica (\*timeline\*) con su historial académico (Técnico 2024, Sistemas 2025, Ingeniería 2026\) y presentar certificados comprobables con hipervínculos a Drive (según especificaciones en T10BLAS.xlsx).

\#\#\# 4.3. Módulo "Mis Proyectos" (\`proyectos.html\`)  
\*   \*\*Segmentación Independiente:\*\* Construir un catálogo visual categorizado claramente en 'Proyectos de Software' y 'Proyectos de Mecatrónica'.  
\*   \*\*Tarjetas Modulares:\*\* Cada proyecto será expuesto a través de una tarjeta (Card) homogénea conteniendo una imagen miniatura, título y una breve descripción.  
\*   \*\*Vista Detallada e Ingeniería:\*\* Cada tarjeta debe permitir abrir detalles avanzados del proyecto, la cual debe incluir:  
    \*   Una descripción técnica de la arquitectura de software/hardware, los retos de ingeniería y algoritmos resueltos, y el rol del desarrollador (según requerimientos de T10BLAS.xlsx).  
    \*   Etiquetas/Insignias (\*Tags\*) descriptivas de las herramientas utilizadas.  
    \*   Multimedia embebida de evidencias en tiempo real (videos \*iframe\* de YouTube o animaciones GIF sobre el funcionamiento) (documentado en T10BLAS.xlsx).  
    \*   Un botón/enlace interactivo de redirección al repositorio oficial en GitHub.

\#\#\# 4.4. Módulo "Mis Contactos" (\`contactos.html\`)  
\*   \*\*Formulario Seguro Embebido:\*\* Insertar un formulario proveniente de Google Forms mediante código \*iframe\*. Los visitantes dejarán su mensaje y las respuestas se almacenarán externamente.  
\*   \*\*Accesos y Redes:\*\* Acomodar junto al formulario botones de redirección hacia perfiles verificados de LinkedIn, GitHub y el correo electrónico institucional.  
\*   \*\*Interactividad Extra Local:\*\* Añadir una "Insignia de Disponibilidad" (\*status badge\*) que denote el estado para vinculación profesional (T10BLAS.xlsx).  
\*   \*\*Herramientas Móviles:\*\* Integrar una imagen en formato vCard (Código QR) que permita, al ser escaneada, guardar todos los datos en la agenda de un smartphone, un botón ligero JS para copiar el correo al portapapeles y un mapa embebido de Google Maps apuntando al Centro Universitario UAEM Tianguistenco (según T10BLAS.xlsx).

\#\# 5\. Especificaciones No Funcionales (Ingeniería y Calidad Local)  
Para que el entorno local se considere completo "al 100%" debe someterse a las siguientes validaciones:  
\*   \*\*Diseño Web Responsivo:\*\* La maquetación debe adaptarse fluidamente a resoluciones de dispositivos móviles, tabletas y computadoras de escritorio sin truncamiento visual.  
\*   \*\*Accesibilidad (WCAG 2.1 AA):\*\* El código debe validar estrictamente las normas de contraste visual (sobre la paleta azul \#E2EFF5) y poseer atributos semánticos \`alt\` en cada una de las imágenes para garantizar el soporte en lectores de pantalla. También debe poder navegarse en su totalidad utilizando solo la tecla de tabulación del teclado (según T10BLAS.xlsx).  
\*   \*\*Control de Rendimiento:\*\* El peso total por subpágina al abrirse en el navegador local no debe exceder los 2.5 MB en descarga global (según RNF-N09 de T10BLAS.xlsx).  
\*   \*\*Seguridad de Enrutamiento:\*\* Cualquier hipervínculo que se dirija hacia un entorno exterior (Drive, GitHub, LinkedIn) debe incluir los atributos obligatorios \`target='\_blank'\` y \`rel='noopener noreferrer'\` (T10BLAS.xlsx).

\#\# 6\. Cronograma de Ejecución del Entorno Local (Plan de Sprints Ágiles)  
Siguiendo la trazabilidad estructurada en el archivo T10BLAS.xlsx, el desarrollo local se ejecutará paso a paso mediante los siguientes entregables o "sprints":

1\.  \*\*Sprint 0 (Línea Base Estática):\*\* Conformación de los archivos raíz (HTML y CSS) asegurando los requisitos de la primera iteración: menú superior Navbar con cuatro botones principales, página de inicio con los letreros de identidad requeridos, las dos fotografías y enlaces funcionales hacia tres subpáginas vacías con botones funcionales de retorno al inicio. Las subpáginas no deben incluir el menú superior. Carga inferior a 1 segundo.  
2\.  \*\*Sprint 1 (Información Personal Local):\*\* Maquetación y codificación del bloque de presentación, matriz dual de habilidades, botón anclado a Drive para descarga del PDF (CV) y configuración visual del carrusel de fotografías.  
3\.  \*\*Sprint 2 (Catálogo Local de Proyectos):\*\* Codificación de la cuadrícula de tarjetas, inserción de miniaturas, botones redireccionables hacia GitHub y división visual de la subpágina mediante un selector o ancla para Software y Mecatrónica.  
4\.  \*\*Sprint 3 (Medios de Contacto y Formularios):\*\* Incrustación segura del \*iframe\* de Google Forms y mapeo visual de los iconos para las cuentas sociales (LinkedIn, GitHub, correo).  
5\.  \*\*Sprint 4 (Navegación Persistente y Calidad):\*\* Reingeniería del \*Navbar\* (menú) para habilitar su estado persistente en el desarrollo local en todas las vistas, compresión masiva de activos estáticos y auditoría de contraste e inserción de atributos \`alt\`.  
6\.  \*\*Sprint 5 (Credenciales y Trayectoria):\*\* Desarrollo del bloque de insignias locales para idiomas (Inglés Técnico), \*status badge\* de disponibilidad verde y la línea de tiempo cronológica de formación y certificaciones de Drive.  
7\.  \*\*Sprint 6 (Ingeniería de Fichas y Multimedia):\*\* Expansión modular del detalle de proyectos con la incrustación de visores PDF (para diagramas o manuales técnicos) y la inserción de demostraciones operativas mediante el uso de reproductores \*iframes\* de YouTube.  
8\.  \*\*Sprint 7 (Conectividad Local e Interactividad):\*\* Inserción del Código QR (vCard), creación del botón de copia inmediata al portapapeles (JS nativo), mapa interactivo de UAEMex y widget visual dinámico con las estadísticas de GitHub.  
9\.  \*\*Sprint 8 (Optimización y Revisión Final):\*\* Revisión integral final de los archivos estáticos en entorno local para asegurar un peso \< 2.5 MB, la creación del registro (Changelog) público de las versiones iterativas desde T14 a T10BLAS, la inserción de \*Meta-Tags\* y la completitud total "al 100". En este punto el proyecto se encontrará listo para ser navegado completamente local e ir siendo mejorado a nivel de código libremente.