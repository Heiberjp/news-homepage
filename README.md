# News homepage — Frontend Mentor

Implementación responsive del reto **News homepage** de Frontend Mentor, maquetada principalmente con **CSS Grid**.

- **Autor:** Jhanpool
- **Actividad:** Diseño Front End — Corte 3 (EXIA, Universidad Autónoma del Caribe)
- **Sitio publicado:** _[pega aquí el enlace de GitHub Pages / Netlify]_

## Herramientas
HTML5 semántico · CSS3 (Grid, variables, media queries) · JavaScript básico (menú mobile) · Fuente Inter (Google Fonts) · Chrome DevTools para probar tamaños.

## Estructura
```
news-homepage/
├── index.html
├── README.md
├── css/style.css
└── imagenes/
```

## Decisiones de diseño

**Enfoque Desktop First.** Partí del diseño de 1440px porque es el que trae más información visual (columna "New" al lado, tres tarjetas en fila). Los estilos base son los de escritorio y las media queries `max-width` (1024px y 600px) van al final del CSS y van simplificando el layout hacia tablet y móvil.

**Breakpoints:** desktop (base) · tablet hasta 1024px · mobile hasta 600px. El diseño original solo trae 1440px y 375px; el de tablet lo definí yo.

**Por qué `grid-template-areas`.** El layout general tiene tres zonas (destacado, bloque "New" y tarjetas). Con áreas nombradas se ve el layout "dibujado" en el código y para móvil solo hay que redibujarlo en una sola columna, sin tocar el HTML.

**Por qué `repeat(auto-fit, minmax(...))` en las tarjetas.** Las tres tarjetas se acomodan solas: caben en fila en escritorio y bajan a 2 o 1 columna cuando falta espacio, sin escribir una media query para cada ancho.

**Cómo resolví el menú mobile.** En móvil el `<nav>` se convierte en un panel lateral fijo que entra desde la derecha con `transform: translateX()` y `transition`. Un botón hamburguesa (con `aria-expanded`) alterna una clase en el `body` con unas pocas líneas de JavaScript; esa clase muestra el panel, el fondo oscuro (overlay) y cambia el icono por el de cerrar. También se cierra con la tecla Esc y al tocar el fondo.

**Imágenes optimizadas.** Uso `<picture>` para cargar `image-web-3-mobile.jpg` en pantallas de hasta 600px y la versión de escritorio en el resto.

**Accesibilidad.** Etiquetas semánticas (`header`, `nav`, `main`, `article`, `aside`, `section`, `footer`), textos `alt`, y estados `:hover` y `:focus-visible` en todos los elementos interactivos.

## Reflexión: dificultad principal
_[Completar con tu experiencia: qué fue lo más difícil de la implementación y cómo lo resolviste.]_
