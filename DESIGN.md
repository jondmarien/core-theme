# Design system

## Color (OKLCH-first)

The palette below is the canonical source.

### Tavern (primary surface)

| Token | OKLCH | Approx hex | Use |
|---|---|---|---|
| `--tavern-pitch` | `oklch(0.12 0.015 60)` | ~#0d0805 | Page background. Tinted toward warm hue 60 deg (amber). |
| `--tavern-ink` | `oklch(0.18 0.020 60)` | ~#1a120a | Card / section backgrounds. |
| `--tavern-stone` | `oklch(0.28 0.025 60)` | ~#2e2218 | Raised surfaces, modal backgrounds. |
| `--tavern-leather` | `oklch(0.42 0.080 50)` | ~#5a3e26 | Borders, dividers, low-emphasis accents. |
| `--tavern-fire` | `oklch(0.72 0.18 55)` | ~#e0a168 | Primary action color (warmer than amber-gold). |
| `--tavern-gold` | `oklch(0.86 0.16 95)` | ~#e8c860 | Hero accents, scores, earned feel. **<=10% of any surface.** |
| `--tavern-parchment` | `oklch(0.92 0.04 80)` | ~#ebdbb8 | Body text on dark surfaces. |

### Functional

| Token | OKLCH | Use |
|---|---|---|
| `--success` | `oklch(0.68 0.16 145)` | Solved, correct flag, healthy status. Muted forest green. |
| `--warning` | `oklch(0.74 0.16 70)` | Hint cost prompts, time-limited indicators. |
| `--danger` | `oklch(0.62 0.20 25)` | Wrong flag, rate-limit hits, errors. |
| `--info` | `oklch(0.78 0.10 240)` | Hint-revealed content, neutral notifications. |

### Forbidden colours

- `#000`, `#fff`, `#000000`, `#ffffff`.
- Pure red `oklch(0.6 0.25 30)` and pure blue `oklch(0.5 0.2 250)`.
- Anything with chroma > 0.18 at lightness > 0.7.

### Color strategy declaration

This palette is **Committed**: one saturated color (`--tavern-fire`/`--tavern-gold`)
carries 30 to 60% of the visual identity.

## Typography

### Families

| Token | Family | Use |
|---|---|---|
| `--font-display` | `"Cormorant Garamond", "Quintessential", serif` | Page titles, hero headlines, major section headers |
| `--font-body` | `"Crimson Pro", "EB Garamond", Georgia, serif` | Body text |
| `--font-flavor` | `"MedievalSharp", cursive` | Ornamental only |
| `--font-mono` | `"JetBrains Mono", "Fira Code", monospace` | Code, flags, API keys, terminal output |

### Scale

Use a 1.333 ratio.

| Token | Size | Use |
|---|---|---|
| text-xs | 0.75rem | Captions |
| text-sm | 0.875rem | Microcopy |
| text-base | 1rem | Body text minimum |
| text-lg | 1.125rem | Larger body |
| text-xl | 1.5rem | H4 |
| text-2xl | 2rem | H3 |
| text-3xl | 2.66rem | H2 |
| text-4xl | 3.5rem | H1 |
| text-5xl | 4.65rem | Hero only |

Body line-length: clamp(45ch, 65ch, 75ch).

## Spacing rhythm

- `space-y-2` dense rows
- `space-y-4` paragraphs
- `space-y-8` subsections
- `space-y-16` major sections
- `space-y-24` top-level regions

## Layout

- No nested cards.
- No default container wrappers unless needed.
- No 3-up feature-card grids.
- Max content width: 65rem (`max-w-5xl`).

## Motion

- Exponential ease-out curves only.
- No bounces or elastic effects.
- Animate `transform` and `opacity` only.
- 200ms hover, 400ms page reveal, 800ms narrative reveal.

## Absolute bans

- Side-stripe borders.
- Gradient text.
- Glassmorphism as default.
- Hero-metric templates.
- Identical card grids.
- Modal-first interactions when inline is possible.
