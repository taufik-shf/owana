---
name: styling-system
description: Audit and fix CSS to comply with this project's design system — type scale, spacing, media queries, tokens, and layout rules. Use when editing/auditing styles or asked to follow the design system.
---

# Styling Audit

Audit and fix CSS to comply with this project's design system. Invoke when reviewing, editing, or adding component styles.

## Base

`html { font-size: 62.5%; }` — 1rem = 10px. All lengths must use rem (except fixed sizes like logo heights, icon dimensions).

## Type Scale

Major Third (1.25). Only these steps:

| Step | rem | px |
|------|-----|----|
| 0 | `1rem` | 10 |
| 1 | `1.25rem` | 12.5 |
| 2 | `1.5rem` | 15 |
| 3 | `2rem` | 20 |
| 4 | `2.5rem` | 25 |

Body copy, labels, nav links — round to clean steps. No `0.85rem`, `0.93rem`, `1.26rem`, `1.42rem`, `1.92rem` etc.

## Spacing

4px grid: `0.4`, `0.6`, `0.8`, `1.2`, `1.6`, `2`, `2.4` rem. No `0.35`, `0.56`, `0.64`, `0.65`, `1.04`.

## Media Queries

`em` only. Divide px by 10:

| Target | Value |
|--------|-------|
| 639px | `63.9em` |
| 768px | `76.8em` |
| 1024px | `102.4em` |
| 1280px | `128em` |

Desktop-first (`max-width`). Source: `_Docs/DESIGN_GUIDE.md`.

## Tokens

Use CSS vars from `src/styles/global.scss`. Never hardcode hex/rgb. Key vars:

- `--dark`, `--text`, `--text-muted`
- `--bg-warm`, `--bg-card`
- `--forest`, `--forest-2`, `--lime`
- `--border`, `--border-subtle`
- `--font-serif`, `--font-sans`, `--font-mono`

## Layout Defaults

From `_Docs/DESIGN_GUIDE.md`:

- Container: `.wrap` — `min(1120px, calc(100% - 2.5rem))`
- Section padding: `.section` — `5rem 0 6rem` (desktop)
- Card radius: `1rem`
- Pill radius: `999px`

## Typography

| Element | Font | Weight | Extras |
|---------|------|--------|--------|
| h1, h2 | `--font-serif` or Inter | 800 | `letter-spacing: -0.04em` |
| body | Inter | 400 | `line-height: 1.7`, color `var(--text)` |
| labels | `--font-mono` | 400 | uppercase, `letter-spacing: 0.14em` |

## Component Conventions

- `.astro`, PascalCase, scoped `<style>`
- Semantic HTML, ARIA, `alt` on images
- External links: `target="_blank" rel="noreferrer"`
- Props via `interface Props` in frontmatter
- Verify with `bun run build`
