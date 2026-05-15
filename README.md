# Ramenwasseropleiding.be

Static one-pager voor de ramenwasser-opleiding van Thomas Boone.

Live: [ramenwasseropleiding.be](https://ramenwasseropleiding.be)

## Lokaal draaien

```bash
# één van deze
python -m http.server 8000
npx serve .
```

Geen build step. Open `index.html`.

## Deployen

Werkt op elke static host (Netlify, Vercel, Cloudflare Pages, GitHub Pages).
Geen build-commando nodig — gewoon de root van de repo als output directory.

## Verder bewerken

Zie [`CLAUDE.md`](./CLAUDE.md) voor de stack, design tokens en sectie-opbouw.
