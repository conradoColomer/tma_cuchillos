# Sitio de la cuchillería artesanal

Sitio estático (HTML + CSS + un poco de JS), sin frameworks ni build. Lo mantiene el agente `cm-cuchilleria`
del bot de Discord «Cerebro» desde la carpeta `~/sitios/cuchilleria`, con aprobación de Conrad.

- `index.html`: portada, catálogo, cómo se hacen, contacto.
- `css/estilo.css`: estilos.
- `catalogo.json`: lista de cuchillos `[{"nombre","acero","mango","vaina","precio","foto","descripcion"}]`; `index.html` la lee y arma las tarjetas.
- `img/`: fotos (nombres cortos, sin espacios). Antes de subirlas, achicarlas: `sips -Z 1600 -s formatOptions 82 img/foto.jpg --out img/foto.jpg` (los originales quedan en `~/discord-bot/data/adjuntos/cuchilleria-web/`).

Vista previa local: `python3 -m http.server 8080` dentro de la carpeta y abrir `http://localhost:8080`.
Publicación: GitHub Pages desde el repo `conradoColomer/tma_cuchillos`, rama `master` (raíz): `https://conradocolomer.github.io/tma_cuchillos/`. Cada `git push` publica en un minuto.
