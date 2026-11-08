# MiniProj1 — Currículo SPA

Currículo desenvolvido numa única página com Vue 3 e Vite.
A navegação do cabeçalho leva às secções internas do CV.

## Wireframe

O [wireframe em PDF](./wireframe.pdf) apresenta a estrutura da página para computador e telemóvel:
barra de navegação fixa no topo durante o scroll, apresentação, as três secções do currículo e rodapé com ícones sociais. Os links navegam para secções internas da mesma página.

Os dados de experiência, formação, competências e idiomas estão em
`src/data/cv.js`. A experiência e a formação estão em componentes separados em
`src/components/`. O layout e os estilos globais estão em `src/assets/main.css`, importado por `src/main.js`.
