---
name: mte_transparencia_salarial-mcp
description: Skill da REST API do MTE: Relatório de Transparência Salarial na MCP.AI: 1 endpoint em /api/mte_transparencia_salarial. MTE: Relatório de Transparência Salarial, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# MTE: Relatório de Transparência Salarial — REST API skill

Você tem acesso à **MTE: Relatório de Transparência Salarial** REST API na MCP.AI.

> MTE: Relatório de Transparência Salarial, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/mte_transparencia_salarial
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
curl -X POST https://api.mcp.ai/api/mte_transparencia_salarial/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"cnpj":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/mte_transparencia_salarial/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `mte_transparencia_salarial_consultar`

MTE: Relatório de Transparência Salarial, consulta em fonte oficial. _(POST /api/mte_transparencia_salarial/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Sim | Parâmetro de consulta "cnpj". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_mte_transparencia_salarial` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
