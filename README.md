# 北陸 Bridge Navigator

> A strategic business command centre for Japanese SME international expansion — built by a Hokuriku-based trilingual researcher.

---

## What this is

**Hokuriku Bridge Navigator** is an AI-powered strategy tool designed to help Japanese SMEs in the Hokuriku region expand into international markets. It serves as a personal command centre for an independent cross-border marketing consultant operating across Japanese, English, and Chinese.

The tool consolidates a complete business operating system into a single browser-based application — no backend, no database, no installation required.

---

## Features

| Module | Description |
|---|---|
| **Dashboard** | 3-phase business roadmap with live revenue targets and milestone tracking |
| **Task Tracker** | Priority-tagged task management with persistent local storage |
| **Strategy Agent** | Claude-powered AI assistant with full business context baked in — pitch scripts, pricing, Japan market intelligence, cultural frameworks |
| **Knowledge Base** | Six reference cards covering service model, pitch scripts, packages, client protection, tech stack, and Japan pain points |
| **Revenue Model** | Complete pricing table and milestone payment structure across all service tiers |

---

## The business context

This tool is built around a three-phase business model:

**Phase 1 — SME Marketing Retainer** *(active)*
Embedded cultural navigation for Hokuriku manufacturers expanding overseas. Services include English social media content, inbound foreign inquiry handling, product catalogue translation, and international buyer communication.

**Phase 2 — Japan Sourcing Hub** *(building)*
Market intelligence reports for foreign importers sourcing from Japanese manufacturers. Priced at $299–799 per report.

**Phase 3 — Japan Export Intelligence** *(future)*
Scalable B2B subscription product covering export market trends, competitor tracking, and regional supplier dashboards.

---

## Tech stack

- **Frontend** — Vanilla HTML/CSS/JS, single file, zero dependencies
- **AI** — Anthropic Claude API (`claude-sonnet-4-20250514`)
- **Automations** — Designed around n8n workflows (social posting pipeline, email translation pipeline, WhatsApp agent via WATI)
- **Storage** — Browser `localStorage` for task persistence
- **Hosting** — GitHub Pages (this repo)

---

## Setup

### 1. Get an Anthropic API key
Go to [console.anthropic.com](https://console.anthropic.com) → API Keys → Create Key.
New accounts receive free credits. The key format is `sk-ant-...`

### 2. Open the app
Visit the live GitHub Pages URL or open `index.html` directly in any browser.

### 3. Paste your key
Enter your API key in the bar at the top of the interface. It is stored only in your browser's local storage and never sent anywhere except the Anthropic API.

The Strategy Agent, task tracker, knowledge base, and revenue model all work immediately after this.

---

## Automation architecture

The tool references three n8n automation pipelines:

**Social posting pipeline**
```
Monthly cron → Claude API (generate 8 posts) → Google Sheets (log) → LinkedIn + Instagram (publish) → Email summary to client
```

**Email translation pipeline**
```
Gmail trigger (foreign email arrives) → Claude (translate to Japanese) → SME inbox
SME replies in Japanese → Claude (translate to English) → Send to foreign client
```

**WhatsApp agent pipeline**
```
WhatsApp Business API (via WATI) → Claude (classify intent) → Auto-reply / Translate-forward to SME via LINE / Escalate with alert
```

---

## Japan market context

The strategy is designed around 10 structural pain points foreign companies face when doing business with Japanese SMEs:

1. Consensus-driven decision making (nemawashi / ringi)
2. Opaque internal hierarchies
3. Closed keiretsu distribution networks
4. Language gap deeper than translation
5. Extreme quality and customization demands
6. Supplier loyalty obligations (giri)
7. Risk aversion toward new vendors
8. Regulatory complexity (PSE, Food Sanitation Act, METI)
9. Scarcity of bilingual bridge talent
10. Multi-layer distribution price erosion

The consulting model treats these not as obstacles but as the actual operating system of Japanese commerce — and positions the consultant as someone who genuinely understands both sides.

---

## Service pricing reference

| Service | Price | Type |
|---|---|---|
| Trust Package | ¥80,000–150,000 | One-time per client |
| Communication Bridge Retainer | ¥60,000–100,000/month | Monthly |
| Managed Inquiry Handling | ¥20,000–30,000/month | Add-on |
| Foreign Buyer Advisory | ¥30,000–80,000 | Per engagement |
| Shokai (referral) introductions | ¥50,000–100,000 | Per introduction |
| Japan Sourcing Hub report | $299–799 | Per report |

Estimated annual revenue from 3 clients: **¥3,780,000**

---

## Competitive advantage

- Trilingual: Japanese · English · Chinese
- Physically embedded in Hokuriku craft manufacturing region
- Graduate researcher credibility — opens doors commercial agents cannot
- Deep understanding of both Japanese indirectness and foreign impatience
- Cultural translation, not just language translation

---

## License

Personal use. Not intended for redistribution.

---

*Built with Claude · Powered by n8n · Deployed on GitHub Pages*
