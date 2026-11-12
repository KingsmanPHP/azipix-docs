# Azipix Docs — Documentação Oficial da API

Documentação interativa construída com [Mintlify](https://mintlify.com) para a plataforma de pagamentos **Azipix**.

## Como rodar localmente

1. Certifique-se de ter o Node.js instalado.
2. Instale o Mintlify CLI globalmente ou execute via `npx`:

```bash
npx mintlify dev
```

3. Acesse `http://localhost:3000` no seu navegador para visualizar as páginas com live-reload.

Para conferir links quebrados antes de publicar:

```bash
npx mintlify broken-links
```

## Como publicar no Mintlify

1. Conecte este repositório (`KingsmanPHP/azipix-docs`) na dashboard do [Mintlify](https://dashboard.mintlify.com).
2. Em **Custom Domain**, aponte para `docs.azipix.com`.
3. Configure o registro DNS CNAME no seu provedor:
   - **Host / Nome**: `docs`
   - **Tipo**: `CNAME`
   - **Destino**: `cname.mintlify.com` (ou o CNAME fornecido pelo Mintlify).

## Estrutura do projeto

- `docs.json` — configuração principal (tema, cores `#9255F7`, navegação). `mint.json` é mantido com a mesma navegação para compatibilidade.
- `introduction.mdx` — visão geral, URL base e o que é feito pela API ou só pelo painel.
- `quickstart.mdx` — primeira cobrança Pix em 5 minutos.
- `authentication.mdx` — credenciais `pk_`/`sk_`, escopos, ambientes, chaves vinculadas a subcontas e rotação.
- `environments.mdx` — produção x sandbox, cartões de teste e checklist para ir ao ar.
- `idempotency.mdx` — `X-Idempotency-Key` e como repetir com segurança.
- `errors.mdx` — formatos de erro, códigos, mensagens frequentes e limites.
- `api-reference/charges/` — Pix, cartão (token e cartão + 3DS), consulta, lista, feed de vendas e comprovante.
- `api-reference/payment-links/` — criar e gerenciar links de pagamento (checkout da Azipix).
- `api-reference/balance/` — saldo, extrato, histórico de saques, solicitar saque (Pix e USDT), consultar saque e destinos.
- `api-reference/account/` — métodos e contas liberadas, subcontas.
- `api-reference/chargebacks/` — chargebacks e MED: consulta e envio da defesa.
- `webhooks/` — configuração, validação da assinatura (HMAC) e eventos.

## Como manter

Cada página descreve o comportamento real da API (`hubfy-backend`). Ao mudar uma rota, um campo ou uma regra no backend, atualize a página correspondente e, se a navegação mudar, edite `docs.json` **e** `mint.json`.
