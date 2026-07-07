# Campo na Mão — Gestão Completa da Fazenda

App de gestão de gado (leiteiro e de corte) para múltiplas fazendas.
Feito em React (via CDN + Babel standalone, sem build step),
Supabase (banco + autenticação) e publicado no Cloudflare Pages.

## Estrutura

```
index.html   → o app inteiro (front-end). O código React de verdade
               fica dentro de uma tag <script type="text/plain" id="app-source">
               — isso é proposital, é o que permite salvar/reabrir o
               arquivo sem perder o código-fonte (um script separado
               lê esse conteúdo, compila com Babel no navegador, e roda).
```

## ⚠️ Faltando neste repositório (ainda)

Esse repositório foi criado a partir do arquivo publicado hoje no
Cloudflare Pages (`rebanhominuto.pages.dev`), recuperado via
"Salvar Como" no Safari. Ele contém o app completo e funcional, mas
**não contém o histórico de migrações SQL** do banco (essas foram
feitas em conversas anteriores e não estão salvas em arquivo ainda).

Se formos mexer nesse projeto de novo, vale reconstruir esse
histórico aos poucos — toda vez que rodarmos um SQL novo no Supabase
desse projeto, já salvamos aqui em `supabase/migrations/`, do mesmo
jeito que organizamos o Mercado Control.

## Deploy

Mesma configuração do Mercado Control: conecte este repositório ao
Cloudflare Pages (Build command: nenhum / Output directory: `/`).
Todo `git push` na branch principal publica automaticamente.
