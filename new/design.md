# Design: grmv8.ru, личный сайт Александра Громова (тестовая копия /new/)

The locked system. Every Hallmark run reads this first and pages share it. Change it on purpose; the file is the rule.

## System
- Genre: editorial
- Shape of the first page: Long Document with figures (hero Stage); the story and posts are Long Document, the blog index an Index with a Banner hero, /raspakovka/ an Offer with a Counter hero
- Theme: brand (the grmv8 navy and gold read from the live site), vibe: "the night edition of a broadsheet"
- Axes: dark/roman-serif/warm · posture: committed (the navy carries every surface; gold stays a signal)

## Tokens
`tokens.css` is the source of truth. The roles:
```css
:root {
  --color-paper: oklch(15.3% 0.029 269);  --color-paper-2: oklch(18.6% 0.038 267);  --color-paper-3: oklch(22% 0.044 268);
  --color-ink: oklch(95.5% 0.011 265);  --color-ink-2: oklch(87% 0.018 265);  --color-muted: oklch(74% 0.032 268);  --color-rule: oklch(28% 0.04 268);
  --color-accent: oklch(74.3% 0.117 90);  --color-accent-ink: oklch(18.7% 0.018 92);  --color-focus: oklch(80% 0.14 88);
  --font-display: "Piazzolla", ui-serif, Georgia, serif;  --font-body: "Manrope", ui-sans-serif, system-ui, sans-serif;  --font-outlier: "Unbounded" (the ∞ grmv8 wordmark only);
  --radius-card: 2px;  --radius-pill: 2px;  --rule-hair: 1px;  --shadow-card: the reading widget only;
}
```
The spacing scale, the type scale, the easings and the durations are the scaffold's and live in `tokens.css`.

## Type
- Piazzolla 400 for every head, the figures, the lead paragraph of a section and the article prose (1.1875rem, line-height 1.72, 65ch).
- Manrope 400 for reading on the landing pages, 700 for controls, lead-ins and labels. Unbounded 500 only in the wordmark.
- Three weights in all: 400, 500 (wordmark), 700. Sentence case everywhere, no tracked capitals, no mono.

## Controls
- Primary: gold fill, `--color-accent-ink` text, 48px tall, 2px radius. One per page: «Написать в Telegram» on /, «Написать @grmv8» in the closing band of the documents, «Забронировать слот» on /raspakovka/.
- Secondary: outlined in `--color-rule-2`, same height; gold border on hover.

## Surfaces
- Depth is a lightness step paper > paper-2 > paper-3. Hairlines part rows, timelines and figures; a gold hairline marks a quote and the aside offers. No glass, glow, gradients or cards inside cards.

## Motion
- Character: still. Hover is one colour step; the reading widget fades in; reduced motion ends everything at once.

## Content rules for this site
- Copy is the owner's (`copy: verbatim`): texts, figures and links carried over as found; only glued arrows and middle dots were taken out, and labels over heads moved under them.
- Test copy: `noindex, nofollow`, no canonical, no Yandex.Metrika; internal links stay inside /new/; images load from the root /img/ by absolute path.

## Exports
`tokens.css`, `base.css`, `site.css` in this folder.
