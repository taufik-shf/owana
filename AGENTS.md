# Gowana - Astro Project

## Build Commands

```bash
npm run dev          # or: bun run dev
npm run build        # or: bun run build
npm run preview      # or: bun run preview
npm run astro        # Astro CLI
```

**Note:** No test/linter configured yet. Add vitest/eslint/prettier as needed.

## Brand Context

- **What we do:** Local tour operation in Sulawesi Tengah, Indonesia. Small groups into off-itinerary places (Togean Islands, Lore Lindu, Bada Valley, Sombori).
- **Who we are:** Locals. Not corporate. Conservation funded directly from tour revenue.
- **Name:** "Gowana" from *wana* (forest). "Go Wana" = go deeper.
- **Amateur ethos:** From Latin *amare* (to love). We do this out of love, not for polish. Never means cutting corners on safety.

### Brand Voice

| Register | Description |
|----------|-------------|
| Honest | Say what's true, including uncomfortable parts (rough roads, late boats) |
| Curious | We're still learning. We ask questions back. |
| Local | Talk about Sulawesi like home. Specific. Personal. No travel brochure language. |
| Playful, grounded | Dry wit exists. Funny because honest, not performing. |

**Never say:** "breathtaking", "pristine", "untouched paradise", "sustainability", corporate tour language.

**Always say:** "Go Deeper. Go Wana.", "Still learning. Always local.", "Nobody talks about this place. We live here."

### Color Palette

| Name | Hex | Role |
|------|-----|------|
| Ink | #1C1C18 | Body text |
| Forest | #2A5C1A | Primary brand |
| Lime | #6FA82F | Main accent |
| Cream | #F2EDE4 | Base background |
| White | #FAF7F2 | Cards, surfaces |
| Rust | #8B4A2A | Earthy accent (sparingly) |

Warm, organic, slightly aged. No cold grays or pure whites.

### Typography

- **DM Serif Display** - Headlines, pull quotes. Warm, editorial.
- **Inter** - Body copy, UI text. 400 regular, 700+ emphasis.
- **Space Mono** - Labels, coordinates, metadata. Uppercase, wide spacing. 9-11px.

## Code Style

Standard Astro conventions apply:

- `.astro` files, PascalCase names (`Welcome.astro`, `Layout.astro`)
- Frontmatter (`---`) for imports/logic, `<style>` for scoped CSS
- Strict TypeScript (`astro/tsconfigs/strict`)
- Tabs for indentation, single quotes
- Relative imports with `.astro` extension: `import X from '../components/X.astro'`
- Semantic HTML, `alt` on images, kebab-case attributes

### File Structure

```
src/
├── assets/       # Static assets
├── components/   # Reusable Astro components
├── layouts/      # Page layouts
└── pages/        # File-based routing
```

### Component Pattern

```astro
---
interface Props {
  title: string;
}
const { title } = Astro.props;
---

<div class="container">
  <h1>{title}</h1>
</div>

<style>
  .container { /* scoped */ }
</style>
```

## Git Conventions

Conventional commits: `feat:`, `fix:`, `docs:`, `refactor:`. Keep atomic.
