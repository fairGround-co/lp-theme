# Refinement notes — lp-theme 0.1.x draft values (issue #2)

*The 0.1.0 seed was extracted from LotPlanner and mapped onto core token
contract v0. Everything below needs a decision pass — per Kyle, worked in this
repo with an agent that has the LP app context, one value at a time, against
`docs/lookbook.html`.*

## Flagged decisions

1. **Dark mode is entirely invented.** LotPlanner ships light-only; the current
   dark block follows the base system's surface-pops-dark pattern in a
   navy-cast charcoal. Needs a real design pass (or a decision that LP products
   simply pin light until one happens).
2. **`--accent` AA question.** The seed uses the brand teal (`#19aec3`) with
   white `--on-accent`, which fails AA on large fills. The app itself uses teal
   for links / borders / selection — not fills. Alternatives: teal-dark
   (`#128fa1`) as the fill accent, or navy buttons with teal kept for
   interaction cues.
3. **Proposed (not sourced) values:** `--match` (navy-light), `--commit`
   (navy), all three `--scope-*` colors, `--status-caution`, `--surface-3`,
   `--border-strong`, `--overlay`.
4. **Categorical mapping.** Slots 1–7 carry the chart-contrast lot palette;
   8–12 stay on the neutral reference. The pale tint palette and the
   shared-hue, pattern-differentiated pairs stay app-side as domain aliases
   onto slots — confirm that split.
5. **No voice doc.** `nwae-theme/docs/voice.md` is the model; LP's voice
   ("confident, not loud") should get the same treatment.
6. **Fonts.** The theme names DM Sans / Playfair Display / JetBrains Mono;
   decide whether files self-host via `lp-brand-assets` or stay app-loaded.
7. **Geometry non-overrides.** Space/radius/motion stay on the contract scale
   (adapt-to-the-base, design-system DECISIONS #18) — LP's slightly different
   radii/timings were deliberately not carried. Confirm.
