# Code actu MCP server

Public, read-only [Model Context Protocol](https://modelcontextprotocol.io) server for **Code actu**, a French-language directory of referral codes verified on the brands' official pages (online banks, energy, crypto, shopping, telecom, insurance, travel, paid surveys).

- **Endpoint:** `https://codeactu.com/mcp` (Streamable HTTP, JSON-RPC 2.0)
- **Authentication:** none
- **Access:** read-only, no account, no personal data collected
- **User guide (FR):** https://codeactu.com/assistants-ia/
- **Privacy:** https://codeactu.com/confidentialite/

## Tools

| Tool | What it does |
| --- | --- |
| `rechercher_offres` | Search offers by brand or keyword |
| `detail_offre` | Full page for one brand: code, referee and referrer rewards, conditions, payout delay, verification date, official source |
| `comparer_offres` | Compare 2 to 5 brands |
| `offres_par_categorie` | List the offers of a category |
| `meilleures_offres` | Monthly selection of the best referral offers |
| `lister_categories` | Categories and number of offers |

ChatGPT clients also get the standard `search` and `fetch` tools.

Every answer includes the URL of the Code actu page and of the brand's official page, so the terms can be checked before signing up. Gambling, casino and prediction-market offers are not served.

## Add it

**Claude:** Settings > Connectors > Add custom connector, URL `https://codeactu.com/mcp`, no authentication.

**Other MCP clients:**

```json
{
  "mcpServers": {
    "codeactu": { "type": "http", "url": "https://codeactu.com/mcp" }
  }
}
```

## Example prompts

- « Quel est le code de parrainage BoursoBank vérifié par Code actu ? »
- « Compare les offres de parrainage Fortuneo et BoursoBank. »
- « Quelles sont les meilleures offres de parrainage ce mois-ci ? »

## Contact

contact.codeactu@gmail.com
