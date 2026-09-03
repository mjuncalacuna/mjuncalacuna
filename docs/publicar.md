# Publicar y añadir propuestas

Un solo proyecto de Netlify (`manueljuncal`) sirve todas las propuestas. El
directorio `web/` es la raíz del sitio, así que **cada carpeta es una URL**:

```
web/
  index.html            → manueljuncal.netlify.app/
  osmaristas/index.html → manueljuncal.netlify.app/osmaristas
  casa-pepe/index.html  → manueljuncal.netlify.app/casa-pepe
```

El nombre de la carpeta es la URL: en minúsculas, sin acentos y con guiones.

## Añadir un restaurante

1. Crea `web/<slug>/index.html` con la propuesta.
2. Añade su tarjeta en `web/index.html`, o no la añadas si prefieres que esa
   propuesta solo la vea quien tenga el enlace.
3. `git push`. Si el repo está enlazado con Netlify, se publica solo; si no,
   arrastra el contenido de `web/` a la pestaña Deploys del proyecto.

## El documento tiene que estar completo

Las propuestas se generan como fragmento para el Artifact de Claude, que ya
aporta el `<head>`. El fichero que se publica en Netlify **no**, así que
`build_site.py` lo envuelve con:

- `<!doctype html>`, o el navegador entra en quirks mode.
- `<meta name="viewport">`, sin el cual el móvil maqueta a 980 px y encoge
  la página hasta dejarla ilegible.
- `<meta charset>`, `theme-color`, favicon y `robots: noindex`.

El `noindex` es deliberado: mientras es una propuesta no interesa que Google
la indexe bajo tu dominio y le haga sombra al restaurante. Cuando el cliente
la compre y pase a su dominio, se quita.
