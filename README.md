# Apify MCP & n8n Hub — structlabs

Production-ready [Apify](https://apify.com/structlabs) Actors packaged as n8n workflows and MCP servers for AI agents. Each companion repo contains a ready-to-import n8n workflow, a one-file Python and Node quickstart, sanitized sample output, and an MCP config.

## Actors

| Actor | Store | n8n workflow | MCP actor |
|---|---|---|---|
| [Fast Contact, Lead & Tech Stack Extractor](https://github.com/structlabs-hq/fast-contact-lead-extractor-n8n-mcp) | [Store](https://apify.com/structlabs/fast-contact-lead-extractor) | [workflow](https://github.com/structlabs-hq/fast-contact-lead-extractor-n8n-mcp/blob/main/n8n/fast-contact-lead-extractor-workflow.json) | `structlabs/fast-contact-lead-extractor` |
| [Live ATS Jobs API](https://github.com/structlabs-hq/live-ats-jobs-api-n8n-mcp) | [Store](https://apify.com/structlabs/live-ats-jobs-api) | [workflow](https://github.com/structlabs-hq/live-ats-jobs-api-n8n-mcp/blob/main/n8n/live-ats-jobs-api-workflow.json) | `structlabs/live-ats-jobs-api` |
| [SEEK Jobs Salary API (AU + NZ)](https://github.com/structlabs-hq/seek-jobs-salary-api-n8n-mcp) | [Store](https://apify.com/structlabs/seek-jobs-salary-api) | [workflow](https://github.com/structlabs-hq/seek-jobs-salary-api-n8n-mcp/blob/main/n8n/seek-jobs-salary-api-workflow.json) | `structlabs/seek-jobs-salary-api` |
| [AliExpress Search Price Tracker](https://github.com/structlabs-hq/aliexpress-search-price-tracker-n8n-mcp) | [Store](https://apify.com/structlabs/aliexpress-search-price-tracker) | [workflow](https://github.com/structlabs-hq/aliexpress-search-price-tracker-n8n-mcp/blob/main/n8n/aliexpress-search-price-tracker-workflow.json) | `structlabs/aliexpress-search-price-tracker` |
| [Zillow ZIP Market Scraper](https://github.com/structlabs-hq/zillow-zip-market-scraper-n8n-mcp) | [Store](https://apify.com/structlabs/zillow-zip-market-scraper) | [workflow](https://github.com/structlabs-hq/zillow-zip-market-scraper-n8n-mcp/blob/main/n8n/zillow-zip-market-scraper-workflow.json) | `structlabs/zillow-zip-market-scraper` |

## Install all three in one MCP client

```json
{
  "mcpServers": {
    "apify-structlabs": {
      "url": "https://mcp.apify.com/?actors=structlabs/fast-contact-lead-extractor,structlabs/live-ats-jobs-api,structlabs/seek-jobs-salary-api"
    }
  }
}
```

## n8n

```bash
export APIFY_TOKEN=apify_api_...
```

Import any workflow from a companion repo, set `APIFY_TOKEN` in the n8n environment, and run. Workflows use `POST /v2/acts/structlabs~<slug>/run-sync-get-dataset-items`.

## Repos

- [fast-contact-lead-extractor-n8n-mcp](https://github.com/structlabs-hq/fast-contact-lead-extractor-n8n-mcp) — B2B lead, email and tech-stack extraction
- [live-ats-jobs-api-n8n-mcp](https://github.com/structlabs-hq/live-ats-jobs-api-n8n-mcp) — ATS job feeds across 8 providers
- [seek-jobs-salary-api-n8n-mcp](https://github.com/structlabs-hq/seek-jobs-salary-api-n8n-mcp) — SEEK AU/NZ jobs with salary data
- [aliexpress-search-price-tracker-n8n-mcp](https://github.com/structlabs-hq/aliexpress-search-price-tracker-n8n-mcp) — AliExpress search results with numeric price, discount and sold count
- [zillow-zip-market-scraper-n8n-mcp](https://github.com/structlabs-hq/zillow-zip-market-scraper-n8n-mcp) — Zillow listings by ZIP or city with Zestimate and rent Zestimate

## License

MIT

## Combined workflows

Apify-only chains that run two structlabs Actors in one n8n flow, with no external paid services:

- [jobs-to-leads-pipeline.json](workflows/jobs-to-leads-pipeline.json) — Live ATS Jobs API → inferred company domains → Fast Contact lead extractor.
