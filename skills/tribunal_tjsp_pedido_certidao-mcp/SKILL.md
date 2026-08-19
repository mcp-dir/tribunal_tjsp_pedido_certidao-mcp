---
name: tribunal_tjsp_pedido_certidao-mcp
description: Skill da REST API do Tribunal TJSP: Cadastro de Pedido de Certidão na MCP.AI: 1 endpoint em /api/tribunal_tjsp_pedido_certidao. Tribunal TJSP: Cadastro de Pedido de Certidão, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TJSP: Cadastro de Pedido de Certidão — REST API skill

Você tem acesso à **Tribunal TJSP: Cadastro de Pedido de Certidão** REST API na MCP.AI.

> Tribunal TJSP: Cadastro de Pedido de Certidão, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tjsp_pedido_certidao
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/tribunal_tjsp_pedido_certidao/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"modelo":"...","email_envio":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tjsp_pedido_certidao/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tjsp_pedido_certidao_consultar`

Tribunal TJSP: Cadastro de Pedido de Certidão, consulta em fonte oficial. _(POST /api/tribunal_tjsp_pedido_certidao/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `modelo` | string | Sim | Parâmetro de consulta "modelo". |
| `email_envio` | string | Sim | Parâmetro de consulta "email_envio". |
| `nome_completo` | string | Não | Parâmetro de consulta "nome_completo". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `rg` | string | Não | Parâmetro de consulta "rg". |
| `cin` | string | Não | Parâmetro de consulta "cin". |
| `razao_social` | string | Não | Parâmetro de consulta "razao_social". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `genero` | string | Não | Parâmetro de consulta "genero". |
| `nome_mae` | string | Não | Parâmetro de consulta "nome_mae". |
| `nome_pai` | string | Não | Parâmetro de consulta "nome_pai". |
| `birthdate` | string | Não | Parâmetro de consulta "birthdate". |
| `naturalidade_municipio` | string | Não | Parâmetro de consulta "naturalidade_municipio". |
| `naturalidade_uf` | string | Não | Parâmetro de consulta "naturalidade_uf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tjsp_pedido_certidao` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
