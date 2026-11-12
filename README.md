# Tostadero Andino — Landing Page Responsive

Landing page de un tostadero de café ficticio de Quito, construida con **HTML semántico, Sass, BEM, Flexbox y CSS Grid** con enfoque *mobile-first*. Sin frameworks ni librerías.

🔗 **Demo en vivo:** https://motitas124.github.io/landing-responsive/

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![Sass](https://img.shields.io/badge/Sass-CC6699?logo=sass&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

| Escritorio | Móvil |
|---|---|
| ![Captura de escritorio](img/captura-escritorio.png) | ![Captura móvil](img/captura-movil.png) |

## Qué incluye

- **Header fijo** con menú hamburguesa animado en móvil (accesible con `aria-expanded`, cierra con <kbd>Esc</kbd>).
- **Hero** con ilustración hecha solo con CSS (taza, vapor animado y etiqueta).
- **Tarjetas de producto** en CSS Grid: 1 columna en móvil, 2 en tablet y 3 en escritorio.
- **Pasos del proceso** en grid de 4 columnas que se adapta a 2 y 1.
- **Formulario de suscripción** con validación en JavaScript y mensajes accesibles (`aria-live`).
- Ilustración de montañas hecha con bordes CSS, sin imágenes.

## Técnicas aplicadas

| Técnica | Dónde |
|---|---|
| **Mobile-first** con mixin `desde($bp)` | Todos los parciales Sass |
| **CSS Grid** | `.cards`, `.steps`, `.stats__list`, `.split`, `.hero__inner` |
| **Flexbox** | `.header__inner`, `.nav__list`, `.card`, `.form__row`, `.schedule__row` |
| **BEM** (bloque__elemento--modificador) | `.card__swatch--dark`, `.button--ghost`, `.nav--open` |
| **Sass**: variables, mixins, anidamiento, parciales | Carpeta `scss/` |
| **Tipografía fluida** con `clamp()` | Títulos del hero y secciones |
| **Accesibilidad** | Enlace "saltar al contenido", `:focus-visible`, `prefers-reduced-motion`, etiquetas ARIA |

## Estructura

```
landing-responsive/
├── index.html
├── css/styles.css          # CSS compilado (lo que usa la página)
├── js/main.js              # Menú móvil, header con sombra, validación del formulario
├── img/                    # Capturas para este README
└── scss/
    ├── styles.scss         # Punto de entrada
    ├── abstracts/          # _variables.scss, _mixins.scss
    ├── base/               # Reset, tipografía, utilidades
    ├── layout/             # _header.scss, _sections.scss
    └── components/         # _button.scss, _card.scss, _form.scss
```

## Cómo ejecutarlo

Abre `index.html` en el navegador, o con un servidor local:

```bash
npx serve .
```

Para editar los estilos y recompilar Sass:

```bash
npx sass --watch scss/styles.scss css/styles.css --no-source-map
```

## Nota

*Tostadero Andino* es una marca ficticia creada para este proyecto; los productos y datos son de ejemplo.

## Autor

**Rendy Silva** — Estudiante de Ingeniería en Software, Universidad de las Américas (UDLA), Quito.
