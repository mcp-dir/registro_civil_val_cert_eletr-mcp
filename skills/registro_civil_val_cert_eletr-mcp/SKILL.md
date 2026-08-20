---
name: registro_civil_val_cert_eletr-mcp
description: Skill da REST API do Registro Civil: Validar Certidão Eletrônica na MCP.AI: 1 endpoint em /api/registro_civil_val_cert_eletr. Registro Civil: Validar Certidão Eletrônica, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Registro Civil: Validar Certidão Eletrônica — REST API skill

Você tem acesso à **Registro Civil: Validar Certidão Eletrônica** REST API na MCP.AI.

> Registro Civil: Validar Certidão Eletrônica, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/registro_civil_val_cert_eletr
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
curl -X POST https://api.mcp.ai/api/registro_civil_val_cert_eletr/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"codigo_certidao":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/registro_civil_val_cert_eletr/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `registro_civil_val_cert_eletr_consultar`

Registro Civil: Validar Certidão Eletrônica, consulta em fonte oficial. _(POST /api/registro_civil_val_cert_eletr/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `codigo_certidao` | string | Sim | Parâmetro de consulta "codigo_certidao". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_registro_civil_val_cert_eletr` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
