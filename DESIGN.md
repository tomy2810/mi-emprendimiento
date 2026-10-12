---
version: alpha
name: YIZU
description: "Sistema de diseño de YIZU, marca de ropa urbana que combina minimalismo, estética agreste y estilo streetwear contemporáneo."
# Guía: evaluacion/guias/fase-2-specs/06-spec-de-diseno.md
# Reemplaza TODOS los valores de ejemplo por los de tu paleta y tipografía
# (docs/08-color-tipografia.md). Los HEX van siempre entre comillas.
# Valida con: npx @google/design.md lint DESIGN.md
colors:

  primary: "#121212"

  primary-hover: "#2D2F2C"

  on-primary: "#FFFFFF"

  secondary: "#989A97"

  on-secondary: "#121212"

  tertiary: "#50584B"

  on-tertiary: "#FFFFFF"

  neutral: "#F4F4F2"

  surface: "#FFFFFF"

  on-surface: "#121212"

  on-surface-variant: "#2D2F2C"

  disabled: "#D6D6D6"

  on-disabled: "#4A4A4A"

  error: "#B3261E"

  success: "#28613B"

typography:

  headline-display:

    fontFamily: "Bebas Neue"

    fontSize: 64px

    fontWeight: 400

    lineHeight: 1.1

  headline-lg:

    fontFamily: "Bebas Neue"

    fontSize: 48px

    fontWeight: 400

    lineHeight: 1.2

  headline-md:

    fontFamily: "Bebas Neue"

    fontSize: 36px

    fontWeight: 400

    lineHeight: 1.25

  body-md:

    fontFamily: "Arial"

    fontSize: 14px

    fontWeight: 400

    lineHeight: 1.6

  label-md:

    fontFamily: "Press Start 2P"

    fontSize: 12px

    fontWeight: 400

    lineHeight: 1.5

rounded:

  none: 0px

  sm: 4px

  md: 8px

  lg: 12px

  full: 9999px

spacing:

  xs: 4px

  sm: 8px

  md: 16px

  lg: 24px

  xl: 32px

  2xl: 48px

  3xl: 64px

components:

  button-primary:

    backgroundColor: "{colors.primary}"

    textColor: "{colors.on-primary}"

    typography: "{typography.label-md}"

    rounded: "{rounded.full}"

    padding: 12px 24px

  button-primary-hover:

    backgroundColor: "{colors.primary-hover}"

    textColor: "{colors.on-primary}"

  button-primary-active:

    backgroundColor: "{colors.tertiary}"

    textColor: "{colors.on-tertiary}"

  button-primary-disabled:

    backgroundColor: "{colors.disabled}"

    textColor: "{colors.on-disabled}"

  button-secondary:

    backgroundColor: "{colors.surface}"

    textColor: "{colors.primary}"

    typography: "{typography.label-md}"

    rounded: "{rounded.full}"

    padding: 12px 24px

  button-secondary-hover:

    backgroundColor: "{colors.neutral}"

    textColor: "{colors.primary}"

  card-product:

    backgroundColor: "{colors.surface}"

    textColor: "{colors.on-surface}"

    rounded: "{rounded.md}"

    padding: "{spacing.md}"

  card-product-hover:

    backgroundColor: "{colors.neutral}"

    textColor: "{colors.on-surface}"

  tag-offer:

    backgroundColor: "{colors.tertiary}"

    textColor: "{colors.on-tertiary}"

    rounded: "{rounded.full}"

    padding: 4px 8px

  input-field:

    backgroundColor: "{colors.surface}"

    textColor: "{colors.on-surface}"

    rounded: "{rounded.md}"

    padding: 12px 14px

  input-field-focus:

    backgroundColor: "{colors.surface}"

    textColor: "{colors.primary}"

  message-error:

    backgroundColor: "{colors.surface}"

    textColor: "{colors.error}"

  message-success:

    backgroundColor: "{colors.surface}"

    textColor: "{colors.success}"

  page:

    backgroundColor: "{colors.neutral}"

    textColor: "{colors.on-surface}"

  text-secondary:

    backgroundColor: "{colors.neutral}"

    textColor: "{colors.on-surface-variant}"

---

# YIZU — Design System

## Overview

YIZU es una marca de ropa urbana inspirada en el streetwear contemporáneo, el minimalismo y la estética agreste.

Su identidad visual combina prendas de estilo oversize, elementos gráficos experimentales y una comunicación directa orientada a un público joven interesado en la moda urbana.

La interfaz digital debe transmitir modernidad, autenticidad, fuerza visual y simplicidad.

Las palabras clave de la identidad son:

- Urbano

- Minimalista

- Agreste

- Contemporáneo

- Experimental

El diseño debe facilitar la exploración de colecciones, la selección de productos y el proceso de compra.

## Colors

La paleta de YIZU utiliza tonos neutros y oscuros, complementados con un verde agreste que refuerza su personalidad visual.

| Token | HEX | Aplicación |
|---|---|---|
|Primary| #121212 | Encabezados, botones principales, navegación y elementos destacados. |
| Primary hover | #2D2F2C | Estado hover de botones principales. |
| On primary | #FFFFFF | Textos sobre fondos negros. |
| Secondary | #989A97 | Elementos gráficos, detalles y superficies secundarias. |
| On secondary | #121212 | Textos sobre superficies gris metálico. |
| Tertiary | #50584B | Etiquetas, acentos y elementos de identidad. |
| On tertiary | #FFFFFF | Textos sobre verde agreste. |
| Neutral | #F4F4F2 | Fondo principal de la página. |
| Surface | #FFFFFF | Tarjetas, formularios y superficies. |
| On surface | #121212 | Texto principal. |
| On surface variant | #2D2F2C | Descripciones y textos secundarios. |
| Disabled | #D6D6D6 | Elementos deshabilitados. |
| On disabled | #4A4A4A | Texto de elementos deshabilitados. |
| Error | #B3261E | Errores y validaciones. |
| Success | #28613B | Confirmaciones y mensajes positivos. |

### Reglas de aplicación

- El negro carbón es el color principal de la interfaz.

- El fondo Lighthouse mantiene una apariencia limpia.

- El verde agreste se utiliza en detalles de identidad y etiquetas.

- El gris metálico se reserva principalmente para superficies y elementos decorativos.

- El blanco proporciona contraste en botones oscuros.

- Los colores de error y éxito se utilizan únicamente para comunicar estados.

### Accesibilidad

Los textos principales deben mantener un contraste mínimo de 4.5:1 según WCAG AA.

Los textos grandes deben mantener un contraste mínimo de 3:1.

No utilizar gris metálico como texto pequeño sobre fondos claros cuando no alcance el contraste necesario.

## Typography

YIZU utiliza dos tipografías principales seleccionadas desde Google Fonts.

### Bebas Neue

Tipografía condensada de estilo urbano y alto impacto visual.

Se utiliza en:

- Títulos principales.

- Encabezados.

- Nombres de colecciones.

- Campañas y promociones.

- Títulos de productos destacados.

### Press Start 2P

Tipografía pixelada de estética retro y digital.

Se utiliza en:

- Frases destacadas.

- Etiquetas.

- Elementos gráficos.

- Botones de carácter experimental.

- Mensajes breves de identidad.

### Tipografía complementaria

Arial se utiliza como fuente de apoyo para párrafos, descripciones extensas, formularios y textos informativos.

Esto permite conservar la legibilidad sin perder la identidad visual de YIZU.

### Escala tipográfica

| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| H1 | 64px | 40px | 400 |
| H2 | 48px | 32px | 400 |
| H3 | 36px | 26px | 400 |
| Párrafo | 14px | 12px | 400 |
| Botón | 12px | 10px | 400 |

Los tamaños corresponden a la escala definida para el proyecto.

En pantallas pequeñas se prioriza la legibilidad y se evita utilizar Press Start 2P en textos extensos.

## Layout

La interfaz utiliza una estructura de retícula flexible y responsive.

### Desktop

- Ancho de referencia: 1440px.

- Ancho máximo de contenido: 1200px.

- Márgenes laterales: 64px.

- Catálogo de productos: 4 columnas.

- Navegación horizontal completa.

- Filtros visibles en barra lateral.

- Imágenes de producto de gran tamaño.

### Tablet

- Ancho: 768px a 1023px.

- Márgenes laterales: 32px.

- Catálogo de productos: 2 columnas.

- Navegación simplificada.

- Filtros mediante panel desplegable.

- Espaciados adaptados al dispositivo.

### Mobile

- Ancho: hasta 767px.

- Márgenes laterales: 16px.

- Catálogo de productos: 2 columnas.

- Menú de navegación desplegable.

- Filtros mediante botón.

- Botones principales de ancho completo cuando sea necesario.

- Imágenes adaptables al ancho disponible.

### Espaciados

| Token | Valor | Uso |
|---|---|---|
| xs | 4px | Separaciones mínimas. |
| sm | 8px | Etiquetas e íconos. |
| md | 16px | Tarjetas y formularios. |
| lg | 24px | Separación entre componentes. |
| xl | 32px | Bloques de contenido. |
| 2xl | 48px | Secciones principales. |
| 3xl | 64px | Separaciones amplias. |

## Elevation & Depth

La interfaz utiliza una jerarquía visual limpia, evitando efectos tridimensionales excesivos.

### Nivel base

Fondos claros sin sombras.

Aplicación: estructura general de las páginas.

### Nivel intermedio

Tarjetas de productos con bordes sutiles.

Aplicación: catálogo, artículos y productos relacionados.

### Nivel destacado

Sombras suaves en menús desplegables y elementos flotantes.

Aplicación: navegación, filtros y mensajes temporales.

### Reglas

- Priorizar contraste y espaciado sobre sombras.

- Evitar degradados innecesarios.

- Mantener una estética minimalista.

- Utilizar bordes discretos para separar elementos.

- Reservar los efectos de profundidad para elementos interactivos.

## Shapes

Las formas deben mantener una apariencia geométrica, simple y contemporánea.

| Elemento | Radio |
|---|---|
| Imágenes de producto | 0px |
| Etiquetas pequeñas | 4px |
| Tarjetas | 8px |
| Campos de formulario | 8px |
| Contenedores destacados | 12px |
| Botones principales | 9999px |

Los botones redondeados contrastan con las imágenes rectangulares de las prendas.

Las formas no deben competir visualmente con los productos.

## Components

### button-primary

Botón principal de YIZU.

Contenido:

- Texto de acción.

- Fondo negro carbón.

- Texto blanco.

- Bordes redondeados.

Aplicación:

- Ver colección.

- Agregar al carrito.

- Ir a pagar.

Estados:

- Normal: negro carbón.

- Hover: gris antracita.

- Active: verde agreste.

- Disabled: gris claro.

Reglas:

- Debe tener una etiqueta clara.

- Debe mantener contraste suficiente.

- No utilizar más de un botón principal dominante por bloque de contenido.

### button-secondary

Botón utilizado para acciones complementarias.

Aplicación:

- Seguir comprando.

- Volver al blog.

- Ver más productos.

Estados:

- Normal: fondo blanco y texto negro.

- Hover: fondo Lighthouse.

- Active: fondo gris claro.

- Disabled: fondo gris claro y texto atenuado.

### card-product

Tarjeta utilizada en el catálogo de YIZU.

Contenido:

- Imagen de la prenda.

- Nombre del producto.

- Precio.

- Etiqueta de oferta cuando corresponda.

- Acceso a la ficha del producto.

Reglas:

- La imagen debe ser el elemento dominante.

- El nombre ocupa máximo 2 líneas.

- El precio siempre debe ser visible.

- Todas las tarjetas mantienen proporciones consistentes.

- No incluir información innecesaria.

Estados:

- Normal: fondo blanco.

- Hover: fondo Lighthouse.

- Active: producto seleccionado.

### tag-offer

Etiqueta para promociones y productos destacados.

Contenido:

- Texto breve.

- Fondo verde agreste.

- Texto blanco.

Ejemplos:

- NUEVO

- DESTACADO

- EDICIÓN LIMITADA

Reglas:

- Utilizar mensajes breves.

- Mantener una ubicación consistente.

- Evitar múltiples etiquetas sobre una misma imagen.

### input-field

Campo de entrada para formularios.

Aplicación:

- Correo electrónico.

- Contraseña.

- Dirección de envío.

- Datos de contacto.

Estados:

- Normal: fondo blanco.

- Focus: borde negro carbón.

- Error: borde rojo oscuro.

- Disabled: fondo gris claro.

Reglas:

- Cada campo debe tener una etiqueta visible.

- Los errores deben explicarse con texto.

- No depender únicamente del color para indicar errores.

### message-error

Componente para comunicar errores.

Aplicación:

- Campos obligatorios incompletos.

- Datos incorrectos.

- Problemas durante la compra.

Reglas:

- Utilizar rojo oscuro.

- Explicar claramente el problema.

- Indicar cómo corregirlo.

### message-success

Componente para confirmaciones positivas.

Aplicación:

- Producto agregado al carrito.

- Formulario enviado.

- Compra confirmada.

Reglas:

- Utilizar verde oscuro.

- Presentar mensajes breves y claros.

- Mantener consistencia visual.

### page

Contenedor general de las páginas.

Contenido:

- Header.

- Navegación.

- Contenido principal.

- Footer.

Reglas:

- Fondo Lighthouse.

- Texto negro carbón.

- Estructura responsive.

- Márgenes consistentes.

## Do's and Don'ts

### Do's

- Utilizar la paleta oficial de YIZU.

- Mantener una estética urbana y minimalista.

- Priorizar fotografías de las prendas.

- Aplicar Bebas Neue en encabezados.

- Utilizar Press Start 2P en textos breves.

- Mantener precios visibles.

- Respetar la jerarquía tipográfica.

- Adaptar la interfaz a mobile, tablet y desktop.

- Mantener botones reconocibles.

- Utilizar espacios en blanco para mejorar la lectura.

### Don'ts

- No utilizar colores ajenos a la identidad.

- No saturar las pantallas con elementos gráficos.

- No utilizar Press Start 2P en párrafos extensos.

- No ocultar los precios de los productos.

- No utilizar imágenes deformadas.

- No abusar de sombras y degradados.

- No utilizar demasiados botones principales.

- No reducir excesivamente el tamaño de los textos.

- No utilizar gris metálico en textos pequeños sobre fondos claros sin contraste suficiente.

- No modificar arbitrariamente los colores oficiales.

## Aplicación en pantallas YIZU

### Landing Page

Presenta la identidad de YIZU, su colección principal y productos destacados.

Componentes:

- Header.

- Navegación.

- Imagen principal.

- Título destacado.

- button-primary.

- card-product.

- Footer.

Acción principal: Ver colección.

### Tienda

Permite explorar el catálogo de productos.

Componentes:

- Header.

- Filtros por categoría.

- Filtros por talla.

- Filtro de precio.

- card-product.

- Footer.

Acción principal: Ver producto.

### Ficha de producto

Presenta los detalles de una prenda.

Componentes:

- Galería de imágenes.

- Nombre del producto.

- Precio.

- Selector de talla.

- Selector de color.

- button-primary.

- Información de envío.

- Descripción.

- Footer.

Acción principal: Agregar al carrito.

### Carrito

Muestra los productos seleccionados.

Componentes:

- Lista de productos.

- Imagen de cada prenda.

- Nombre.

- Talla y color.

- Cantidad.

- Precio.

- Resumen de compra.

- button-primary.

- button-secondary.

Acciones: Ir a pagar y seguir comprando.

### Blog

Presenta publicaciones relacionadas con la cultura urbana y la identidad de YIZU.

Componentes:

- Header.

- Título.

- Tarjetas de artículos.

- Imágenes.

- Categorías.

- Footer.

Acción principal: Leer artículo.

### Artículo

Permite leer contenido editorial de la marca.

Componentes:

- Header.

- Imagen principal.

- Título del artículo.

- Categoría.

- Contenido.

- Artículos relacionados.

- Footer.

Acción principal: Volver al blog.

## Justificación del sistema

El sistema de diseño de YIZU busca construir una experiencia digital coherente con su identidad de ropa urbana.

El negro carbón transmite fuerza y modernidad, mientras que el gris metálico y el fondo Lighthouse generan equilibrio visual.

El verde agreste incorpora un elemento distintivo que refuerza la personalidad de la marca.

Bebas Neue aporta impacto a los títulos, mientras que Press Start 2P incorpora un lenguaje gráfico experimental y digital.

La combinación de estos elementos permite desarrollar una interfaz reconocible, funcional y adaptable a diferentes dispositivos.

El resultado es un sistema visual orientado a destacar los productos, facilitar la navegación y mantener una identidad consistente en todas las pantallas de YIZU.
