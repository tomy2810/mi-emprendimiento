# Spec de desarrollo — YIZU

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

## 1. Estructura de archivos

El sitio web de YIZU se organizará mediante una estructura de carpetas simple, ordenada y escalable.

```text

yizu/

│

├── index.html

├── tienda.html

├── producto.html

├── carrito.html

├── blog.html

├── articulo.html

│

├── css/

│   ├── variables.css

│   ├── reset.css

│   ├── styles.css

│   ├── components.css

│   └── responsive.css

│

├── img/

│   ├── logo-yizu.svg

│   ├── hero-yizu.jpg

│   ├── productos/

│   ├── colecciones/

│   └── blog/

│

├── stitch/

│   ├── landing/

│   ├── tienda/

│   ├── producto/

│   ├── carrito/

│   ├── blog/

│   └── articulo/

│

├── docs/

│   ├── 09-spec-diseno.md

│   └── 10-spec-desarrollo.md

│

└── DESIGN.md

```

### Descripción de archivos

| Archivo | Función |
|---|---|
| index.html | Página principal de YIZU |
| tienda.html | Catálogo de productos |
| producto.html | Ficha individual de producto |
| carrito.html | Resumen del carrito |
| blog.html | Listado de artículos |
| articulo.html | Lectura de artículo |
| variables.css | Tokens del design system |
| reset.css | Normalización de estilos |
| styles.css | Estilos generales y layouts |
| components.css | Componentes reutilizables |
| responsive.css | Adaptaciones responsive |
| img/ | Recursos gráficos |
| stitch/ | Referencias exportadas de Stitch |

Esta estructura corresponde a los archivos previstos para la etapa de implementación.

---

## 2. Páginas y navegación

El sitio tendrá seis páginas HTML conectadas mediante una navegación principal.

### Mapa de navegación

```text

LANDING

│

├── TIENDA

│   └── FICHA DE PRODUCTO

│       └── CARRITO

│           └── SEGUIR COMPRANDO → TIENDA

│

├── BLOG

│   └── ARTÍCULO

│       └── VOLVER A BLOG

│

└── CONTACTO

    └── Sección de contacto en la landing

```

### Tabla de navegación

| Desde | Elemento | Lleva a |
|---|---|---|
| Todas | Logo YIZU | index.html |
| Todas | Inicio | index.html |
| Todas | Tienda | tienda.html |
| Todas | Blog | blog.html |
| Todas | Contacto | index.html#contacto |
| Todas | Icono carrito | carrito.html |
| Landing | Explorar colección | tienda.html |
| Landing | Tarjeta producto | producto.html |
| Landing | Blog Universo YIZU | blog.html |
| Tienda | Tarjeta producto | producto.html |
| Producto | Agregar al carrito | carrito.html |
| Carrito | Seguir comprando | tienda.html |
| Blog | Tarjeta artículo | articulo.html |
| Artículo | Volver a blog | blog.html |
| Artículo | Artículo relacionado | articulo.html |

### Navegación principal

El header incluirá:

- Logotipo YIZU.

- Inicio.

- Tienda.

- Contacto.

- Blog.

- Icono de carrito.

En desktop se utilizará navegación horizontal.

En mobile se utilizará un menú hamburguesa, manteniendo visible el logotipo y el carrito.

Los enlaces deben utilizar rutas relativas para facilitar el funcionamiento del sitio.

El enlace Contacto dirigirá a una sección identificada con `id="contacto"` dentro de la landing.

---

## 3. Estructura semántica

Se utilizará HTML5 semántico para organizar correctamente el contenido de las seis páginas.

### Estructura general

```html

<!DOCTYPE html>

<html lang="es">

<head>

  <meta charset="UTF-8">

  <meta name="viewport"

        content="width=device-width, initial-scale=1.0">

  <title>YIZU | Streetwear</title>

  <link rel="stylesheet" href="css/variables.css">

  <link rel="stylesheet" href="css/reset.css">

  <link rel="stylesheet" href="css/styles.css">

  <link rel="stylesheet" href="css/components.css">

  <link rel="stylesheet" href="css/responsive.css">

</head>

<body>

  <header class="site-header">

    <nav class="navbar" aria-label="Navegación principal">

      <!-- Logo, menú y carrito -->

    </nav>

  </header>

  <main>

    <!-- Contenido específico de cada página -->

  </main>

  <footer class="site-footer">

    <!-- Enlaces, marca y contacto -->

  </footer>

</body>

</html>

```

### Landing — index.html

- `header`: logotipo y navegación.

- `nav`: enlaces principales.

- `main`: contenido central.

- `section.hero`: imagen principal y mensaje.

- `section.collection`: colección destacada.

- `article.product-card`: cada producto.

- `section.blog-preview`: acceso al blog.

- `section#contacto`: información de contacto.

- `footer`: enlaces e información corporativa.

### Tienda — tienda.html

- `header`: navegación principal.

- `main`: catálogo.

- `section.shop-header`: título y ordenamiento.

- `aside.filters`: categorías, tallas y precios.

- `section.product-grid`: cuadrícula de productos.

- `article.product-card`: cada prenda.

- `footer`: navegación secundaria.

### Ficha de producto — producto.html

- `header`: navegación.

- `main`: contenido del producto.

- `section.product-gallery`: imágenes y miniaturas.

- `section.product-info`: nombre, precio y descripción.

- `fieldset`: selección de talla y color.

- `button`: agregar al carrito.

- `section.product-details`: descripción, envíos y devoluciones.

- `footer`: información general.

### Carrito — carrito.html

- `header`: navegación.

- `main`: contenido del carrito.

- `section.cart-items`: productos seleccionados.

- `article.cart-item`: información de cada producto.

- `section.cart-summary`: subtotal, envío y total.

- `footer`: información y enlaces.

### Blog — blog.html

- `header`: navegación.

- `main`: contenido editorial.

- `section.blog-intro`: presentación.

- `nav.blog-categories`: filtros editoriales.

- `section.blog-grid`: artículos.

- `article.blog-card`: cada publicación.

- `footer`: enlaces generales.

### Artículo — articulo.html

- `header`: navegación.

- `main`: contenido principal.

- `article.blog-article`: publicación completa.

- `header.article-header`: título y categoría.

- `figure`: imagen editorial.

- `section.article-content`: texto del artículo.

- `section.related-articles`: artículos relacionados.

- `footer`: navegación secundaria.

### Consideraciones semánticas

- Cada página tendrá un solo `h1`.

- Los subtítulos seguirán una jerarquía lógica.

- Los enlaces utilizarán elementos `a`.

- Las acciones utilizarán elementos `button`.

- Las imágenes informativas tendrán atributos `alt`.

- Los formularios utilizarán `label` y controles accesibles.

- No se utilizarán elementos HTML únicamente por su apariencia visual.

---

## 4. Organización del CSS

Los estilos se organizarán mediante archivos independientes para facilitar su mantenimiento.

### Variables CSS

Los tokens visuales se centralizarán en `variables.css`, tomando como referencia el archivo `DESIGN.md`.

```css

:root {

  /* Colores YIZU */

  --color-primary: #121212;

  --color-primary-hover: #2D2F2C;

  --color-secondary: #989A97;

  --color-tertiary: #50584B;

  --color-background: #F4F4F2;

  --color-surface: #FFFFFF;

  --color-text: #2D2F2C;

  --color-text-inverse: #FFFFFF;

  --color-success: #28613B;

  --color-error: #B3261E;

  /* Tipografías */

  --font-heading: "Bebas Neue", sans-serif;

  --font-accent: "Press Start 2P", monospace;

  --font-body: Arial, sans-serif;

  /* Tamaños desktop */

  --font-h1: 64px;

  --font-h2: 48px;

  --font-h3: 36px;

  --font-body-size: 14px;

  /* Espaciados */

  --space-1: 4px;

  --space-2: 8px;

  --space-3: 12px;

  --space-4: 16px;

  --space-5: 24px;

  --space-6: 32px;

  --space-7: 48px;

  --space-8: 64px;

  /* Bordes */

  --radius-image: 0px;

  --radius-small: 4px;

  --radius-card: 8px;

  --radius-container: 12px;

  --radius-button: 9999px;

  /* Layout */

  --container-max: 1200px;

  --container-padding: 24px;

  /* Transiciones */

  --transition-default: 0.2s ease;

}

```

Los valores definitivos deberán mantenerse sincronizados con `DESIGN.md`. Si existe alguna diferencia, prevalecerán los tokens documentados en ese archivo.

### Organización de estilos

**reset.css**

Normalización de márgenes, padding y comportamiento de cajas.

**styles.css**

Estilos generales del sitio, estructura de páginas, contenedores y distribución de elementos.

**components.css**

Componentes reutilizables como:

- `.navbar`

- `.button-primary`

- `.product-card`

- `.product-grid`

- `.product-gallery`

- `.filter-sidebar`

- `.size-selector`

- `.color-selector`

- `.cart-item`

- `.cart-summary`

- `.blog-card`

- `.site-footer`

**responsive.css**

Media queries para adaptar el sitio a diferentes dispositivos.

### Ejemplo de botón principal

```css

.button-primary {

  display: inline-flex;

  align-items: center;

  justify-content: center;

  padding: 14px 28px;

  background: var(--color-primary);

  color: var(--color-text-inverse);

  border: none;

  border-radius: var(--radius-button);

  font-family: var(--font-heading);

  cursor: pointer;

  transition: background var(--transition-default);

}

.button-primary:hover {

  background: var(--color-primary-hover);

}

.button-primary:focus-visible {

  outline: 2px solid var(--color-tertiary);

  outline-offset: 3px;

}

.button-primary:disabled {

  opacity: 0.5;

  cursor: not-allowed;

}

```

### Breakpoints responsive

Se utilizarán tres rangos principales:

| Dispositivo | Ancho | Distribución |
|---|---|---|
| Mobile | Hasta 767px | Una columna principal |
| Tablet | 768px a 1023px | Distribución adaptable |
| Desktop | Desde 1024px | Layout completo |

### Ejemplo de media queries

```css

/* Tablet */

@media (min-width: 768px) and (max-width: 1023px) {

  .product-grid {

    grid-template-columns: repeat(2, minmax(0, 1fr));

  }

  .container {

    padding-inline: 24px;

  }

}

/* Mobile */

@media (max-width: 767px) {

  :root {

    --font-h1: 40px;

    --font-h2: 32px;

    --font-h3: 26px;

    --font-body-size: 12px;

    --container-padding: 16px;

  }

  .desktop-nav {

    display: none;

  }

  .mobile-nav {

    display: flex;

  }

  .product-grid {

    grid-template-columns: 1fr;

  }

  .product-layout {

    display: flex;

    flex-direction: column;

  }

  .cart-layout {

    display: flex;

    flex-direction: column;

  }

  .blog-grid {

    grid-template-columns: 1fr;

  }

  .button-primary {

    width: 100%;

  }

}

```

### Criterios visuales

- Imágenes de productos rectangulares.

- Botones principales redondeados.

- Tarjetas con radio de 8px.

- Jerarquía tipográfica marcada.

- Uso consistente de colores.

- Espaciados uniformes.

- Contraste adecuado entre texto y fondo.

- Efectos visuales discretos.

- Prioridad visual para fotografías de prendas.

---

## 5. Criterios de aceptación

Los siguientes criterios permitirán verificar que el sitio cumple con los requisitos establecidos.

Las casillas se mantendrán sin marcar hasta la implementación y validación del sitio.

### Navegación

- [ ] Las seis páginas HTML existen y cargan correctamente.

- [ ] El logotipo YIZU dirige a la landing.

- [ ] Los enlaces Inicio, Tienda y Blog funcionan.

- [ ] El enlace Contacto dirige a la sección correspondiente.

- [ ] Las tarjetas de productos enlazan a sus fichas.

- [ ] El carrito es accesible desde la navegación.

- [ ] El enlace Volver a blog funciona.

- [ ] No existen enlaces internos rotos.

### Funcionalidades

- [ ] La tienda presenta productos con imágenes, nombres y precios.

- [ ] Las categorías y tallas se muestran correctamente.

- [ ] Los controles de filtros tienen estados visuales definidos.

- [ ] La ficha de producto presenta galería de imágenes.

- [ ] Las opciones de talla y color son accesibles.

- [ ] El botón Agregar al carrito tiene estados visuales.

- [ ] El carrito muestra productos, cantidades y precios.

- [ ] El resumen de compra presenta subtotal, envío y total.

- [ ] El blog muestra las ocho tarjetas editoriales previstas.

- [ ] Cada artículo incluye título, imagen, contenido y relacionados.

**Nota:** los filtros dinámicos, favoritos, persistencia del carrito, actualización automática de totales y procesamiento de compras requerirán JavaScript o servicios adicionales. No se considerarán funcionalidades operativas mientras solo exista HTML y CSS.

### Diseño

- [ ] Los colores coinciden con DESIGN.md.

- [ ] Las tipografías corresponden al sistema visual.

- [ ] Los títulos mantienen jerarquía consistente.

- [ ] Los botones utilizan estilos reutilizables.

- [ ] Las tarjetas mantienen bordes y espaciados definidos.

- [ ] Las imágenes de producto son protagonistas.

- [ ] Las seis páginas comparten una identidad visual coherente.

- [ ] Los diseños respetan los wireframes de Whimsical.

- [ ] Se consideran los prototipos exportados de Stitch.

### Responsive

- [ ] El sitio se adapta a desktop de 1440px.

- [ ] El sitio se adapta a tablet de 768px.

- [ ] El sitio se adapta a mobile de 375px.

- [ ] El menú principal se adapta a pantallas pequeñas.

- [ ] La tienda muestra un producto por fila en mobile.

- [ ] La ficha de producto organiza su contenido verticalmente.

- [ ] El carrito presenta un resumen legible en mobile.

- [ ] El blog organiza sus tarjetas en una columna en mobile.

- [ ] Los botones mantienen áreas táctiles accesibles.

- [ ] No existe desplazamiento horizontal no deseado.

### Accesibilidad y publicación

- [ ] Todas las imágenes informativas incluyen atributo alt.

- [ ] Los enlaces tienen textos descriptivos.

- [ ] Los botones son identificables y accesibles.

- [ ] Los controles tienen etiquetas asociadas.

- [ ] La navegación por teclado es posible.

- [ ] Los elementos interactivos muestran foco visible.

- [ ] Se utiliza HTML semántico correctamente.

- [ ] Cada página incluye título y metadatos básicos.

- [ ] Los archivos CSS cargan correctamente.

- [ ] Las rutas de imágenes funcionan.

- [ ] El sitio puede publicarse como proyecto estático.

- [ ] Se verificó su funcionamiento en navegadores modernos.
