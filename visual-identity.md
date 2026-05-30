# Visual Identity — Generación O2

> Todos los valores de esta página se han extraído **directamente del código fuente**: hojas de estilo del tema (`wp-bootstrap-starter-child/style.css`), declaraciones `@font-face`, `<link>` de Google Fonts y análisis de los píxeles del archivo del logo. No hay estimaciones; lo que no consta en el código se marca como **[por definir]**.

---

## Tipografías (datos reales)

### Tipografía principal — **Gotham (GothamRounded)**

Definida mediante `@font-face` en el child theme y forzada en todo el sitio:

```css
html, body { font-family:'Gotham', sans-serif !important; }
```

Variantes cargadas (archivos en `/public/fonts/gotham/`):

| Variante | Archivo | Peso |
|---|---|---|
| GothamRounded Light | `GothamRoundedLight_21020.ttf` / `.otf` | Light |
| GothamRounded Medium | `GothamRoundedMedium_21022.ttf` / `.otf` | Normal |
| GothamRounded Bold | `GothamRoundedBold_21016.ttf` / `.otf` | Bold |

> Se usa **Gotham Rounded** (versión de extremos redondeados). Es la tipografía de titulares, cuerpo, botones y pestañas.

### Tipografía secundaria — **Montserrat**

Cargada desde Google Fonts en el `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
```

> Nota técnica: la clase `.font-montserrat` está mapeada en el CSS a `'Gotham'`, por lo que en la práctica Gotham predomina. Montserrat queda disponible como tipografía de respaldo / sistema.

### Iconografía
- **Font Awesome 5.1.0** (vía CDN `use.fontawesome.com`) para iconos de interfaz y redes sociales.

### Pila tipográfica de fallback
`'Gotham', sans-serif`

---

## Paleta de colores (datos reales del CSS)

### Naranja — color de acento web (escala completa)

| Token | Hex | Uso en el código |
|---|---|---|
| orange-100 | `#FFB486` | Hover de menú, fondo de carrusel (caption), degradados |
| orange-300 | `#FF9A5D` | Acento intermedio |
| **orange-500 / orange** | `#F37F37` | **Botón secundario, pestañas activas, color naranja principal** |
| orange-700 | `#D85C0F` | Acento oscuro |
| orange-900 | `#A94303` | Fondo de la barra superior del header (`#top-header`) |

### Verde — color primario web (escala completa)

| Token | Hex | Uso en el código |
|---|---|---|
| green-100 | `#B6EC54` | Acento claro |
| green-300 | `#9DDE29` | Acento intermedio |
| **green-500 / green** | `#7EBE0A` | **Botón primario (fondo + borde)** |
| green-700 | `#649B00` | Acento oscuro |
| green-900 | `#4B7500` | Acento más oscuro |

### Grises — fondos

| Token | Hex |
|---|---|
| grey-100 | `#C6C6C6` |
| grey-300 | `#B2B2B2` |
| grey-500 / grey | `#999999` |
| grey-700 | `#787878` |
| grey-900 | `#5A5A5A` |

### Neutros y utilitarios

| Color | Hex | Uso |
|---|---|---|
| Blanco | `#FFFFFF` | Texto sobre fondos de color, fondos generales |
| Texto de menú | `#343435` | Enlaces del menú principal |
| Gris overlay / texto | `#333333` | Overlay de imágenes (opacidad 0.5), degradado de tarjetas |

### El logotipo Go2

El logotipo **Go2** se compone así:

- **"G"** mayúscula en **blanco** (`#FFFFFF`)
- **"o"** minúscula en **rojo granate** (`#8B1A1A`)
- **superíndice "2"** en **blanco** (`#FFFFFF`)
- todo sobre **fondo negro** (`#000000`)

La composición juega con la fórmula química del oxígeno (O₂), con la "o" granate como elemento distintivo.

| Color del logo | Hex | RGB |
|---|---|---|
| Blanco (G y ²) | `#FFFFFF` | rgb(255, 255, 255) |
| **Rojo granate (o)** | `#8B1A1A` | rgb(139, 26, 26) |
| Negro (fondo) | `#000000` | rgb(0, 0, 0) |

> Nota: el verde de los botones de la web (`#7EBE0A`) y la paleta naranja del CSS corresponden a la interfaz del sitio, no al logotipo.

---

## Estilos de interfaz (datos reales)

| Elemento | Especificación CSS |
|---|---|
| Botón primario | Fondo `#7EBE0A`, borde `1px solid #7EBE0A`, texto `#FFFFFF`, **negrita** |
| Botón secundario | Fondo `#F37F37`, texto blanco, negrita |
| Radio de borde de botones | `15px` |
| Radio de borde de imágenes/tarjetas | `15px` (clase `.rounded`) |
| Header superior | Fondo `#A94303`, texto `#FFFFFF` |
| Hover de menú | Color `#FFB486` |
| Altura del logo en header | `75px` |
| Pestañas (tabs) | Texto `#F37F37`; activa: fondo `#F37F37`, texto blanco; fuente Gotham bold |
| Carrusel (caption) | Fondo `#FFB486` con degradado `rgba(255,180,134, …)` |
| Overlay de imágenes de fondo | `#333333` con `opacity: .5` |

---

## Estilo fotográfico

Basado en el uso real de imágenes en la web (tarjetas con `object-fit:cover`, carrusel a media pantalla, overlays oscuros):

- **Personas reales** protagonistas de los proyectos (no stock genérico)
- **Imágenes a sangre** dentro de tarjetas con esquinas redondeadas (15px)
- **Overlay oscuro semitransparente** (`#333333` al 50%) sobre fondos para legibilidad del texto
- **Degradados de marca** (naranja claro `#FFB486`) en los captions del carrusel
- **Diversidad visible** — representación de distintas identidades, géneros y capacidades
- **Tono cálido y esperanzador**, en línea con la paleta naranja-verde

### Estilo a evitar
- Imágenes de pobreza o sufrimiento explícito (narrativa de víctima)
- Stock genérico sin contexto real
- Composiciones sin el tratamiento de overlay/redondeo propio de la web

---

## Notas técnicas

- **CMS:** WordPress 6.9.4
- **Tema:** WP Bootstrap Starter + child theme "WP Bootstrap Starter Child" (autor: Ruben Molina / quickcomputers.net)
- **Framework CSS:** Bootstrap
- **Formularios:** Contact Form 7
- **Logo principal:** `logo_go2.png` (767×477 px, PNG RGBA)
- **Sub-marca podcast:** `Efecto-DAN_Logo.png` (403×403 px) — ver [logo-notes.md](logo-notes.md)
