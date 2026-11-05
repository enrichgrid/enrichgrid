<p align="center">
  <a href="https://enrichgrid.com/?ref=github"><img src="https://enrichgrid.com/static/icon-512.png" width="96" height="96" alt="EnrichGrid"></a>
</p>

<h1 align="center">EnrichGrid</h1>

<p align="center">
  <b>LinkedIn person, company and school data through one REST API.</b><br>
  Pay only for profiles that are found. 50 free credits, no card.
</p>

<p align="center">
  <a href="https://enrichgrid.com/?ref=github">Website</a> ·
  <a href="https://enrichgrid.com/api-docs?ref=github">API docs</a> ·
  <a href="https://enrichgrid.com/mcp-server?ref=github">MCP server</a> ·
  <a href="https://enrichgrid.com/chrome-extension?ref=github">Chrome extension</a> ·
  <a href="https://www.postman.com/enrichgrid-api/enrichgrid-api">Postman</a>
</p>

---

### What you get

| | |
|---|---|
| **Person enrichment** | Name, headline, current role and seniority, company with website and headcount, full work history, education, skills |
| **Company & school enrichment** | Industry, headcount, website, HQ, founding year, specialties |
| **People search** | By job title, current or past company, country, city, company size, tenure, school |
| **Bulk** | Upload Excel / CSV with up to 10,000 LinkedIn URLs, download it enriched |
| **AI agents** | MCP server for Claude, Cursor and other MCP clients |

Not found = not charged. Repeat lookups within 30 days are instant.

### Quick start

```bash
curl -X POST https://enrichgrid.com/v1/enrich/person \
  -H "x-api-key: YOUR_API_KEY" -H "content-type: application/json" \
  -d '{"identifier": "https://www.linkedin.com/in/williamhgates"}'
```

```python
import requests

r = requests.post(
    "https://enrichgrid.com/v1/enrich/person",
    headers={"x-api-key": "YOUR_API_KEY"},
    json={"identifier": "https://www.linkedin.com/in/williamhgates"},
)
print(r.json()["profile"]["current_title"])
```

Get a key: [enrichgrid.com/signup](https://enrichgrid.com/signup?ref=github)

### Use with AI agents (MCP)

```bash
claude mcp add --transport http enrichgrid https://enrichgrid.com/mcp --header "x-api-key: YOUR_API_KEY"
```

Listed in the [official MCP Registry](https://registry.modelcontextprotocol.io) as `com.enrichgrid/enrichgrid` and on [Glama](https://glama.ai/mcp/connectors/com.enrichgrid/enrichgrid).

### Pricing

Free 50 credits · Starter $29/mo (10,000) · Growth $99/mo (50,000) · Scale $299/mo (250,000) · Enterprise $999/mo (1,000,000).
One credit per found profile, company or school. [Full pricing](https://enrichgrid.com/?ref=github#pricing)

### Contact

[support@enrichgrid.com](mailto:support@enrichgrid.com) · Telegram [@EnrichGrid_bot](https://t.me/EnrichGrid_bot)
