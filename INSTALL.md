# Instalação rápida

Registro Civil: Validar Certidão Eletrônica é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_registro_civil_val_cert_eletr`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Registro Civil: Validar Certidão Eletrônica` / `https://api.mcp.ai/p_registro_civil_val_cert_eletr`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "registro_civil_val_cert_eletr": { "type": "http", "url": "https://api.mcp.ai/p_registro_civil_val_cert_eletr" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=registro_civil_val_cert_eletr&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9yZWdpc3Ryb19jaXZpbF92YWxfY2VydF9lbGV0ciJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "registro_civil_val_cert_eletr": { "url": "https://api.mcp.ai/p_registro_civil_val_cert_eletr" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=registro_civil_val_cert_eletr&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_registro_civil_val_cert_eletr%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "registro_civil_val_cert_eletr": { "type": "http", "url": "https://api.mcp.ai/p_registro_civil_val_cert_eletr" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_registro_civil_val_cert_eletr
```

Dúvidas? [registro_civil_val_cert_eletr@mcp.ai](mailto:registro_civil_val_cert_eletr@mcp.ai)
