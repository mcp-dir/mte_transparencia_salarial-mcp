# Instalação detalhada

MTE: Relatório de Transparência Salarial é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_mte_transparencia_salarial`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_mte_transparencia_salarial` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_mte_transparencia_salarial` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_mte_transparencia_salarial` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.mte_transparencia_salarial` (ou `servers.mte_transparencia_salarial` no VS Code) do config do cliente e reinicie.
