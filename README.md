# WebDataTools Leads, jobs & company data MCP server
`webdatatools-leads-mcp`

An MCP server with 22 leads, jobs & company data tools for AI agents — Claude Desktop, Cursor, Cline or any MCP client. Company profiles from a domain, hiring signals from ATS boards, Y Combinator companies, Wikidata enrichment, e-mail validation, OpenStreetMap places, market quotes and remote jobs.

**This server uses *your own* Apify API token.** Every tool call runs a [WebDataTools](https://apify.com/webdatatools) Actor under your Apify account and is billed to your Apify credit — pay per result, the price is in each tool description. Your token is only sent to Apify's API.

## Quick start

Requires Node.js 18+.

```bash
APIFY_TOKEN=apify_api_... npx -y github:paulet4a-commits/webdatatools-leads-mcp
```

Get a free token (the free plan includes monthly credit): https://console.apify.com/settings/integrations

## Claude Desktop / Cursor

Add this to `claude_desktop_config.json` (Claude Desktop) or `.cursor/mcp.json` (Cursor):

```json
{
  "mcpServers": {
    "webdatatools-leads": {
      "command": "npx",
      "args": [
        "-y",
        "github:paulet4a-commits/webdatatools-leads-mcp"
      ],
      "env": {
        "APIFY_TOKEN": "apify_api_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
      }
    }
  }
}
```

## Tools (22)

| Tool | What it does | Price (free plan) | Backing Actor |
|---|---|---|---|
| `career_site_jobs_api` | Career Site Jobs API (Greenhouse, Lever, Ashby, Workday +1) | $0.003 / job | [Actor](https://apify.com/webdatatools/career-site-jobs-api) |
| `google_maps_scraper` | Google Maps Scraper | $0.002 / place | [Actor](https://apify.com/webdatatools/google-maps-scraper) |
| `2gis_places_scraper` | 2GIS Places Scraper (Phones, Websites, Ratings, Hours) | $0.002 / place | [Actor](https://apify.com/webdatatools/2gis-places-scraper) |
| `linkedin_jobs_scraper` | LinkedIn Jobs Scraper | $0.001 / job | [Actor](https://apify.com/webdatatools/linkedin-jobs-scraper) |
| `company_360` | Company 360: full company profile from a domain | $0.05 / company | [Actor](https://apify.com/webdatatools/company-360) |
| `hiring_signals` | Hiring Signals Scraper (Greenhouse, Lever, Ashby, Workable) | $0.002 / result | [Actor](https://apify.com/webdatatools/hiring-signals) |
| `yc_companies_scraper` | Y Combinator Companies & Founders Scraper | $0.002 / result | [Actor](https://apify.com/webdatatools/yc-companies-scraper) |
| `wikidata_entity_enrichment` | Wikidata Entity & Company Enrichment (facts, IDs, links) | $0.001 / result | [Actor](https://apify.com/webdatatools/wikidata-entity-enrichment) |
| `email_validator` | Email Validator & Verifier — Bulk Email Check | $0.0005 / email | [Actor](https://apify.com/webdatatools/email-validator) |
| `overpass_poi_extractor` | OpenStreetMap POI Extractor (Overpass API: shops, amenities) | $0.0005 / place | [Actor](https://apify.com/webdatatools/overpass-poi-extractor) |
| `market_quotes` | Stock, Crypto & FX Quotes | $0.001 / Quote | [Actor](https://apify.com/webdatatools/market-quotes) |
| `yahoo_finance_scraper` | Yahoo Finance Scraper (Quotes, Fundamentals, Financials, News) | $0.0015 / symbol | [Actor](https://apify.com/webdatatools/yahoo-finance-scraper) |
| `dexscreener_scraper` | DexScreener Scraper (DEX Pairs, Prices, Liquidity, Boosts) | $0.0005 / row | [Actor](https://apify.com/webdatatools/dexscreener-scraper) |
| `polymarket_scraper` | Polymarket Scraper (Prediction Markets, Odds, Volume) | $0.001 / market | [Actor](https://apify.com/webdatatools/polymarket-scraper) |
| `stocktwits_scraper` | StockTwits Scraper (Messages, Sentiment, Trending) | $0.0005 / message | [Actor](https://apify.com/webdatatools/stocktwits-scraper) |
| `remote_jobs_aggregator` | Remote Jobs Aggregator (RemoteOK, WWR, Hacker News) | $0.001 / Job | [Actor](https://apify.com/webdatatools/remote-jobs-aggregator) |
| `seek_jobs_scraper` | Seek Jobs Scraper (Australia & New Zealand) | $0.001 / job | [Actor](https://apify.com/webdatatools/seek-jobs-scraper) |
| `wellfound_jobs_scraper` | Wellfound Jobs Scraper (AngelList Startup Jobs) | $0.002 / job | [Actor](https://apify.com/webdatatools/wellfound-jobs-scraper) |
| `stepstone_scraper` | StepStone Scraper (Germany, Austria, Belgium Jobs) | $0.001 / job | [Actor](https://apify.com/webdatatools/stepstone-scraper) |
| `naukri_jobs_scraper` | Naukri Jobs Scraper (Salary, Skills, Company Rating) | $0.0008 / job | [Actor](https://apify.com/webdatatools/naukri-jobs-scraper) |
| `zillow_scraper` | Zillow Scraper (Homes for Sale, Rent & Sold, Zestimates) | $0.001 / home | [Actor](https://apify.com/webdatatools/zillow-scraper) |
| `zillow_detail_scraper` | Zillow Home Details Scraper (Description, Photos, History) | $0.003 / home | [Actor](https://apify.com/webdatatools/zillow-detail-scraper) |

## More WebDataTools MCP servers

- [webdatatools-mcp-server](https://github.com/paulet4a-commits/webdatatools-mcp-server) — the 10 most popular tools in one server
- [webdatatools-domain-mcp](https://github.com/paulet4a-commits/webdatatools-domain-mcp) — Domain & website intelligence
- [webdatatools-rag-mcp](https://github.com/paulet4a-commits/webdatatools-rag-mcp) — Web content for AI & RAG
- [webdatatools-social-mcp](https://github.com/paulet4a-commits/webdatatools-social-mcp) — Search, video & social data
- [webdatatools-dev-mcp](https://github.com/paulet4a-commits/webdatatools-dev-mcp) — Developer, app & research data

## License

MIT
