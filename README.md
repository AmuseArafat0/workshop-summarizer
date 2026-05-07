# ⚡ Workshop Intel — Transcript Summarizer

A zero-dependency, single-file web app that turns raw workshop VTT transcripts into structured 5-section intelligence reports using the Claude API.

![Workshop Intel Screenshot](https://placehold.co/900x500/0a0a0f/c8ff00?text=Workshop+Intel)

## What It Does

Upload one or more `.vtt` transcript files from your workshops and get an instant report covering:

| # | Section | What it extracts |
|---|---------|-----------------|
| 01 | **What They Taught** | Core lessons, concepts, workflows, skills |
| 02 | **Tools Used** | Every software, platform, API, and service mentioned |
| 03 | **Courses Being Sold** | Programs, memberships, training offers described |
| 04 | **Upsell Prices** | Exact prices, tiers, discounts, payment plans |
| 05 | **Important Hook Points** | Key sales hooks, pain points, urgency tactics |

## Quick Start

### Option A — Open Locally
1. Download `index.html`
2. Open it in any browser (double-click or drag into browser)
3. Enter your Anthropic API key
4. Upload your `.vtt` files
5. Click **Generate Workshop Intel**

### Option B — Deploy to GitHub Pages
1. Fork this repo
2. Go to **Settings → Pages → Source → Deploy from branch → main / root**
3. Your app will be live at `https://yourusername.github.io/workshop-summarizer`

### Option C — Any static host
Drop `index.html` onto Netlify, Vercel, Cloudflare Pages — it works anywhere. No build step needed.

## Requirements

- A modern browser (Chrome, Firefox, Safari, Edge)
- A **free** [Google Gemini API key](https://aistudio.google.com/apikey) — no credit card needed, just sign in with your Google account
- Workshop transcripts in `.vtt`, `.srt`, or `.txt` format

> **Free tier:** Gemini 2.5 Flash gives you 1,500 requests/day. More than enough for summarizing workshops.

## Features

- 🗂 **Multi-file support** — upload multiple workshop transcripts at once
- 🔑 **Session-safe key storage** — API key stays in `sessionStorage`, never sent anywhere except the Anthropic API
- 📋 **One-click copy** — copy individual sections or the entire report
- 🎨 **Zero dependencies** — single HTML file, no npm, no build tools
- 📡 **Direct API calls** — no backend required

## Privacy

Your API key is stored only in `sessionStorage` (cleared when the tab closes). Transcript text is sent directly to the Anthropic API and is subject to [Anthropic's privacy policy](https://www.anthropic.com/privacy).

## Supported File Formats

| Format | Extension | Notes |
|--------|-----------|-------|
| WebVTT | `.vtt` | Primary format — timestamps stripped automatically |
| SubRip | `.srt` | Works, timestamps stripped |
| Plain text | `.txt` | Works as-is |

## Customizing the Prompt

Open `index.html` and find the `buildPrompt()` function (~line 220). Edit the instructions for each of the 5 sections to match your specific use case.

## License

MIT — use freely, modify as needed.

---

Built with ❤️ using the [Google Gemini API](https://aistudio.google.com) — free, no credit card required
