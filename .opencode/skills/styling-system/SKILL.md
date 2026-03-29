---
name: styling-system
description: Audit and fix CSS to comply with this project's design system — type scale, spacing, media queries, tokens, and layout rules. Use when editing/auditing styles or asked to follow the design system.
---

# Styling Audit

Audit and fix CSS to comply with this project's design system. Invoke when reviewing, editing, or adding component styles.

## Base

`html { font-size: 62.5%; }` — 1rem = 10px. All lengths must use rem (except fixed sizes like logo heights, icon dimensions).

## Type Scale

Major Third (1.25 ratio). Use these CSS variables from `global.scss`:

| Token | rem | px |
|-------|-----|----|
| `--text-xs` | `0.64rem` | 6.4 |
| `--text-sm` | `0.8rem` | 8 |
| `--text-base` | `1rem` | 10 |
| `--text-md` | `1.25rem` | 12.5 |
| `--text-lg` | `1.5625rem` | 15.6 |
| `--text-xl` | `1.953rem` | 19.5 |
| `--text-2xl` | `2.441rem` | 24.4 |
| `--text-3xl` | `3.052rem` | 30.5 |
| `--text-4xl` | `3.815rem` | 38.2 |
| `--text-5xl` | `4.768rem` | 47.7 |

Body copy, labels, nav links — use tokens. No `0.85rem`, `0.93rem`, `1.26rem` etc.

**Do not use `clamp()` for font sizes.** Use a single token for each breakpoint. Override in media queries if needed.

## Spacing

4px grid: `0.4`, `0.6`, `0.8`, `1.2`, `1.6`, `2`, `2.4` rem. No `0.35`, `0.56`, `0.64`, `0.65`, `1.04`.

## Media Queries

`em` only. Divide px by 16 (browser default):

| Token | Target | Value |
|-------|--------|-------|
| `$bp-sm` | 768px | `48em` |
| `$bp-md` | 1229px | `76.8em` |
| `$bp-lg` | 1638px | `102.4em` |
| `$bp-xl` | 2048px | `128em` |

Desktop-first (`max-width`). Define in `global.scss`.

## Tokens

Use CSS vars from `src/styles/global.scss`. Never hardcode hex/rgb.

**Colors:**
- `--dark`, `--text`, `--text-muted`
- `--bg-warm`, `--bg-card`
- `--forest`, `--forest-2`, `--lime`
- `--border`, `--border-subtle`

**Fonts:**
- `--font-serif`, `--font-sans`, `--font-mono`

**Type scale:**
- `--text-xs` through `--text-5xl` (see Type Scale section)

## Layout Defaults

- Container wide: `.wrap-wide` — `min(1120px, calc(100% - 2.5rem))`
- Container narrow: `.wrap` — `min(960px, calc(100% - 2.5rem))`
- Section padding: `.section` — `4.5rem 0` mobile, `6rem 0` desktop
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
