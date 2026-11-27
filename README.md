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
| [Google Ads Transparency API](https://github.com/structlabs-hq/google-ads-transparency-api-n8n-mcp) | [Store](https://apify.com/structlabs/google-ads-transparency-api) | [workflow](https://github.com/structlabs-hq/google-ads-transparency-api-n8n-mcp/blob/main/n8n/google-ads-transparency-api-workflow.json) | `structlabs/google-ads-transparency-api` |
| [Flashscore Tennis Stats API](https://github.com/structlabs-hq/flashscore-tennis-stats-api-n8n-mcp) | [Store](https://apify.com/structlabs/flashscore-tennis-stats-api) | [workflow](https://github.com/structlabs-hq/flashscore-tennis-stats-api-n8n-mcp/blob/main/n8n/flashscore-tennis-stats-api-workflow.json) | `structlabs/flashscore-tennis-stats-api` |
| [Product Hunt Launch Intelligence API](https://github.com/structlabs-hq/producthunt-launch-intelligence-api-n8n-mcp) | [Store](https://apify.com/structlabs/producthunt-launch-intelligence-api) | [workflow](https://github.com/structlabs-hq/producthunt-launch-intelligence-api-n8n-mcp/blob/main/n8n/producthunt-launch-intelligence-api-workflow.json) | `structlabs/producthunt-launch-intelligence-api` |
| [Twitch Live Stream Analytics API](https://github.com/structlabs-hq/twitch-live-stream-analytics-api-n8n-mcp) | [Store](https://apify.com/structlabs/twitch-live-stream-analytics-api) | [workflow](https://github.com/structlabs-hq/twitch-live-stream-analytics-api-n8n-mcp/blob/main/n8n/twitch-live-stream-analytics-api-workflow.json) | `structlabs/twitch-live-stream-analytics-api` |
| [Job Posting Enrichment API](https://github.com/structlabs-hq/job-posting-enrichment-api-n8n-mcp) | [Store](https://apify.com/structlabs/job-posting-enrichment-api) | [workflow](https://github.com/structlabs-hq/job-posting-enrichment-api-n8n-mcp/blob/main/n8n/job-posting-enrichment-api-workflow.json) | `structlabs/job-posting-enrichment-api` |

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
- [google-ads-transparency-api-n8n-mcp](https://github.com/structlabs-hq/google-ads-transparency-api-n8n-mcp) — Google Ads Transparency creatives with format, dates and preview
- [flashscore-tennis-stats-api-n8n-mcp](https://github.com/structlabs-hq/flashscore-tennis-stats-api-n8n-mcp) — Flashscore tennis results with per-set and match stats
- [producthunt-launch-intelligence-api-n8n-mcp](https://github.com/structlabs-hq/producthunt-launch-intelligence-api-n8n-mcp) — Product Hunt rows with n8n workflow and MCP config
- [twitch-live-stream-analytics-api-n8n-mcp](https://github.com/structlabs-hq/twitch-live-stream-analytics-api-n8n-mcp) — Twitch rows with n8n workflow and MCP config
- [job-posting-enrichment-api-n8n-mcp](https://github.com/structlabs-hq/job-posting-enrichment-api-n8n-mcp) — ATS postings with company domain, function, seniority and hiring velocity

## License

MIT

## Combined workflows

Apify-only chains that run two structlabs Actors in one n8n flow, with no external paid services:

- [jobs-to-leads-pipeline.json](workflows/jobs-to-leads-pipeline.json) — Live ATS Jobs API → inferred company domains → Fast Contact lead extractor.
