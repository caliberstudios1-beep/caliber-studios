# Caliber Studios — Time. Frame. Precision.

Site institucional da Caliber Studios, um estúdio de imagem e movimento (audiovisual, fotografia e identidade visual). A página única apresenta o estúdio, o filme institucional, a identidade visual (com o manual da marca em PDF), a equipe e o contato.

## Tecnologias

- Site estático pré-renderizado (HTML + CSS + JavaScript), originalmente gerado com um build React/RSC estilo Next.js
- Hospedado no Netlify, servido diretamente da pasta `public/` sem etapa de build

## Rodar localmente

```bash
netlify dev
# ou qualquer servidor estático:
npx serve public
```

## Estrutura

- `public/index.html` — a página
- `public/_next/static/` — CSS e JavaScript compilados (nomes com hash, cache permanente)
- `public/assets/` — imagens, vídeos e o manual da marca
- `netlify.toml` — pasta publicada e cabeçalhos de cache
