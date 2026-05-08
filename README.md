# ⚡ Workshop Intel — Transcript Summarizer

A zero-dependency, single-file web app that turns raw workshop transcripts into structured intelligence reports and deep competitive growth analysis — powered by your choice of AI provider.

![Workshop Intel Screenshot](https://placehold.co/900x500/0a0a0f/c8ff00?text=Workshop+Intel)

## What It Does

Upload one or more `.vtt`, `.srt`, or `.txt` transcript files from your workshops and get:

**1. Workshop Intelligence Report** — a 5-section structured summary:

| # | Section | What it extracts |
|---|---------|-----------------|
| 01 | **Summary of Workshop** | Paragraph overview of the session |
| 02–05 | **Details Report** | Tools used, courses being sold, upsell prices, key hook points |

**2. Competitive Growth Report** *(optional second pass)* — a deep strategic analysis including:

- Quantitative intelligence dashboard with threat gauges, radar chart, and bar chart
- 7-dimension competitive breakdown: Hook & Target Audience, Sales & Conversion, Offer & Monetization, Trust & Engagement, AI Tools, Business Moat, Weaknesses & Opportunities
- Competitor strength vs. your opportunity scores per dimension
- Strategic overview and actionable growth playbook

## Quick Start

### Option A — Open Locally
1. Download `index.html`
2. Open it in any browser (double-click or drag into browser)
3. Choose your AI provider and enter your API key
4. Upload your transcript files
5. Click **Generate Workshop Intel**

### Option B — Deploy to GitHub Pages
1. Fork this repo
2. Go to **Settings → Pages → Source → Deploy from branch → main / root**
3. Your app will be live at `https://yourusername.github.io/workshop-summarizer`

### Option C — Any static host
Drop `index.html` onto Netlify, Vercel, or Cloudflare Pages — it works anywhere. No build step needed.

## Supported AI Providers

Choose from 6 providers at runtime — no code changes needed:

| Provider | Model | Cost |
|----------|-------|------|
| **Google Gemini** | gemini-2.5-flash | 🆓 Free · No credit card |
| **OpenRouter** | 100+ models (Llama, Qwen, GPT-4o Mini, and more) | 🆓 Free models available |
| **Claude (Anthropic)** | claude-haiku-4-5 | 💳 Paid · Best quality on long transcripts |
| **Groq** | llama-3.3-70b | 🆓 Free · Ultra fast inference |
| **Mistral AI** | mistral-small-latest | 🆓 Free tier |
| **Cohere** | command-r-plus | 🆓 Free trial key |

## Features

- 🗂 **Multi-file support** — upload multiple transcripts at once; each is labeled as a separate day
- 🔀 **6 AI providers** — switch between Gemini, OpenRouter, Claude, Groq, Mistral, and Cohere in one click
- 📊 **Competitive Growth Report** — optional deep-dive with radar/bar charts, threat gauges, and a strategic playbook
- ⬇️ **Download reports** — export Summary and Details as `.html` files
- 📋 **One-click copy** — copy individual sections or the full report
- 🔑 **Session-safe key storage** — API keys live in `sessionStorage` and clear when the tab closes
- 🎨 **Zero dependencies** — single HTML file, no npm, no build tools
- 📡 **Direct API calls** — no backend, no server required

## Requirements

- A modern browser (Chrome, Firefox, Safari, Edge)
- An API key from any supported provider (see table above — most have free tiers)

## Supported File Formats

| Format | Extension | Notes |
|--------|-----------|-------|
| WebVTT | `.vtt` | Primary format — timestamps stripped automatically |
| SubRip | `.srt` | Works, timestamps stripped |
| Plain text | `.txt` | Works as-is |

## Privacy

Your API key is stored only in `sessionStorage` (cleared when the tab closes) and sent directly to your chosen provider's API. Transcript text is never routed through any intermediary server.

## Customizing the Prompt

Open `index.html` and find the `buildPrompt()` function. Edit the instructions for each section to match your specific use case.

## License

MIT — use freely, modify as needed.

---

Built with ❤️ — supports Google Gemini, OpenRouter, Claude, Groq, Mistral, and Cohere
