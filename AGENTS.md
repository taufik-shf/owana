# Gowana - Astro Project

## Build Commands
```bash
bun run build        # Build for production
bun run preview      # Preview production build
```
No lint/test scripts; use Astro VSCode extension.

## Brand Context
Local tour in Sulawesi Tengah. Small groups, off-itinerary. Not corporate.
**Voice**: Honest, curious, local. Dry wit. We're still learning.
**Never**: "breathtaking", "pristine", "untouched paradise", "sustainability"

## Design System

When asked to follow the design system (or when editing/auditing CSS), load the `styling-system` skill via the Skill tool. It covers type scale, spacing, media queries, tokens, and layout rules.

## Code Style
- `.astro` files, PascalCase component names
- Frontmatter `---` for logic; scoped `<style>` blocks
- 2-space indentation, single quotes
- Semantic HTML, `alt` on images, ARIA attributes
- TypeScript strict mode (`astro/tsconfigs/strict`), explicit prop types
- Minimal client-side JS; vanilla JS at bottom of file
- Use design tokens (`var(--dark)`); desktop-first responsive CSS

## Component Patterns
- Props via `interface Props` in frontmatter
- Wrap pages in `Layout.astro`
- Import assets via `import img from '../assets/...'`
- External links open in new tab with `rel="noreferrer"`

## Testing & Validation
- No test suite; add with Vitest (`astro/testing`): `npx vitest run path/to/test.ts`
- Build must succeed: `bun run build`
- Manual checks: responsive design, hover/focus

## Git Conventions
- Conventional commits: `feat:`, `fix:`, `docs:`, `refactor:`
- Small focused commits, no secrets/env files.

## Agent Guidelines
1. Run `bun run build` after changes.
2. Preserve code style (2 spaces, single quotes, PascalCase).
3. Maintain semantic HTML and accessibility.
4. Use design tokens for colors and fonts.
5. Keep dependencies minimal (Astro + sass-embedded only).
6. Check TypeScript strictness; props must have explicit interfaces.

## Project Structure
```
src/
  components/    # Reusable .astro components (PascalCase)
  layouts/       # Layout wrappers (Layout.astro)
  pages/         # Route pages (index.astro, etc.)
  assets/        # Images and static assets
public/          # Static files served as-is
```

## Environment
- Node >= 22.12.0
- Bun as package manager
- Astro 6.x
