# Instalação detalhada

Registro Civil: Validar Certidão Eletrônica é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_registro_civil_val_cert_eletr`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_registro_civil_val_cert_eletr` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_registro_civil_val_cert_eletr` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_registro_civil_val_cert_eletr` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.registro_civil_val_cert_eletr` (ou `servers.registro_civil_val_cert_eletr` no VS Code) do config do cliente e reinicie.
