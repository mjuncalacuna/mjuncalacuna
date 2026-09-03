# Carta digital — Os Maristas

Rediseño de la carta de **Os Maristas** (cervecería · tapería, Plaza de la
Verdura, 5), como alternativa a la versión servida hoy en `hosteleria.pide-lo.es`.

Es una única página estática: `index.html`. Sin build, sin dependencias y sin
llamadas a red salvo la hoja de estilos de Google Fonts. Se abre en el navegador
tal cual o se sirve desde cualquier hosting estático.

## Cómo está montada

- **Una sola pantalla.** Las tapas se ven nada más entrar, sin navegar. Debajo
  van postres, vinos, cervezas y refrescos, y vermut y destilados.
- **Barra fija** con el idioma a la izquierda y las cinco secciones a la
  derecha; marca sola la sección que estás leyendo y el salto es suave.
- **Listado en una columna**: foto, nombre, precio, descripción, alérgenos y
  «Ver más».
- **Ficha de detalle** en hoja inferior, con la foto grande, el desglose de
  elaboración o ingredientes y los alérgenos declarados.
- **Alérgenos con icono y nombre** en el propio listado, más leyenda al pie.
- **Español, galego e inglés**, con banderas grandes.

## Datos

Todo el contenido está en el bloque `const D` (productos) y `const MENU`
(estructura de secciones y subsecciones), extraído de la carta del cliente:
169 productos, 86 con foto y 90 con descripción.

Las fotos son las del propio restaurante, recortadas y reconvertidas a WebP
embebido en base64 (comida a 880 px, botellas a 340 px). La página no carga
ninguna imagen externa.

## Qué corrige respecto a la carta actual

- El `0,00 €` fantasma que aparece en once productos.
- Una categoría entera sin nombre (`cat_144`, nueve platos).
- Nombre y precio en la misma ficha, en vez de dos columnas que se desalinean
  cuando el nombre ocupa varias líneas.
- La carta de vinos, reordenada por tipo y luego por zona (Galicia → resto de
  España → mundo) en vez de las cuatro secciones solapadas del original.
- Erratas del origen: «uan textura cremosa», «depositos de inos», «Pnot Nor»,
  «Nieepoort», «Scotch Wisky».

## Pendiente (depende del cliente)

- 70 bebidas sin ficha: los últimos tintos, cervezas, refrescos y destilados
  salen con nombre y precio solamente.
- Las descripciones están en español también en galego e inglés.
- 13 vinos sin foto de botella en el gestor del cliente.
- Destilados: tres columnas de precio sin etiquetar en el origen.
