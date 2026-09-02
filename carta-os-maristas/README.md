# Carta digital — Os Maristas

Rediseño de la carta de **Os Maristas** (cervecería · tapería, Galicia), como
alternativa a la versión servida hoy en `hosteleria.pide-lo.es`.

Es una única página estática: `index.html`. No tiene build, ni dependencias, ni
llamadas a red salvo la hoja de estilos de Google Fonts. Se abre en el navegador
tal cual o se sirve desde cualquier hosting estático.

## Qué corrige respecto a la carta actual

- Nombre y precio viven en la misma ficha, en vez de en dos columnas que se
  desalinean cuando el nombre ocupa varias líneas.
- Desaparece el `0,00 €` que se colaba en el detalle del puerro.
- Se arregla el texto de la ficha de quesos, que se partía a una palabra por línea.
- Buscador por plato e ingrediente.
- Filtros: Del mar · De la tierra · Vegetariano · Vegano.
- Dos vistas: fichas con imagen y lista compacta.
- Alérgenos con icono **y** nombre, más leyenda desplegable.
- Español, galego e inglés de verdad, no sólo banderas.
- Modo claro y oscuro, siguiendo la preferencia del sistema.

## Imágenes

La página no carga imágenes externas: todo va embebido en el HTML.

- **Fotos reales** (tabla de quesos y tostas de anchoa): recuperadas de la carta
  actual del restaurante, incrustadas como WebP en base64.
- **Resto de platos**: ilustración generada en Canvas a partir de una
  especificación por plato (`art`), y etiquetada como «Ilustración» en la ficha
  para no dar a entender que es una foto del plato que se sirve.
- El botón **«Probar con vuestras fotos»** del pie permite subir fotos y verlas
  en su sitio. Se guardan en `localStorage`, sólo en ese dispositivo: sirve para
  validar el diseño, no para publicar.

Para fijar una foto definitiva basta con añadir su data URI a `PHOTOS` y apuntar
el plato con `photo: "<clave>"`.

## Datos de la carta

Transcritos del menú publicado por el restaurante. No hay descripciones
inventadas: los platos de los que sólo se conoce nombre y precio se muestran así,
y sus alérgenos aparecen como «por confirmar» en lugar de deducirlos.

Pendiente de recibir del restaurante:

- Fotos de los platos.
- Las secciones que faltan: raciones, bebidas, vinos, postres.
- Descripción y alérgenos de las 15 tapas que hoy sólo tienen nombre y precio.
- Nombre completo y precio de los canelones de rabo de vaca.

Dos cosas a verificar en el original: el precio del Zaalouk (15,00 €, fuera de
rango respecto al resto de tapas) y un hueco en blanco tras los mejillones, que
parece un plato sin nombre.
