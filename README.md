# annaCarreras — diseños

Archivo de las pruebas de diseño para annacarreras.com: cada línea que se prueba
se guarda aquí tal cual estaba, también las que se descartan, para poder volver
a verlas y recuperar ideas.

El contenido y el trabajo vivo están en
[meowrhino/annaCarreras](https://github.com/meowrhino/annaCarreras).

<https://meowrhino.github.io/annaCarreras-disenos/>

## Diseños

| # | línea | estado | contenido |
|---|---|---|---|
| 01 | [índice cronológico](01-indice-cronologico/) | integrado en la 02 como Archive | [`7f4a0de`](https://github.com/meowrhino/annaCarreras/tree/7f4a0deae4e0107bc07f95be76b66bca971b88f1) |
| 02 | [selección + ficha](02-seleccion-ficha/) (líneas 5 + 6 sobre la 1) | en prueba, textos provisionales | [`fac8c2e`](https://github.com/meowrhino/annaCarreras/tree/fac8c2e7d03d48ee8154a86d50b5fb24253b5bbf) |
| 03 | [la web es un output](03-web-output/) (línea A sobre la 02) | en prueba, marco provisional | [`ccde40e`](https://github.com/meowrhino/annaCarreras/tree/ccde40e64bfb3ea9ad251c5cfe9e9f3e0adbaa71) |

## Cómo se archiva un diseño

1. Copiar la carpeta de la prueba (`index.html`, `style.css`, `app.js` y los
   `.js` que tenga) a una
   carpeta nueva `NN-nombre/`.
2. En su `index.html`, fijar el contenido a un commit de annaCarreras:

   ```html
   <html lang="en" data-content="https://raw.githubusercontent.com/meowrhino/annaCarreras/<sha>/">
   ```

   Así el diseño sigue funcionando aunque el contenido o su esquema cambien
   después: lee siempre los JSON y las imágenes de ese commit.
3. Añadir la fila a la tabla de arriba y al `index.html` de la raíz. Si se
   descarta, cambiar el estado y apuntar por qué en una línea.

Sin frameworks ni build: HTML, CSS y JS a pelo. Para verlo en local:

```bash
python3 -m http.server 8766
```
