# annaCarreras — diseños

Archivo de las pruebas de diseño para annacarreras.com: cada línea que se prueba
se guarda aquí tal cual estaba, también las que se descartan, para poder volver
a verlas y recuperar ideas.

El contenido y el trabajo vivo están en
[meowrhino/annaCarreras](https://github.com/meowrhino/annaCarreras).

<https://meowrhino.github.io/annaCarreras-disenos/>

## Diseños

Agrupados por familia: dentro de una familia el esqueleto es el mismo y cada
versión cambia una cosa. La columna «idea» es lo que se puede llevar a otra web.

### Listas de texto

| # | diseño | idea | estado | contenido |
|---|---|---|---|---|
| 01 | [índice cronológico](01-indice-cronologico/) | tabla por año: título, categorías y tags, sin imágenes | integrado en la 02 como Archive | [`7f4a0de`](https://github.com/meowrhino/annaCarreras/tree/7f4a0deae4e0107bc07f95be76b66bca971b88f1) |
| 08A | [índice tipográfico](08-proto-abc/a-index.html) | como la 01 a escala (103 proyectos), con separadores por década y la portada al hover | descartada: se rehace desde el feedback de Anna (2026-10-06) | [`ba0a310`](https://github.com/meowrhino/annaCarreras/tree/ba0a3105a5cd95eb651407417c63dffd1e4822e0) |

### Tarjetas a dos columnas (selección + ficha)

| # | diseño | idea | estado | contenido |
|---|---|---|---|---|
| 02 | [selección + ficha](02-seleccion-ficha/) | portada, título, año y una frase; proyecto con ficha arriba | descartada: sustituida por Rajoles, se veía genérica | [`fac8c2e`](https://github.com/meowrhino/annaCarreras/tree/fac8c2e7d03d48ee8154a86d50b5fb24253b5bbf) |
| 03 | [la web es un output](03-web-output/) | variante de la 02: una semilla tiñe toda la web y pinta un marco Truchet | sustituida por la 04: se veía casi igual que la B | [`ccde40e`](https://github.com/meowrhino/annaCarreras/tree/ccde40e64bfb3ea9ad251c5cfe9e9f3e0adbaa71) |
| 04 | [hoja fija](04-hoja-fija/) | variante de la 03: la semilla solo pinta el marco; el contenido va en una hoja | descartada: sustituida por Rajoles, se veía genérica | [`587a3e7`](https://github.com/meowrhino/annaCarreras/tree/587a3e7b1b3c2f7f41473b59af43b3e09a9461dd) |
| 05 | [portadas vivas](05-portadas-vivas/) | variante de la 04: la portada de Trossets es el código on-chain corriendo | descartada: sustituida por Rajoles, se veía genérica | [`a11d51d`](https://github.com/meowrhino/annaCarreras/tree/a11d51dafbefd0f3c533e2da69983afc16062f04) |
| 08B | [parrilla con filtro](08-proto-abc/b-grid.html) | portadas en rejilla con filtro por categoría y su número de piezas | descartada: se rehace desde el feedback de Anna (2026-10-06) | [`ba0a310`](https://github.com/meowrhino/annaCarreras/tree/ba0a3105a5cd95eb651407417c63dffd1e4822e0) |

### Fondo generativo

| # | diseño | idea | estado | contenido |
|---|---|---|---|---|
| 06 | [rajoles](06-rajoles/) | Trossets en rejilla con la paleta del día; mandos de día, paleta y semilla en el pie; cambios lentos y rastro del cursor. El fondo se mueve con el scroll | sustituida por la 07 | [`4383436`](https://github.com/meowrhino/annaCarreras/tree/4383436708e2d5454da3663d0c41ff32f975435d) |
| 07 | [fondo fijo](07-fondo-fijo/) | variante de la 06: el fondo quieto y la hoja hace scroll por dentro (sin tirones en móvil) | descartada por Anna (2026-10-06): el contenido flotando con scroll en medio se ve de principios de los 2000; quiere contenido grande y que el fondo se vea claramente generado y animado | [`c39df68`](https://github.com/meowrhino/annaCarreras/tree/c39df68c6a1c1aa66154cf690f2d9978cf834ca3) |
| 09 | [rajoles grande](09-rajoles-grande/) | primer intento con el feedback de Anna: portadas a sangre con título y año encima (v3ga), proyecto con el vídeo arriba (La Diegol), el fondo cambia cada 0,25 s | descartada: se rehace de cero sin Rajoles (la 10) | [`fb9e4e7`](https://github.com/meowrhino/annaCarreras/tree/fb9e4e7d0a4f4fc19fcf77a37114e54508c789be) |
| 08C | [home generativa](08-proto-abc/c-canvas.html) | Truchet multiescala a pantalla completa en la portada y el índice debajo, a dos columnas; `?still` lo pinta de golpe | descartada: se rehace desde el feedback de Anna (2026-10-06) | [`ba0a310`](https://github.com/meowrhino/annaCarreras/tree/ba0a3105a5cd95eb651407417c63dffd1e4822e0) |

La 08 es una sola carpeta: A, B y C comparten `base.css`, `proto.js` y
`density.json` (los 103 posts del WordPress, portadas enlazadas a
annacarreras.com). [`08-proto-abc/`](08-proto-abc/) explica las tres y sus riesgos.

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
