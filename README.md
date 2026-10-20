# WABRA MCP Server

> O WhatsApp Business MCP server feito no Brasil — WhatsApp × Claude Desktop / Cursor / Windsurf / ChatGPT / Cline

[![Site](https://img.shields.io/badge/wabra.com.br-live-22C55E?style=flat-square)](https://jadetech-v2.vercel.app)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-3.1-blue?style=flat-square)](https://jadetech-v2.vercel.app/api/openapi.json)
[![License](https://img.shields.io/badge/license-Proprietary-slate?style=flat-square)](#license)

**WABRA** é um Model Context Protocol server hospedado que conecta WhatsApp Business API ao Claude, Cursor, ChatGPT e outros clientes IA — otimizado para o mercado brasileiro.

Diferente dos MCPs genéricos do WhatsApp (US-centric, inglês apenas), o WABRA inclui:
- 🇧🇷 **Enriquecimento CNPJ nativo** (base RFB, 71M empresas) — veja razão social, sócios, CNAE, situação cadastral em uma chamada
- 💬 **Templates PT-BR aprovados Meta** (mercado natural, cobrança, pós-venda)
- 🔗 **Integração CRM BR**: Pipedrive, HubSpot, RD Station, Agendor, Moskit, Conta Azul
- ✅ **Compliance LGPD** nativo

## Install

### Claude Desktop / Code / Cursor / Windsurf / Cline

Adicione ao seu `claude_desktop_config.json` (ou equivalente):

```json
{
  "mcpServers": {
    "wabra": {
      "url": "https://jadetech-v2.vercel.app/api/mcp/mcp",
      "headers": {
        "Authorization": "Bearer wabra_sk_..."
      }
    }
  }
}
```

Reinicie seu cliente IA — as 5 ferramentas WABRA aparecem no painel MCP.

### ChatGPT (Custom GPT via Actions)

Importe a OpenAPI spec: `https://jadetech-v2.vercel.app/api/openapi.json`

### Playground sem instalação

Teste `enrich_cnpj` ao vivo no browser: https://jadetech-v2.vercel.app/connectors/ia-mcp

## Tools disponíveis

| Tool | Status | Descrição |
|---|---|---|
| `enrich_cnpj` | ✅ Live | Razão social, CNAE, sócios, endereço (71M CNPJs RFB via minhareceita.org) |
| `send_whatsapp_message` | 🟡 Beta | Envio direto com templates PT-BR aprovados Meta |
| `list_conversations` | 🟡 Beta | Últimas conversas WhatsApp Business |
| `get_messages` | 🟡 Beta | Histórico completo de uma conversa |
| `search_contacts` | 🟡 Beta | Busca por nome, telefone ou CNPJ |

## Como pegar uma chave API

Durante o soft launch, chaves são criadas manualmente após validação do caso de uso.

Envie um email para **pronto@wabra.com.br** com:
- Seu CNPJ
- Caso de uso principal
- Cliente IA que você usa (Claude Desktop, Cursor, ChatGPT, etc.)
- Volume esperado de mensagens/mês

Resposta em até 24h úteis. Grátis durante o beta.

## Casos de uso

- **Prospecção**: "Claude, baseado no CNPJ 48.084.231/0001-57, me diga quem é a empresa e redija um follow-up WhatsApp personalizado"
- **Resumo de conversas**: "ChatGPT, resuma as últimas 50 conversas WhatsApp com o cliente Mercado Natural e identifique objeções recorrentes"
- **Automação de tickets**: "Cursor, monitore o WhatsApp e crie um ticket GitHub cada vez que um cliente reportar um bug"
- **Enriquecimento em massa**: "Para cada CNPJ nesta lista, retorne razão social, sócios e situação cadastral"

## Links

- 🌐 Site: https://jadetech-v2.vercel.app
- 📄 OpenAPI: https://jadetech-v2.vercel.app/api/openapi.json
- 🧪 Playground: https://jadetech-v2.vercel.app/connectors/ia-mcp
- 📧 Suporte: pronto@wabra.com.br

## Sobre

WABRA é operado por **Jade Bresil LTDA** (CNPJ 48.084.231/0001-57), empresa brasileira sediada no Rio de Janeiro.

WhatsApp® é marca registrada da Meta Platforms, Inc. WABRA é um provedor independente de integração (Business Solution Provider), não afiliado, patrocinado ou endossado pela Meta.

## License

Proprietary. All rights reserved. Este repositório contém apenas documentação pública — o código do servidor MCP é proprietário.
