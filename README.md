# Sitio de la cuchillería artesanal

Sitio estático (HTML + CSS + un poco de JS), sin frameworks ni build. Lo mantiene el agente `cm-cuchilleria`
del bot de Discord «Cerebro» desde la carpeta `~/sitios/cuchilleria`, con aprobación de Conrad.

- `index.html`: portada (foto grande + titular), galería «bento», cinta, «Piezas» (se arma sola desde
  `catalogo.json`), «Del fuego a la mano» (carrusel de 5 pasos) y cierre de contacto (sin formulario por ahora).
- `css/estilo.css`: estilo oscuro, tipografía grande (Inter Tight / Inter desde Google Fonts), tarjetas redondeadas.
  Si se cambia, actualizar el `?v=` del `<link>` en `index.html` para que no quede cacheado.
- `catalogo.json`: lista de cuchillos `[{"nombre","acero","mango","vaina","precio","foto","descripcion"}]`;
  `foto` es un archivo dentro de `img/`. Un precio «a definir» se muestra como «Precio a consultar».
- `img/`: fotos (nombres cortos, sin espacios). Antes de subirlas, achicarlas:
  `sips -Z 1600 -s formatOptions 82 img/foto.jpg --out img/foto.jpg` (los originales quedan en
  `~/discord-bot/data/adjuntos/cuchilleria-web/`).

Vista previa local: `python3 -m http.server 8080` dentro de la carpeta y abrir `http://localhost:8080`.
Publicación: GitHub Pages desde el repo `conradoColomer/tma_cuchillos`, rama `master` (raíz):
`https://conradocolomer.github.io/tma_cuchillos/`. Cada `git push` publica en un minuto.
