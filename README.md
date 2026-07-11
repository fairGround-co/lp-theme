# lp-theme

**→ [Open the lookbook](https://fairground-co.github.io/lp-theme/)** — this
theme rendered live: every contract token with its resolved Leadership
Properties value, all core primitives, light/dark, a neutral ⇄ lp switcher, and
density. Source: [docs/lookbook.html](docs/lookbook.html).

> **0.1.x is a draft-quality seed** extracted from LotPlanner so app work can
> start; the value refinement pass is issue #2 (flags in
> [docs/refinement-notes.md](docs/refinement-notes.md)) — notably, the dark
> mode is drafted (LotPlanner ships light-only today).

Brand **token values only** for this org — all palettes/variants, consumed with
`@fairground-co/core`'s token contract. Invariant: no components, no widget code,
no licensed assets (those live in the private `<org>-brand-assets` repo). Always
safe to publish.

Published as `@fairground-co/lp-theme` (GitHub Packages). See
`fairground-co/design-system` DECISIONS.md #10.

## Usage

```js
import '@fairground-co/core/styles.css';   // the contract + neutral reference
import '@fairground-co/lp-theme/styles.css'; // brand values (must load AFTER core)
```

```html
<html data-brand="lp" data-theme="light">
```

Fonts are named here (DM Sans, Playfair Display, JetBrains Mono) but not
shipped — apps load them (or a future `lp-brand-assets` hosts them). Lot-type
domain aliases (echelon/estate/…) live app-side, mapped onto `--cat-*` slots.

## Regenerating the lookbook

```bash
node <design-system>/packages/core/scripts/build-lookbook.mjs \
  --brand lp --title "Leadership Properties" \
  --package "@fairground-co/lp-theme@<version>" \
  --theme-css ./styles.css \
  --out ./docs/lookbook.html \
  --note "0.1.x values are a draft-quality seed; refinement is issue #2."
```
