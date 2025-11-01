# Proyecto HTML/CSS — Carpeta1

Descripción
- Proyecto pequeño de ejemplo con páginas HTML estáticas y una hoja de estilos CSS.
- Estructura pensada para practicar etiquetas HTML, listas, imágenes, enlaces y selectores CSS.

Contenido del workspace
- [home.html](home.html) — Página principal con ejemplos de párrafos, listas y encabezados.
- [blog2.html](blog2.html) — Página de ejemplo que enlaza a una hoja de estilos (ver nota sobre la ruta).
- [blog.html/home2.html](blog.html/home2.html) — Archivo adicional dentro de la carpeta `blog.html`.
- [blog.html/main.css](blog.html/main.css) — Hoja de estilos CSS con selectores por etiqueta y un id: [`#subtitulo`](blog.html/main.css).
- [carpeta2](carpeta2) — Carpeta vacía/auxiliar (presente en la estructura).

Cómo ver el proyecto
1. Abrir la carpeta `c:\Users\ADMIN\carpeta1` en Visual Studio Code.
2. Abrir cualquiera de los archivos listados arriba desde el explorador de VS Code.
3. Para vista en navegador:
   - Hacer clic derecho sobre el archivo HTML -> "Open with Live Server" (recomendado).
   - O abrir directamente el archivo en el navegador (doble clic sobre `home.html` o `blog2.html`).

Problemas detectados y recomendaciones (rápidas)
- [home.html](home.html)
  - Falta la etiqueta `<body>` antes del contenido HTML. Mover el contenido entre `<body>...</body>`.
  - Las listas están mal anidadas: hay un `<ul>` que contiene un `<ol>` pero el cierre de etiquetas no sigue la jerarquía correcta. Revisar cierre de `</ol>` y `</ul>`.
  - La etiqueta `<img src="carpeta1" ...>` usa `src` incorrecto: debe ser la ruta a un archivo (por ejemplo `img/foto.jpg`).
- [blog2.html](blog2.html)
  - El enlace a la hoja de estilos es `href="main.css"`, pero la CSS real está en `blog.html/main.css`. Actualizar la ruta a `blog.html/main.css` o mover `main.css` al mismo directorio que `blog2.html`.
  - Hay un `article` malformed: aparece ` <article> class= ""` — la sintaxis correcta es `<article class=""> ... </article>`.
- [blog.html/main.css](blog.html/main.css)
  - Contiene el selector `#subtitulo` documentado como id. Asegurarse de aplicarlo en HTML con `<h2 id="subtitulo">...</h2>` si se desea su estilo.

Sugerencias de mejoras
- Normalizar estructura de carpetas:
  - Colocar todos los assets (CSS, imágenes) en carpetas claras: `css/`, `img/`.
  - Ejemplo: mover `blog.html/main.css` a `css/main.css` y actualizar `<link rel="stylesheet" href="css/main.css">`.
- Validar HTML con un validador (W3C) para detectar etiquetas mal cerradas y errores de sintaxis.
- Añadir meta información en cada HTML (title descriptivo, description) y un favicon.
- Usar un pequeño README por página para documentar su propósito si el proyecto crece.

Ejemplos de corrección rápida
- Corregir enlace CSS en `blog2.html`:
```html
<link rel="stylesheet" href="blog.html/main.css">