# AGENTS.md

## O que é
Site estático de página única da Caliber Studios, espelhado a partir da versão publicada originalmente em `caliber-studios.guigranjaabreu.chatgpt.site`. Não há código-fonte, package.json nem etapa de build — apenas a saída compilada.

## Arquitetura
- `netlify.toml` publica `public/` diretamente (sem comando de build).
- `public/index.html` é HTML renderizado no servidor com um payload RSC inline; os chunks em `public/_next/static/chunks/` fazem a hidratação (menu, cursor, barra de progresso, vídeos).
- Os vídeos (`assets/*.mp4`) são definidos pelo JavaScript em tempo de execução, não pelo HTML.
- `robots.txt` e `sitemap.xml` apontam para `luxury-raindrop-332148.netlify.app`; atualize-os se um domínio próprio for configurado.

## Convenções
- Para mudar textos, edite `public/index.html` **e** o payload RSC inline no mesmo arquivo (o cliente hidrata a partir dele); textos divergentes podem causar erros de hidratação.
- Não renomeie arquivos em `_next/static/` — os nomes com hash são referenciados entre os chunks.
- Não existe backend; o contato é feito via link `mailto:`.
