# Sitio de la cuchillería artesanal

Sitio estático (HTML + CSS + un poco de JS), sin frameworks ni build. Lo mantiene el agente `cm-cuchilleria`
del bot de Discord «Cerebro» desde la carpeta `~/sitios/cuchilleria`, con aprobación de Conrad.

- `index.html`: portada, catálogo, cómo se hacen, contacto.
- `css/estilo.css`: estilos.
- `catalogo.json`: lista de cuchillos `[{"nombre","acero","mango","vaina","precio","foto","descripcion"}]`; `index.html` la lee y arma las tarjetas.
- `img/`: fotos (nombres cortos, sin espacios; idealmente ≤ 1600 px de ancho).

Vista previa local: `python3 -m http.server 8080` dentro de la carpeta y abrir `http://localhost:8080`.
Publicación: GitHub Pages desde la rama `main` (raíz). Cada `git push` publica en un minuto.
