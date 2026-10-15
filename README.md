# Code actu MCP server

[![Code actu MCP connector – tool definition quality and endpoint health on Glama](https://glama.ai/mcp/connectors/io.github.Cryptomoon7/codeactu/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Cryptomoon7/codeactu)

Public, read-only [Model Context Protocol](https://modelcontextprotocol.io) server for **[Code actu](https://codeactu.com)**, a French-language directory of referral codes (codes de parrainage) verified on the brands' official pages: online banks, energy, crypto, shopping, telecom, insurance, travel, food delivery, paid surveys.

- **Endpoint:** `https://codeactu.com/mcp` (Streamable HTTP, JSON-RPC 2.0)
- **Authentication:** none
- **Access:** free, read-only, no account, no API key, no personal data collected
- **Coverage:** referral programs available in France and French-speaking countries
- **User guide (FR):** https://codeactu.com/assistants-ia/
- **Privacy:** https://codeactu.com/confidentialite/
- **Registry:** `io.github.Cryptomoon7/codeactu` on the [official MCP Registry](https://registry.modelcontextprotocol.io)

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

**Other MCP clients (Cursor, VS Code, Windsurf…):**

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

## En français

Code actu est un annuaire francophone de **codes de parrainage vérifiés à la source** sur les pages officielles des marques. Ce serveur MCP permet à Claude, ChatGPT et aux autres assistants IA de trouver un code de parrainage, ses avantages pour le filleul et le parrain, ses conditions et sa date de vérification, avec le lien vers la fiche Code actu. Gratuit, en lecture seule, sans compte ni clé d'API. Mode d'emploi : https://codeactu.com/assistants-ia/

## Other discovery files

- MCP server card: https://codeactu.com/.well-known/mcp/server-card.json
- API catalog (RFC 9727): https://codeactu.com/.well-known/api-catalog
- OpenAPI description of the public offers feed: https://codeactu.com/.well-known/openapi-offres.json

## Contact

contact.codeactu@gmail.com

## License

[MIT](LICENSE)
