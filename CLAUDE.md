# website/ — CLAUDE.md

Marketing website for **The Bull** (`www.the-bull.ai`).
Static HTML, no build step. Edit files and push — GitHub Pages deploys automatically.

## Repo
- GitHub: `https://github.com/Ofia/the-bull.ai`
- Hosted: GitHub Pages → `www.the-bull.ai`
- Local: `C:\Users\ofir\Desktop\The Bull Marketing\website\`

## Deploy
```bash
# from inside The Bull Marketing\website\
git add .
git commit -m "..."
git push origin main
```

## Structure
```
index.html          ← homepage
privacy.html
favicon.png
CNAME               ← www.the-bull.ai
contracts/          ← /contracts product page (payment.html, pricing.html)
properties/         ← /properties product page
salon/              ← /salon product page (Coming Soon)
developer/          ← /developer product page (Coming Soon)
chat-api/           ← Vercel serverless function (AI chat proxy)
  api/chat.js       ← POST {messages} → Claude sonnet-4-6 → {reply}
  vercel.json
```

## Chat section (added 2026-07-29)

A chat box sits between the hero and the mockups carousel in `index.html`.

- **Frontend:** plain JS inside `index.html` — no framework, no extra files
- **API:** `https://the-bull-chat-api.vercel.app/api/chat` — Vercel serverless function in `chat-api/`
- **Vercel project:** `the-bull-chat-api` under `ofias-projects`, linked to `Ofia/the-bull.ai` repo, root directory `chat-api`
- **Model:** `claude-sonnet-4-6`, system prompt baked into `chat-api/api/chat.js`
- **Env var:** `ANTHROPIC_API_KEY` set in Vercel dashboard (Production only)
- **Deploy flow:** push to `main` → GitHub Pages updates the site AND Vercel rebuilds the API
- **CORS:** currently open (`*`) — restrict to `the-bull.ai` before launch

## Design system
- Background: `#ffffff` / `#f5f5f3`
- Primary text: `#1a1a1a`
- Muted: `#8a8a85`
- Accent: `#b38600` (brand gold) — matches `--accent` in `index.html` and `..\Style\style_ui.md`
- Font: Inter + JetBrains Mono (Google Fonts)
- Style: clean, minimal, professional SaaS
