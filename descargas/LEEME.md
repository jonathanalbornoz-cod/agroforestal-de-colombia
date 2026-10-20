# Paquete para Hostinger

`sitio-completo.zip` es el sitio entero en un solo archivo: 561 archivos, 35 MB.
Sustituye a las tres partes de antes, que se subían incompletas.

## Subirlo

1. Descárgalo con el botón **Download** de GitHub.
2. En el administrador de archivos de Hostinger, respalda y vacía `public_html`.
3. Sube `sitio-completo.zip` a `public_html` y pulsa **Extraer**.
4. Borra el ZIP del servidor y abre el sitio con **Ctrl+F5**.

Dentro del ZIP no hay carpeta contenedora: `index.html` queda directamente
en `public_html/index.html`, que es donde tiene que estar.

## Comprobarlo

`https://agroforestaldecolombia.com/revision.html` pide los 558 archivos del
sitio uno por uno y dice cuáles faltan. Bórralo del servidor cuando todo esté bien.

## Regenerarlo

Cuando cambie algo en este repositorio, el ZIP queda viejo. Para rehacerlo:

```sh
git archive --format=zip -o descargas/sitio-completo.zip HEAD \
  ':!descargas' ':!*.md' ':!.github'
```
