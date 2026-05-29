1. Objetivo del proyecto
El objetivo principal de esta actividad es replicar visualmente y de forma exacta la interfaz de un contador de caracteres en tiempo real. En esta primera etapa, el desarrollo se enfoca puramente en la maquetación semántica y la estilización avanzada con CSS de forma estática (hardcodeada), sin incluir funcionalidad con JavaScript.

2. Tecnologías utilizadas
HTML5: Para la estructura global y el maquetado semántico del sitio.

CSS3: Para la estilización visual (uso de variables :root, Flexbox, Grid, bordes redondeados e interacciones :hover).

Google Fonts: Importación de la familia tipográfica "Inter" para mantener la consistencia del diseño.

3. Cómo se organizó el HTML
La estructura del documento se organizó dividiendo el contenido en bloques lógicos y contenedores limpios:

Se utilizó un contenedor principal para agrupar el logo de la empresa y el título principal "(<h1>)" a la izquierda mediante un subcontenedor, separándolos del botón de configuración de tema situado a la derecha mediante Flexbox.

Cuerpo Principal (.content): Un contenedor centralizado que alberga el título de la sección "(<h2>)" y el resto de los elementos interactivos y visuales.

Área de Texto (<textarea>): Siguiendo las pautas de maquetado semántico, se implementó la etiqueta obligatoria <textarea> con el texto estático, evitando el uso de etiquetas genéricas como <div> o <p>.

Tarjetas de Métricas: Se creó un contenedor padre (.tarjetas-contenedor) que agrupa tres divisiones independientes, cada una estructurada lógicamente con un número principal y su respectivo título descriptivo.

Densidad de Letras: Para las barras horizontales de progreso, se optó por la etiqueta nativa <progress>, agrupándola en filas junto a la letra correspondiente y sus valores numéricos para mantener la estructura semántica limpia.

4. Cómo se resolvió el CSS
La estilización se llevó a cabo utilizando un enfoque modular basado en una maquetación flexible y precisa:

Estructura de Bloques: Se implementó Flexbox tanto en la sección de la cabecera como en la fila de opciones de control (.fila_Text_Bottom) para garantizar una correcta distribución espacial de los elementos a los extremos izquierdo y derecho (justify-content: space-between).

CSS Grid: Se aplicó Grid Layout (grid-template-columns: repeat(3, 1fr)) en el contenedor de las tarjetas para alinear perfectamente las tres métricas y permitir que pasen a una sola columna en dispositivos móviles mediante Media Queries.

Consistencia en Píxeles: Se unificaron los márgenes, rellenos (paddings) y espaciados internos utilizando medidas fijas en píxeles (px) para asegurar la precisión con respecto al diseño guía del proyecto.

Variables CSS Globales: Se utilizó la pseudoclase :root para almacenar toda la paleta de colores exigida, facilitando la reutilización del código y manteniendo la coherencia visual en toda la página.

Integración de Fondos y Contraste: En la versión anterior solo aparecían los colores como fondo y no las imágenes. Para solucionarlo, en las tarjetas de estadísticas se combinaron las propiedades background-color y background-image. Mediante background-position: right top y background-size: auto 100%, se logró arrinconar el patrón decorativo a la derecha, garantizando que el texto oscuro mantuviera un contraste óptimo sobre el color sólido de fondo.

5. Dificultades encontradas
Durante el desarrollo del proyecto se presentaron los siguientes desafíos técnicos y de diseño:

Extracción de imágenes de fondo: Hubo complicaciones al extraer los patrones de las tarjetas utilizando herramientas de IA, ya que la inteligencia artificial alteraba los tonos, el contraste y el brillo originales, requiriendo ajustes manuales posteriores.

Alineación de color (Tarjeta Violeta): La IA generaba errores al intentar extraer el diseño específico con el color violeta (falla replicada en Copilot, Gemini y ChatGPT). Para mantener la alineación visual y la coherencia del diseño, fue necesario adaptar y utilizar un patrón de otro color, modificando su opacidad pero manteniendo la base. A modo de registro, las imágenes originales sin editar se adjuntaron en la raíz del proyecto, fuera de la carpeta de assets, para documentar el estado previo a los ajustes.

Personalización de los Checkboxes: Los inputs nativos de tipo checkbox poseen estilos predeterminados por el navegador que rompían con el diseño oscuro. Se resolvió aplicando appearance: none para ocultar el cuadro por defecto y se construyó un diseño personalizado simulando el tilde ("palomita") mediante el pseudoelemento ::after.

Legibilidad en Tarjetas de Métricas: Inicialmente, las imágenes de fondo de las tarjetas se extendían por todo el contenedor, camuflando el texto. La dificultad se superó asegurando un color de fondo sólido en cada tarjeta y restringiendo el área de la imagen mediante posicionamiento CSS.

CSS Grid: Se aplicó Grid Layout (grid-template-columns: repeat(3, 1fr)) en el contenedor de las tarjetas para alinear perfectamente las tres métricas y permitir que pasen a una sola columna en dispositivos móviles mediante Media Queries.

Consistencia en Píxeles: Se unificaron los márgenes, rellenos y espaciados internos utilizando medidas fijas en píxeles (px) para asegurar la precisión con respecto al diseño guía del proyecto.

Variables CSS Globales: Se utilizó la pseudo-clase :root para almacenar toda la paleta de colores exigida, facilitando la reutilización del código y manteniendo la coherencia visual en toda la página.

Integración de Fondos y Contraste: Para las tarjetas de estadísticas, se combinaron las propiedades background-color y background-image. Mediante background-position: right top y background-size: auto 100%, se logró arrinconar el patrón decorativo a la derecha, garantizando que el texto oscuro mantuviera un contraste óptimo sobre el color sólido de fondo.

Estilización de Barras de Progreso: La etiqueta <progress> requirió el uso de selectores específicos para los motores web (::-webkit-progress-bar, ::-webkit-progress-value) para poder sobrescribir sus colores azules por defecto y aplicar los tonos grises y violetas de la paleta oficial.


