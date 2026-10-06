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
| 02 | [selección + ficha](02-seleccion-ficha/) (líneas 5 + 6 sobre la 1) | descartada: sustituida por Rajoles, se veía genérica | [`fac8c2e`](https://github.com/meowrhino/annaCarreras/tree/fac8c2e7d03d48ee8154a86d50b5fb24253b5bbf) |
| 03 | [la web es un output](03-web-output/) (línea A sobre la 02) | sustituida por la 04: el seed teñía también el contenido y se veía casi igual que la B | [`ccde40e`](https://github.com/meowrhino/annaCarreras/tree/ccde40e64bfb3ea9ad251c5cfe9e9f3e0adbaa71) |
| 04 | [hoja fija](04-hoja-fija/) (línea A: el seed solo pinta el fondo) | descartada: sustituida por Rajoles, se veía genérica | [`587a3e7`](https://github.com/meowrhino/annaCarreras/tree/587a3e7b1b3c2f7f41473b59af43b3e09a9461dd) |
| 05 | [portadas vivas](05-portadas-vivas/) (línea B sobre la 04: Trossets on-chain en la portada) | descartada: sustituida por Rajoles, se veía genérica | [`a11d51d`](https://github.com/meowrhino/annaCarreras/tree/a11d51dafbefd0f3c533e2da69983afc16062f04) |
| 06 | [rajoles](06-rajoles/) (Trossets de verdad en rejilla, con mandos y animaciones; el fondo se mueve con el scroll) | sustituida en la web por el fondo fijo (scrollea la hoja, no la página) | [`4383436`](https://github.com/meowrhino/annaCarreras/tree/4383436708e2d5454da3663d0c41ff32f975435d) |
| 07 | [fondo fijo](07-fondo-fijo/) (Rajoles: el fondo quieto y la hoja hace scroll por dentro) | descartada por Anna (2026-10-06): el contenido flotando con scroll en medio se ve de principios de los 2000; quiere contenido grande, y que el fondo se vea claramente generado y animado | [`c39df68`](https://github.com/meowrhino/annaCarreras/tree/c39df68c6a1c1aa66154cf690f2d9978cf834ca3) |
| 08 | [proto A · B · C](08-proto-abc/) (índice tipográfico, parrilla con filtro, home generativa; con los 103 posts del WordPress) | descartadas: se rehace desde el feedback de Anna (2026-10-06) | [`ba0a310`](https://github.com/meowrhino/annaCarreras/tree/ba0a3105a5cd95eb651407417c63dffd1e4822e0) |

## Cómo se archiva un diseño

1. Copiar la carpeta de la prueba (`index.html`, `style.css` y todos sus
   `.js`, también los de `js/`) a una
   carpeta nueva `NN-nombre/`.
2. En su `index.html`, fijar el contenido a un commit de annaCarreras:

   ```html
   <html lang="en" data-content="https://raw.githubusercontent.com/meowrhino/annaCarreras/<sha>/">
   ```

   (Los de `proto/` no leen `data-content`: se fija `BASE` en `proto.js`.)
   Así el diseño sigue funcionando aunque el contenido o su esquema cambien
   después: lee siempre los JSON y las imágenes de ese commit.
3. Añadir la fila a la tabla de arriba y al `index.html` de la raíz. Si se
   descarta, cambiar el estado y apuntar por qué en una línea.

Sin frameworks ni build: HTML, CSS y JS a pelo. Para verlo en local:

```bash
python3 -m http.server 8766
```
