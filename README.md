# Marketing AI Lab 🧠

A modular marketing AI toolkit built for SEA go-to-market teams.

Each agent automates a specific marketing research or analysis task — so teams make faster, better-informed decisions without manual grunt work.

---

## Agents

### 🔍 Agent 01 — Competitor Intelligence System

Automates end-to-end competitor research: from raw web scraping to strategic synthesis.

**Stack:** Python 3.9 · OpenRouter · Qwen3 · BeautifulSoup · n8n  
**Input:** Competitor URL  
**Output:** Markdown report + JSON for n8n automation  
**Repo:** Private — architecture and sample output available on request

#### Section 1 — Data Extraction

| # | Agent | What it does |
|---|-------|-------------|
| 01a | `landing_page_parser` | Extracts homepage messaging and value proposition |
| 01b | `pricing_extractor` | Decodes pricing tiers and upsell structure |
| 01c | `product_features_evaluator` | Catalogs product capabilities |
| 01d | `social_media_brand_tracker` | Tracks competitor social content and tone |
| 01e | `social_media_community_listener` | *(coming soon)* |
| 01f | `platform_review_listener` | Scrapes G2 / Capterra / Trustpilot reviews |
| 01g | `data_cleaner_and_tokenizer` | Strips HTML noise, prepares text for analysis |
| 01h | `icp_identifier` | Synthesizes competitor ICP from extraction agents |
| 01i | `pain_point_identifier` | Identifies customer pain points from reviews + content |

#### Section 2 — Strategy Analysis

| # | Agent | What it does |
|---|-------|-------------|
| 01j | `icp_identifier` | Maps optimal ICP for your company vs competitor |
| 01k | `swot_analyzer` | Head-to-head SWOT analysis |
| 01l | `brand_positioning_strategist` | Crafts differentiated positioning |
| 01m | `gtm_orchestrator` | Builds full GTM plan |
| 01n | `demand_gen_builder` | Builds demand generation campaigns |

#### Section 3 — Synthesis

| # | Agent | What it does |
|---|-------|-------------|
| 01o | `report_markdown_architect` | Compiles all outputs into executive report (.md) |
| 01p | `json_schema_validator` | Converts report to structured JSON for n8n |

---

### 🎯 Agent 02 — Outreach Agent

Identifies and qualifies B2B leads, then routes them to automated outreach.

#### 02a — Wellfound Lead Sourcing & Intent Scoring ✅

Scores B2B leads from Wellfound using a 3-phase AI intent model.

| Phase | Signal | Logic |
|-------|--------|-------|
| A — Industry fit | Company description | HR/SaaS/Productivity = 40pts · Other tech = 25pts · Else = 10pts |
| B — Stage multiplier | Employee size | 11–50 = 1.0x · 1–10 = 0.9x · 51–100 = 0.8x · 101–200 = 0.6x · 200+ = 0.3x |
| C — Heat score | Location + role type | SEA + commercial = +50 · APAC + commercial = +35 · SEA + non-commercial = +20 · APAC + non-commercial = +10 |

**Stack:** Google Sheets · Google Apps Script · Gemini 2.5 Flash  
**Input:** Wellfound company + job data (weekly scrape)  
**Output:** Intent score 0–100 per company, written to Google Sheets  
**Docs:** [agents/02a-wellfound-intent-scoring/README.md](./agents/02a-wellfound-intent-scoring/README.md)

#### 02b — Multi-source Lead Scraping *(coming soon)*
Extend sourcing to LinkedIn, ProductHunt, and Crunchbase with unified scoring.

#### 02c — Outreach Message Generation *(coming soon)*
Auto-generate personalised outreach messages for qualified leads.

---

## Roadmap

- [x] Agent 01 — Competitor Intelligence System (16 sub-agents)
- [ ] Agent 01e — Social Media Community Listener
- [x] Agent 02a — Wellfound Lead Sourcing & Intent Scoring
- [ ] Agent 02b — Multi-source Lead Scraping
- [ ] Agent 02c — Outreach Message Generation
- [ ] Agent 03 — Content Strategist Agent
- [ ] Agent 04 — Growth Experiment Tracker

---

## About

Built by **Intan Khatulistiwa** — growth marketer and consultant focused on SEA go-to-market strategy.

All agents built hands-on: architecture design, implementation, and GitHub deployment.
