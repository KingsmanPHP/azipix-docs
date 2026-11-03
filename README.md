# Azipix Docs — Documentação Oficial da API

Documentação interativa construída com [Mintlify](https://mintlify.com) para a plataforma de pagamentos **Azipix**.

## Como rodar localmente

1. Certifique-se de ter o Node.js instalado.
2. Instale o Mintlify CLI globalmente ou execute via `npx`:

```bash
npx mintlify dev
```

3. Acesse `http://localhost:3000` no seu navegador para visualizar as páginas com live-reload.

## Como publicar no Mintlify

1. Crie um repositório no seu GitHub (ex: `KingsmanPHP/azipix-docs`).
2. Conecte o repositório na dashboard do [Mintlify](https://dashboard.mintlify.com).
3. Em **Custom Domain**, aponte para `docs.azipix.com`.
4. Configure o registro DNS CNAME no seu provedor:
   - **Host / Nome**: `docs`
   - **Tipo**: `CNAME`
   - **Destino**: `cname.mintlify.com` (ou o CNAME fornecido pelo Mintlify).

## Estrutura do Projeto

- `mint.json` — Arquivo principal de configuração, tema, cores (`#9255F7`) e navegação.
- `introduction.mdx` — Visão geral da plataforma.
- `quickstart.mdx` — Guia prático de criação de cobranças em 5 minutos.
- `authentication.mdx` — Padrões de cabeçalho e segurança.
- `api-reference/` — Endpoints de Pix, Cartão e consulta.
- `webhooks/` — Instruções completas para postbacks e Pagar.me.
- `advanced/` — Motor de Drops e Idempotência.
