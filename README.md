<p align="center">
  <a href="https://enrichgrid.com/?ref=github"><img src="https://enrichgrid.com/static/icon-512.png" width="96" height="96" alt="EnrichGrid"></a>
</p>

<h1 align="center">EnrichGrid</h1>

<p align="center">
  <b>LinkedIn profile &amp; company scraper API: person, company and school data as JSON.</b><br>
  Pay only for profiles that are found. 50 free credits, no card.
</p>

<p align="center">
  <a href="https://enrichgrid.com/?ref=github">Website</a> ·
  <a href="https://enrichgrid.com/api-docs?ref=github">API docs</a> ·
  <a href="https://enrichgrid.com/mcp-server?ref=github">MCP server</a> ·
  <a href="https://chromewebstore.google.com/detail/camfalbgbfimllhmdncpjmnaabidceci">Chrome extension</a> ·
  <a href="https://pypi.org/project/enrichgrid/">Python SDK</a> ·
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
| **On LinkedIn** | Chrome extension: the profile or company you are viewing, decision makers, leads to CSV |

Not found = not charged. Repeat lookups within 30 days are instant.

### Quick start

```bash
curl -X POST https://enrichgrid.com/v1/enrich/person \
  -H "x-api-key: YOUR_API_KEY" -H "content-type: application/json" \
  -d '{"identifier": "https://www.linkedin.com/in/williamhgates"}'
```

```bash
pip install enrichgrid
```

```python
from enrichgrid import Client

eg = Client("YOUR_API_KEY")  # or set ENRICHGRID_KEY
lookup = eg.person("https://www.linkedin.com/in/williamhgates")
print(lookup["profile"]["current_title"])
```

Get a key: [enrichgrid.com/signup](https://enrichgrid.com/signup?ref=github)

### Libraries and integrations

| | |
|---|---|
| [enrichgrid-python](https://github.com/enrichgrid/enrichgrid-python) | Python SDK and CLI: `pip install enrichgrid`, then `enrichgrid csv leads.csv` enriches a CSV file |
| [proxycurl-adapter](https://github.com/enrichgrid/proxycurl-adapter) | Drop-in for code written for Proxycurl: returns Proxycurl-shaped profiles |
| [n8n-nodes-enrichgrid](https://github.com/enrichgrid/n8n-nodes-enrichgrid) | n8n community node, plus [ready-made workflows](https://enrichgrid.com/integrations/n8n?ref=github) |
| [Chrome extension](https://chromewebstore.google.com/detail/camfalbgbfimllhmdncpjmnaabidceci) | Profile & company data on the LinkedIn page you are viewing, leads to CSV |
| [Apify Actor](https://apify.com/enrichgrid/linkedin-profile-scraper) | LinkedIn profile scraper on Apify, no cookies |
| [Postman](https://www.postman.com/enrichgrid-api/enrichgrid-api) | Every endpoint as a ready collection |

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
