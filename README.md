Proyecto de Maquetado Web – Character Counter (HTML + CSS)

 1. Objetivo del proyecto
El objetivo principal de esta actividad es replicar visualmente y de forma exacta el diseño de la interfaz de un contador de caracteres en tiempo real. En esta primera etapa, el desarrollo se enfoca puramente en la maquetación semántica y la estilización avanzada con CSS de forma estática (hardcodeada), sin incluir funcionalidad con JavaScript.

 2. Tecnologias utilizadas
* HTML5: Para la estructura global y el maquetado semantico del sitio.
* CSS3: Para la estilización visual (uso de variables `:root`, Flexbox, bordes redondeados, interaciones `:hover`).
* Google Fonts: Importación de la familia tipográfica "Inter" para mantener la consistencia del diseño.

 3. Cómo se organizo el HTML
La estructura del documento se organizó dividiendo el contenido en bloques lógicos y contenedores limpios:
* Cabecera (`.barra`):Se utilizó un contenedor principal para agrupar el logo de la empresa y el título principal (`<h1>`) a la izquierda mediante un sub-contenedor, separándolos del botón de configuración de tema situado a la derecha mediante Flexbox.
* Cuerpo Principal (`.content`): Un contenedor centralizado que albergará el título de la sección (`<h2>`),

*  4. Cómo resolvieron el CSS
La estilización se llevo a cabo utilizando un enfoque modular basado en maquetación flexible:
* Estructura de Bloques: Se implementó Flexbox tanto en la sección de la cabecera (`.barra`) como en la fila de opciones de control (`.controles-fila`) para garantizar una correcta distribución espacial de los elementos a los extremos izquierdo y derecho (`justify-content: space-between`).
* Consistencia en Píxeles: Se unificaron los márgenes, rellenos y espaciados internos utilizando medidas fijas en píxeles (`px`) para asegurar la precisión con respecto al diseño guía del proyecto.
