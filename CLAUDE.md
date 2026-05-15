# Ramenwasseropleiding.be

Statische one-pager website voor de ramenwasser-opleiding van Thomas Boone (Goldmund Puur Eau).

## Stack

Pure HTML + CSS + vanilla JS — geen build step, geen framework. Open `index.html` rechtstreeks in de browser of serveer met een willekeurige static server (`python -m http.server`, `npx serve`, etc.).

## Bestandsstructuur

```
/
├── index.html       Alle markup en inline scripts
├── styles.css       Alle styling (custom properties bovenaan)
└── assets/
    └── thomas.png   Portretfoto (al opgehelderd: +brightness +contrast +saturation)
```

## Design tokens (CSS custom properties in styles.css)

```css
--cream:  #FFF3DC   /* page background */
--paper:  #FFFBF2   /* cards on cream */
--ink:    #0E2433   /* primary text + dark sections */
--sky:    #3FB4E5   /* clean-window blue */
--sun:    #FFC93C   /* accent + price card */
--coral:  #FF6B57   /* primary CTA */
--coral-2:#E64A36   /* CTA shadow + accent text */
--leaf:   #3FAE6C
```

## Typografie

Google Fonts:
- **Bricolage Grotesque** — display (h1–h4, prijzen, buttons)
- **DM Sans** — body
- **JetBrains Mono** — kickers, kleine labels, footer

## Secties (in volgorde, allemaal in `index.html`)

1. **Intro-overlay** (`#intro`) — vuile glaslaag (SVG met waterdruppels & smudges) wordt door een squeegee weggeveegd via clip-path. Skip-knop rechtsonder. Verdwijnt na ~2.2s.
2. **Nav** — sticky, met logo (inline SVG wordmark).
3. **Hero** — H1 + lead + CTA's + meta-stats links; rechts een SVG-visual van een raam dat halverwege wordt gewassen (dirty side / clean side gescheiden door een diagonale squeegee). Drie stickers eromheen.
4. **Marquee** — horizontale auto-scrollende USP-balk.
5. **Programma** (`#programma`) — 8 kaarten in een auto-grid met chunky drop-shadow (`box-shadow: 6px 6px 0 var(--ink)`).
6. **Inclusief + Prijs** (`#prijs`) — donkere sectie, 2-koloms grid met inclusief-items + gele prijskaart (€690).
7. **Facts** — coral horizontale band met 4 cijfers.
8. **Thomas** (`#thomas`) — foto met badge sticker + bio + quote. Foto en badge zitten in `.thomas-photo-wrap` (badge mag buiten de fotokader uitsteken).
9. **Inschrijven** (`#inschrijven`) — contact info + inschrijvingsformulier. Form is front-end only: success-state toont na submit, geen backend.
10. **Footer** — donker, met BTW-nummer (BE 0642.913.129) en bedrijfsinfo (Goldmund Puur Eau).

## TODO / open punten

- Inschrijvingsformulier koppelen aan een echte mailservice (Formspree, Resend, Netlify Forms, …).
- Echte data voor eerstvolgende opleidingsdagen toevoegen.
- Eventueel extra foto's of een korte video van Thomas in actie.
- SEO: Open Graph / Twitter Card meta tags, structured data (Course schema).
- Favicon op basis van de logo-SVG.

## Conventies

- Canonieke HTML: elke non-void tag expliciet sluiten, attributen tussen dubbele quotes. (Dit maakt het bestand makkelijker direct te bewerken.)
- Geen em-dashes (—) in de copy — bewust verwijderd op verzoek.
- Mobile breakpoint op 1000px (hero wordt single-column).
