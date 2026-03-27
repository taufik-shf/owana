# Gowana Design Guide

## Brand Feel

Local. Warm. Honest. No corporate polish - we're locals sharing our home.

**Voice**: Direct, curious, slightly dry humor. We're still learning.
**Never**: "breathtaking", "pristine", "untouched paradise", "sustainability"
**Always**: "Go Deeper. Go Wana."

## CSS Variables

```scss
:root {
  /* Dark warm palette */
  --dark: #1a1714;
  --dark-hover: #2d2822;
  --text: #5a544a;
  --text-muted: #8a8278;

  /* Backgrounds */
  --bg-warm: #efe9df;
  --bg-card: #e3ddd3;
  --bg-map: #d9d1c5;

  /* Borders */
  --border-subtle: rgba(26, 23, 20, 0.08);
  --border: rgba(26, 23, 20, 0.12);

  /* Brand greens */
  --forest: #2a5c1a;
  --forest-2: #3d7a22;
  --lime: #6fa82f;
  --lime-light: #a8d060;
}
```

## Typography

- **Headlines**: Inter 800, `letter-spacing: -0.04em`
- **Body**: Inter 400, `line-height: 1.7`, color `--text`
- **Labels**: Space Mono 400, uppercase, `letter-spacing: 0.14em`

## Layout

- **Container**: `min(1120px, calc(100% - 2.5rem))`
- **Section padding**: `5rem 0 6rem`
- **Grid gap**: `3rem` mobile, `4.5rem` desktop
- **Border radius cards**: `1rem`
- **Border radius pills**: `999px`

## Breakpoints

Desktop-first approach. Base styles target desktop (1024px+). Use `max-width` for smaller screens.

| Breakpoint | Target |
|------------|--------|
| Base | Desktop 1024px+ |
| `max-width: 1023px` | Tablet landscape |
| `max-width: 768px` | Tablet / Large mobile |
| `max-width: 639px` | Mobile |

## CSS Approach

**Desktop-first methodology:**
```scss
// Base styles (desktop)
.component {
  display: grid;
  grid-template-columns: 1fr 1fr; // 2-column layout
}

// Tablet and below
@media (max-width: 768px) {
  .component {
    grid-template-columns: 1fr; // Single column
  }
}

// Mobile
@media (max-width: 639px) {
  .component {
    padding: 2rem;
  }
}
```

