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
```

## Design system
- Background: `#ffffff` / `#f5f5f3`
- Primary text: `#1a1a1a`
- Muted: `#8a8a85`
- Accent: `#b38600` (brand gold) — matches `--accent` in `index.html` and `..\Style\style_ui.md`
- Font: Inter + JetBrains Mono (Google Fonts)
- Style: clean, minimal, professional SaaS
