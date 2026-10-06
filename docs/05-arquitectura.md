# Arquitectura de la información — YIZU

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

<!-- Incluye landing, blog, tienda y las páginas obligatorias:
contacto, preguntas frecuentes, términos, privacidad y 404. -->

```text
Inicio (landing)
├── Tienda
│   ├── Pantalones (Wide Leg / Cargo)
│   ├── Poleras & Hoodies Oversize
│   └── Accesorios
├── Blog
│   ├── Tendencias & Estilo Streetwear
│   ├── Guías de Tallas y Calce
│   └── Cuidado de Prendas & Calidad
├── Nosotros
├── Contacto
├── Preguntas Frecuentes (FAQ)
├── Términos y Condiciones
├── Política de Privacidad
└── 404 (Página no encontrada)
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

```text
Instagram / Feed -> Landing Page -> [Ver catálogo en Tienda] -> Seleccionar producto (ej. Pantalón Wide Leg) -> Ficha de producto -> [Seleccionar Talla y Color] -> [Agregar al carrito] -> Vista Carrito -> [Proceder al Pago] -> Formulario de Envío -> Checkout / Pasarela de Pago -> Confirmación de Compra
```

### Flujo 2: contenido

```text
Buscador / Redes Sociales -> Artículo de Blog ("Cómo combinar pantalones muy anchos con zapatillas") -> Lectura del contenido -> [Clic en producto recomendado en la nota] -> Ficha de producto -> [Agregar al carrito] / [Ir a Contacto por consultas de calce]
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

| Categoría | Productos |
|---|---|
| Pantalones Anchos & Streetwear | Pantalón Wide Leg Denim, Cargo Oversize Canvas, Pantalón Parachute |
| Tops & Poleras | Polera Oversize Heavy Cotton, Hoodie Boxy Fit, Polera Graphic Street |
| Accesorios & Complementos | Gorros Beanie, Bananos Streetwear, Calcetines Urbanos |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
|---|---|---|---|
| Guías de Estilo & Outfits | Cómo combinar pantalones anchos con distintas zapatillas urbanas | Quiere saber cómo armar un look equilibrado y con estilo usando corte wide leg. | Pantalón Wide Leg Denim |
| Calce y Tallas | Encuentra tu talla ideal: Guía de medidas para cortes Oversize y Wide Fit | Miedo a que la prenda no le quede bien o el tiro sea incómodo al comprar online. | Pantalón Cargo Oversize Canvas |
| Cuidado de Ropa | Cómo lavar y mantener tus prendas de algodón denso para que duren años | Desea conservar la calidad, color y textura de su ropa urbana favorita. | Polera Oversize Heavy Cotton |
