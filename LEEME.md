# Gráficalo · versión 0.7

Gráficalo vive ahora en **https://marcsgc.github.io/graficalo/**, publicado desde el repositorio `graficalo`.

## Cómo actualizar la web

1. En el repositorio `graficalo`, pulsa **Add file → Upload files**.
2. Arrastra **todo el contenido** de esta carpeta, incluidas las carpetas `lang`, `lib`, `ocr` e `icons`.
3. Pulsa **Commit changes** y espera un par de minutos.

Este repositorio no necesita `.well-known` ni `.nojekyll`: esos archivos están en el repositorio `marcsgc.github.io` (la raíz del dominio), porque Android los busca allí.

## Numeración de versiones

Cada vez que publiques cambios, sube el número en dos sitios:
- `app.js` → `APP_VERSION` (lo que se ve en Menú → Acerca de), ahora `"0.7"`.
- `sw.js` → `VERSION`, ahora `"graficalo-v0.7"`. Debe empezar siempre por `graficalo-`: el service worker solo borra las cachés con ese prefijo.

Si generas un `.aab` nuevo en PWABuilder, la dirección es `https://marcsgc.github.io/graficalo/`, usa el mismo nombre de versión y sube siempre el version code.

## Novedades que ve el usuario

El texto del aviso «Novedades» está en `extras.js`, en `WHATS_NEW`. Para la próxima versión añade una entrada nueva con su número (por ejemplo `"0.8": [...]`).

## Traducciones

Cada idioma está en `lang/xx.js`. Para corregir una frase, búscala en ese archivo y cambia el texto que hay después de los dos puntos.

## Google Drive

El ID de cliente de Google está al principio de `sync.js` (`GDRIVE_CLIENT_ID`). No es secreto. En Google Cloud, la URI de redirección autorizada debe incluir `https://marcsgc.github.io/graficalo/` (con la barra final).
