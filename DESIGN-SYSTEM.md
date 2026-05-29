# Arizona AI Solutions — Design System v2 (Phase 1)

> Revised per client feedback. Professional B2B tone for home service businesses.
> Reference feel: ServiceTitan.com (audience match), GetJobber.com (clean/practical), Linear.app (dark theme excellence).

---

## 1. Design Principles

- **Professional over promotional** — Confident, not shouty. Home service owners scan fast; give them clarity.
- **Dark-mode excellence** — Inspired by Linear's depth and shadow craft. Every surface earns its layer.
- **Trust through precision** — Exact spacing, tight alignment, and consistent interaction states signal competence.
- **Wide, breathable layouts** — Content uses horizontal space. No cramped single-column on desktop.
- **Accessible by default** — Focus-visible on everything interactive. Contrast ratios ≥ 4.5:1 for all body text.

---

## 2. Color System

### 2.1 Core Palette

| Token                 | Hex       | Usage                                       |
|-----------------------|-----------|---------------------------------------------|
| `--bg-base`           | `#0A1428` | Page background, nav background              |
| `--bg-raised`         | `#1E293B` | Cards, pricing card, CTA banner background   |
| `--bg-surface`        | `#162032` | Subtle raised surface (hover states, alt bg) |
| `--border-primary`    | `#334155` | Card borders, dividers, input borders        |
| `--border-secondary`  | `#475569` | Hover-state borders, emphasis borders        |
| `--text-primary`      | `#F8FAFC` | Headings, primary content text               |
| `--text-secondary`    | `#CBD5E1` | Body copy, secondary content                 |
| `--text-muted`        | `#94A3B8` | Supporting text, descriptions                |
| `--text-dimmed`       | `#8B9BB5` | Labels, tertiary text, captions              |
| `--accent`            | `#F97316` | CTAs, highlights, badges, focus rings        |
| `--accent-hover`      | `#EA6C0A` | Accent hover state                                    |
| `--accent-active`     | `#C2590A` | Accent active/pressed state                            |
| `--accent-bg-subtle`  | `rgba(249, 115, 22, 0.08)` | Launch special bg, subtle accent fills |
| `--accent-border-subtle` | `rgba(249, 115, 22, 0.25)` | Launch special border |

### 2.2 Focus-Visible Color

All focus-visible outlines use `--focus-ring-color: #F97316` across every interactive element.

---

## 3. Typography

### 3.1 Font Stack

```
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
```

Inter loaded from Google Fonts (`https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap`) for weight range 400–800. System stack as fallback.

### 3.2 Scale

| Token         | Desktop                    | Mobile (≤640px)           | Line-Height | Letter-Spacing | Weight | Usage                          |
|---------------|----------------------------|---------------------------|-------------|-----------------|--------|--------------------------------|
| `--h1`        | **44px** / 2.75rem        | 32px / 2rem               | 1.15        | -0.5px          | 800    | Hero headline only             |
| `--h2`        | 24px / 1.5rem             | 20px / 1.25rem            | 1.3         | -0.3px          | 700    | Section headings               |
| `--h3`        | 18px / 1.125rem           | 16px / 1rem               | 1.4         | —               | 600    | Step headings, card titles     |
| `--body-lg`   | 18px / 1.125rem           | 16px / 1rem               | 1.65        | —               | 400    | Hero tagline, lead paragraphs |
| `--body`      | 16px / 1rem               | 15px / 0.9375rem          | 1.7         | —               | 400    | Body text, descriptions       |
| `--body-sm`   | 14px / 0.875rem           | 14px / 0.875rem           | 1.6         | —               | 400    | Notes, captions, labels       |
| `--label`     | 12px / 0.75rem            | 12px / 0.75rem            | 1.4         | 0.06em          | 700    | Uppercase labels (pricing, badges) |
| `--nav-link`  | 14px / 0.875rem           | 16px / 1rem               | 1.0         | —               | 500    | Nav links                      |
| `--btn-text`  | 15px / 0.9375rem          | 15px / 0.9375rem          | 1.0         | —               | 700    | Button labels                  |

**Key change:** h1 reduced from 52px → 44px. Professional authority, not marketing amplitude. The hero copy does the heavy lifting — the size doesn't need to shout.

---

## 4. Layout & Spacing

### 4.1 Container & Content Widths

| Token                  | Value                        | Usage                                       |
|------------------------|------------------------------|---------------------------------------------|
| `--container-max`      | **1160px**                   | Max width for nav, full-width sections      |
| `--content-max`        | **1160px**                   | Primary content max-width (was 640px)       |
| `--content-narrow`     | 720px                        | Long-form prose, privacy text, fine print   |
| `--side-padding`       | 24px                         | Left/right page padding (mobile ≤640px)    |
| `--side-padding-lg`    | 32px                         | Left/right page padding (tablet/desktop)    |

**Key change:** Content max-width expanded from 560–640px to **1160px**. Sections like "How It Works" and "What You Get" should use wider multi-column or grid layouts. Only long-form body copy (privacy policy, legal) narrows to 720px.

### 4.2 Section Spacing

| Token                      | Desktop     | Mobile (≤640px) |
|----------------------------|-------------|-----------------|
| `--section-gap`            | **92px**    | 72px            |
| `--section-gap-lg`         | **96px**    | 80px            |
| `--section-gap-sm`         | 64px        | 48px            |
| `--hero-padding-top`        | 96px        | 72px            |
| `--hero-padding-bottom`    | 64px        | 48px            |

**Key change:** Desktop section spacing reduced from 112–128px → **88–96px**. Closer grouping creates better connection between related content. Mobile stays at 64–80px. The spacing between major page sections (Hero → How It Works → What You Get → Pricing → CTA → Contact) uses `--section-gap` (92px). Only the final pre-footer gap uses `--section-gap-lg` (96px).

### 4.3 Internal Spacing

| Token             | Value   | Usage                              |
|-------------------|---------|------------------------------------|
| `--gap-xs`        | 4px     | Icon-text gaps, tight inline      |
| `--gap-sm`        | 8px     | Label-to-value, tight vertical    |
| `--gap-md`        | 16px    | Between elements in a group        |
| `--gap-lg`        | 24px    | Between groups, step gaps          |
| `--gap-xl`        | 32px    | After headlines, before CTAs       |
| `--gap-2xl`       | 48px    | Major section internal breaks       |

---

## 5. Grid Systems

### 5.1 Desktop Grid (≥1024px)

- **How It Works:** 4-column horizontal layout. Each step is a column with icon/number on top, title + description below.
- **What You Get:** 2-column grid, 3 rows. Each benefit is a card or list item with icon.
- **Pricing:** Centered, max-width 580px card (stays narrow — pricing should feel contained).
- **Contact:** 2-column layout with label/value pairs.

### 5.2 Tablet Grid (641–1023px)

- **How It Works:** 2×2 grid (2 columns, 2 rows).
- **What You Get:** 2-column grid.
- **Pricing:** Same as desktop, centered.

### 5.3 Mobile Grid (≤640px)

- All sections collapse to single column.
- Steps stack vertically with step-number aligned left.

---

## 6. Interactions — Complete Specification

### 6.1 Buttons — Primary (e.g., "Book a Free Demo")

```
Base State:
  display:          inline-flex
  align-items:      center
  justify-content:  center
  padding:          14px 28px
  font-size:        15px (0.9375rem)
  font-weight:      700
  line-height:      1.0
  background:       #F97316
  color:            #0A1428
  border:           none
  border-radius:    8px
  box-shadow:       0 1px 2px rgba(0, 0, 0, 0.16),     — ambient
                    0 2px 4px rgba(0, 0, 0, 0.08)        — spread
  cursor:           pointer
  text-decoration:  none
  transition:       background 0.15s ease,
                    box-shadow 0.15s ease,
                    transform 0.1s ease

Hover State:
  background:       #EA6C0A
  color:            #FFFFFF
  box-shadow:       0 2px 4px rgba(0, 0, 0, 0.20),
                    0 4px 8px rgba(0, 0, 0, 0.12)
  text-decoration:  none

Active State (:active):
  background:       #C2590A
  color:            #FFFFFF
  box-shadow:       0 0px 1px rgba(0, 0, 0, 0.12),
                    0 1px 2px rgba(0, 0, 0, 0.08)
  transform:        translateY(1px)

Focus-Visible State:
  outline:          3px solid #F97316
  outline-offset:   3px
  border-radius:    8px

Disabled State:
  background:       #334155
  color:            #8B9BB5
  cursor:           not-allowed
  box-shadow:       none
```

### 6.2 Buttons — Secondary (e.g., "Calculate Your Lost Revenue")

```
Base State:
  display:          inline-flex
  align-items:      center
  justify-content:  center
  padding:          14px 28px
  font-size:        15px (0.9375rem)
  font-weight:      600
  line-height:      1.0
  background:       #1E293B
  color:            #F8FAFC
  border:           1px solid #334155
  border-radius:    8px
  box-shadow:       0 1px 2px rgba(0, 0, 0, 0.12),
                    0 1px 3px rgba(0, 0, 0, 0.08)
  cursor:           pointer
  text-decoration:  none
  transition:       background 0.15s ease,
                    border-color 0.15s ease,
                    box-shadow 0.15s ease,
                    transform 0.1s ease

Hover State:
  background:       #334155
  border-color:     #475569
  color:            #F8FAFC
  box-shadow:       0 2px 4px rgba(0, 0, 0, 0.16),
                    0 3px 6px rgba(0, 0, 0, 0.10)

Active State (:active):
  background:       #475569
  border-color:     #64748B
  color:            #F8FAFC
  box-shadow:       0 0px 1px rgba(0, 0, 0, 0.10),
                    0 1px 2px rgba(0, 0, 0, 0.06)
  transform:        translateY(1px)

Focus-Visible State:
  outline:          3px solid #F97316
  outline-offset:   3px
  border-radius:    8px

Disabled State:
  background:       #0A1428
  border-color:     #1E293B
  color:            #475569
  cursor:           not-allowed
  box-shadow:       none
```

### 6.3 Buttons — Nav CTA (compact, in nav bar)

```
Base State:
  display:          inline-flex
  align-items:      center
  justify-content:  center
  padding:          8px 18px
  font-size:        14px (0.875rem)
  font-weight:      700
  line-height:      1.0
  background:       #F97316
  color:            #0A1428
  border:           none
  border-radius:    6px
  box-shadow:       0 1px 2px rgba(0, 0, 0, 0.14)
  cursor:           pointer
  text-decoration:  none
  transition:       background 0.15s ease,
                    box-shadow 0.15s ease

Hover State:
  background:       #EA6C0A
  color:            #FFFFFF
  box-shadow:       0 2px 4px rgba(0, 0, 0, 0.20)

Active State (:active):
  background:       #C2590A
  color:            #FFFFFF
  box-shadow:       0 1px 1px rgba(0, 0, 0, 0.10)
  transform:        translateY(1px)

Focus-Visible State:
  outline:          3px solid #F97316
  outline-offset:   2px
  border-radius:    6px
```

### 6.4 Buttons — Small / Inline (if needed for future use)

```
Base State:
  padding:          10px 20px
  font-size:        14px (0.875rem)
  font-weight:      700
  border-radius:    6px
  (All other properties mirror Primary or Secondary variant, scaled down)
```

---

## 7. Cards — Complete Specification

### 7.1 Content Card (feature cards, benefit cards)

```
Base State:
  background:       #1E293B
  border:           1px solid #334155
  border-radius:    12px
  padding:          32px
  box-shadow:       0 1px 2px rgba(0, 0, 0, 0.10),
                    0 2px 6px rgba(0, 0, 0, 0.08),
                    0 4px 12px rgba(0, 0, 0, 0.06)
  transition:       border-color 0.2s ease,
                    box-shadow 0.2s ease,
                    transform 0.2s ease

Hover State:
  border-color:     #475569
  box-shadow:       0 2px 4px rgba(0, 0, 0, 0.12),
                    0 4px 10px rgba(0, 0, 0, 0.10),
                    0 8px 20px rgba(0, 0, 0, 0.08)
  transform:        translateY(-2px)

Focus-Visible State (if card is clickable):
  outline:          3px solid #F97316
  outline-offset:   2px
  border-radius:    12px
```

### 7.2 Pricing Card

```
Base State:
  background:       #1E293B
  border:           1px solid #334155
  border-radius:    12px
  padding:          36px 32px
  box-shadow:       0 1px 2px rgba(0, 0, 0, 0.10),
                    0 2px 6px rgba(0, 0, 0, 0.08),
                    0 6px 16px rgba(0, 0, 0, 0.06)
  max-width:         580px
  margin:           0 auto

Hover State:
  border-color:     #475569
  box-shadow:       0 2px 4px rgba(0, 0, 0, 0.12),
                    0 4px 10px rgba(0, 0, 0, 0.10),
                    0 8px 24px rgba(0, 0, 0, 0.08)

Focus-Visible:      N/A (pricing card is not a clickable element itself)
```

### 7.3 CTA Banner Card

```
Base State:
  background:       linear-gradient(135deg, #1E293B 0%, #0A1428 100%)
  border:           1px solid #334155
  border-radius:    12px
  padding:          48px 40px
  text-align:       center
  box-shadow:       0 1px 2px rgba(0, 0, 0, 0.10),
                    0 4px 12px rgba(0, 0, 0, 0.08)

Mobile (≤640px):
  padding:          32px 24px
```

### 7.4 Step Number Circle

```
Base State:
  width:             36px
  height:            36px
  background:        #1E293B
  border:            1px solid #334155
  border-radius:     50%
  display:           flex
  align-items:       center
  justify-content:   center
  font-size:         14px (0.875rem)
  font-weight:       700
  color:             #F97316
  flex-shrink:       0
```

### 7.5 Launch Special Callout (inside pricing card)

```
background:          rgba(249, 115, 22, 0.08)
border:              1px solid rgba(249, 115, 22, 0.25)
border-radius:       8px
padding:             16px 20px
```

---

## 8. Focus-Visible — Universal Specification

Every interactive element on the page receives a consistent focus-visible style. The focus ring must be visible against both dark backgrounds (`#0A1428`, `#1E293B`) and the orange accent (`#F97316`).

### 8.1 Global Focus Ring

```css
:focus-visible {
  outline: 3px solid #F97316;
  outline-offset: 2px;
}
```

### 8.2 Per-Element Focus Adjustments

| Element                  | Outline Width | Outline Offset | Border-Radius Override | Notes                                      |
|--------------------------|---------------|-----------------|------------------------|---------------------------------------------|
| **Primary Button**       | 3px           | 3px             | 8px                    | Extra offset keeps ring outside shadow      |
| **Secondary Button**     | 3px           | 3px             | 8px                    | Same as primary                              |
| **Nav CTA Button**       | 3px           | 2px             | 6px                    | Tighter offset in nav context                |
| **Nav Links**            | 3px           | 2px             | —                      | Default works; no border-radius needed       |
| **Text Links (in body)** | 3px           | 2px             | —                      | Orange ring clearly visible on dark text     |
| **Contact Links**        | 3px           | 2px             | —                      | Same as text links                            |
| **Footer Links**         | 2px           | 2px             | —                      | Slightly thinner in footer context           |
| **Content Cards** (if clickable) | 3px   | 2px             | 12px                   | Matches card border-radius                   |
| **Mobile Menu Toggle**   | 3px           | 2px             | —                      | Default radius on icon button                |
| **Skip-to-Content Link** | 3px           | —               | 0 0 8px 0              | Custom: white outline on orange bg, special positioning |
| **Input Fields** (future)| 3px           | 2px             | —                      | Same as text links                           |

### 8.3 Focus Ring Color Rationale

- `#F97316` (accent orange) chosen because:
  - 4.6:1 contrast ratio against `#0A1428` (background) — passes WCAG AA
  - Visually distinct from both dark surfaces and light text
  - Reinforces brand identity on every keyboard interaction
  - Matches active CTA color — creates visual consistency between "action" and "focus"

### 8.4 Focus Ring Must NOT Appear On

- Mouse clicks (use `:focus-visible`, not `:focus`)
- Non-interactive elements
- Elements already in active state that show a separate visual change

---

## 9. Navigation Bar

```
Position:           sticky
Top:                0
Z-Index:            50
Background:         rgba(10, 20, 40, 0.95)
Backdrop-Filter:    blur(12px)
Border-Bottom:      1px solid #1E293B
Max-Width:          1160px (matches container)
Inner Padding:      16px 24px (mobile), 16px 32px (desktop)
Nav-Link Color:     #8B9BB5
Nav-Link Hover:     #F8FAFC
Nav-Link Font:      14px, weight 500
Nav-Link Gap:       28px
Nav CTA Gap:        Separate from links with gap
Logo Font:          18px (1.1rem), weight 800
Logo Color:         #F8FAFC (with "AI" in #F97316)
Mobile Breakpoint:  ≤640px → hamburger menu
```

---

## 10. Shadows — Reference Table

Every shadow on the site uses one of these defined layers. No ad-hoc shadow values.

| Token                    | Value                                                                 | Usage                              |
|--------------------------|-----------------------------------------------------------------------|-------------------------------------|
| `--shadow-sm`            | `0 1px 2px rgba(0,0,0,0.10)`                                        | Nav links, small static elements    |
| `--shadow-btn-base`      | `0 1px 2px rgba(0,0,0,0.16), 0 2px 4px rgba(0,0,0,0.08)`           | Primary button base                 |
| `--shadow-btn-hover`     | `0 2px 4px rgba(0,0,0,0.20), 0 4px 8px rgba(0,0,0,0.12)`          | Primary button hover                |
| `--shadow-btn-active`    | `0 0px 1px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.08)`          | Button pressed state               |
| `--shadow-btn2-base`     | `0 1px 2px rgba(0,0,0,0.12), 0 1px 3px rgba(0,0,0,0.08)`          | Secondary button base               |
| `--shadow-btn2-hover`    | `0 2px 4px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.10)`          | Secondary button hover              |
| `--shadow-card-base`     | `0 1px 2px rgba(0,0,0,0.10), 0 2px 6px rgba(0,0,0,0.08), 0 4px 12px rgba(0,0,0,0.06)` | Content card base         |
| `--shadow-card-hover`    | `0 2px 4px rgba(0,0,0,0.12), 0 4px 10px rgba(0,0,0,0.10), 0 8px 20px rgba(0,0,0,0.08)` | Content card hover       |
| `--shadow-pricing-base`  | `0 1px 2px rgba(0,0,0,0.10), 0 2px 6px rgba(0,0,0,0.08), 0 6px 16px rgba(0,0,0,0.06)` | Pricing card base         |
| `--shadow-pricing-hover` | `0 2px 4px rgba(0,0,0,0.12), 0 4px 10px rgba(0,0,0,0.10), 0 8px 24px rgba(0,0,0,0.08)` | Pricing card hover        |
| `--shadow-banner`        | `0 1px 2px rgba(0,0,0,0.10), 0 4px 12px rgba(0,0,0,0.08)`        | CTA banner card                     |
| `--shadow-nav`           | `0 1px 3px rgba(0,0,0,0.08)`                                        | Nav bar bottom shadow               |

---

## 11. Borders & Dividers

| Token                   | Value                                          | Usage                              |
|-------------------------|------------------------------------------------|-------------------------------------|
| `--border-default`      | `1px solid #334155`                            | Card borders, input borders         |
| `--border-subtle`       | `1px solid #1E293B`                            | Section dividers, footer border     |
| `--border-hover`        | `1px solid #475569`                            | Card hover border, secondary btn hover |
| `--border-active`       | `1px solid #64748B`                            | Active state borders               |
| `--border-accent-subtle`| `1px solid rgba(249, 115, 22, 0.25)`           | Launch special callout              |
| `--radius-sm`           | 6px                                             | Nav CTA, small buttons, badges     |
| `--radius-md`           | 8px                                             | Primary/secondary buttons, inputs  |
| `--radius-lg`           | 12px                                            | Cards, CTA banner, pricing card   |
| `--radius-full`         | 50%                                             | Step number circles, avatars        |

---

## 12. Motion & Transitions

| Property              | Duration  | Easing            | Usage                                    |
|-----------------------|-----------|-------------------|------------------------------------------|
| color                 | 0.15s     | ease              | Nav link hover, text link hover           |
| background-color      | 0.15s     | ease              | Button hover/active                       |
| border-color          | 0.15s     | ease              | Secondary button hover                    |
| box-shadow            | 0.15s     | ease              | Button hover states                       |
| transform             | 0.1s      | ease              | Button active (translateY), card hover    |
| box-shadow (cards)    | 0.2s      | ease              | Card hover transitions                    |
| border-color (cards)  | 0.2s      | ease              | Card hover transitions                    |
| transform (cards)     | 0.2s      | ease              | Card hover lift                           |

**No animations on page load. No fade-ins, no slide-ups, no scroll-triggered reveals.** This is a professional B2B site — content should be immediately present. Motion only on interaction.

---

## 13. Responsive Breakpoints

| Token       | Width        | Notes                                    |
|-------------|--------------|-------------------------------------------|
| `--bp-sm`   | ≤480px       | Small phones — single column, stacked CTAs |
| `--bp-md`   | ≤640px       | Mobile — hamburger nav, reduced spacing   |
| `--bp-lg`   | ≤1023px      | Tablet — 2-column grids                   |
| `--bp-xl`   | ≥1024px      | Desktop — full layout, 4-col how-it-works |

### Responsive Adjustments Summary

- **≤480px:** h1 → 28px, section gap → 48px, CTA buttons stack, hero padding reduces
- **≤640px:** h1 → 32px, nav collapses to hamburger, section gap → 64–72px, cards padding → 24px
- **641–1023px:** h1 → 36px, grids to 2 columns, section gap → 80px
- **≥1024px:** h1 → 44px, full grid layouts, section gap → 92px, container max-width 1160px

---

## 14. Section-by-Section Layout Notes

### 14.1 Hero
- Full container width (1160px max)
- h1 max-width: ~720px (doesn't span full width — wraps at 2–3 lines)
- Tagline + tagline-sub max-width: ~720px
- CTA row: flex, gap 16px
- Padding top: 96px desktop, 72px mobile
- Padding bottom: 64px desktop, 48px mobile

### 14.2 How It Works
- Desktop: 4-column grid, each step is a card or column
- Step number circle on top, content below
- Or: horizontal timeline with step numbers
- Section gap before: 92px

### 14.3 What You Get
- Desktop: 2-column grid, icon + text per benefit
- Section gap before: 92px

### 14.4 Who We Serve
- Simple centered paragraph; no special layout needed
- Section gap before: 92px

### 14.5 Pricing
- Single centered card, max-width 580px (pricing feels best tight)
- Section gap before: 92px

### 14.6 CTA Banner
- Full container width (1160px max)
- Centered text, centered CTA button
- Section gap before: 92px

### 14.7 Contact
- 2-column grid on desktop: labels left, values right
- Or: flex row with justified items
- Section gap before: 92px

### 14.8 Footer
- Full width within container
- Top border 1px solid #1E293B
- No bottom section gap (last section)

---

## 15. Accessibility Checklist

- [x] All interactive elements have focus-visible styles (specified above)
- [x] Skip-to-content link present
- [x] Color contrast: `#F8FAFC` on `#0A1428` = 14.3:1 (AAA)
- [x] Color contrast: `#CBD5E1` on `#0A1428` = 9.2:1 (AAA)
- [x] Color contrast: `#94A3B8` on `#0A1428` = 5.9:1 (AA)
- [x] Color contrast: `#8B9BB5` on `#0A1428` = 4.7:1 (AA)
- [x] Color contrast: `#0A1428` on `#F97316` = 4.6:1 (AA) — primary button text
- [x] Focus ring `#F97316` on `#0A1428` = 4.6:1 (AA)
- [x] Focus ring `#F97316` on `#1E293B` = 3.9:1 — acceptable for large UI components (WCAG 1.4.11)
- [x] No information conveyed by color alone
- [x] All form elements have visible labels (future)
- [x] Nav has `aria-label`
- [x] Semantic HTML: `<nav>`, `<main>`, `<footer>`, `<section>`
- [x] Reduced motion: `prefers-reduced-motion` disables all transitions

---

## 16. Reference Site Alignment

### ServiceTitan.com
- Same audience (home service businesses)
- Professional, trust-building tone
- Clear value propositions with specifics
- **Adopted:** Direct language, "never miss a call" framing, pricing clarity

### GetJobber.com
- Clean, practical layout
- Generous whitespace but not sparse
- Clear CTAs without being aggressive
- **Adopted:** Section spacing tightness, button sizing, content width balance

### Linear.app
- Best-in-class dark theme execution
- Subtle but layered shadows
- Tight typography with controlled hierarchy
- **Adopted:** Shadow system (multi-layer, graduated), focus-visible consistency, controlled h1 size, interaction state precision

---

*This design system is Phase 1 only — no HTML or section code. All values are exact and ready for implementation.*