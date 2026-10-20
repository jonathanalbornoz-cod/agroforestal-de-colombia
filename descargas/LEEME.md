# Paquete para Hostinger

Hay dos paquetes:

- **`arreglo-rapido.zip`** (400 KB) — la página, el código y los datos, sin las
  fotos de producto. Es el que hay que subir cuando las fotos ya están en el
  servidor y lo que falla es el diseño o el catálogo.
- **`sitio-completo.zip`** (35 MB) — el sitio entero, 561 archivos, para una
  instalación desde cero.

Los dos se extraen directamente en `public_html` y se sobrescribe lo que haya.

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
