# Jeongjin Profile Design System

## 1. Atmosphere & Identity

A concise personal homepage that feels credible, direct, and easy to scan. The signature is a centered profile identity with editorial project sections below it: familiar enough to feel canonical, but with enough structure to make the visitor understand what Jeongjin builds.

## 2. Color

### Palette

| Role | Token | Light | Dark | Usage |
|------|-------|-------|------|-------|
| Surface/primary | --surface-primary | #FBFAF7 | #101214 | Page background |
| Surface/secondary | --surface-secondary | #FFFFFF | #171A1D | Profile and project surfaces |
| Surface/elevated | --surface-elevated | #F3F0EA | #202428 | Highlight panels |
| Text/primary | --text-primary | #16181B | #F7F4EE | Headlines, body |
| Text/secondary | --text-secondary | #626970 | #B8B2A8 | Supporting copy |
| Text/tertiary | --text-tertiary | #8A9299 | #817B72 | Metadata |
| Border/default | --border-default | #DED8CF | #34383D | Cards, dividers |
| Border/subtle | --border-subtle | #EDE7DD | #24282C | Soft separations |
| Accent/primary | --accent-primary | #1F6FEB | #79A7FF | CTAs, links, focus |
| Accent/hover | --accent-hover | #174EA6 | #A7C3FF | Hover states |
| Accent/warm | --accent-warm | #B15C28 | #E6A06D | Profile mark and tags |
| Status/success | --status-success | #1A7F37 | #4BD46A | Confirmations |
| Status/warning | --status-warning | #9A6700 | #E3B341 | Cautions |
| Status/error | --status-error | #CF222E | #FF7B72 | Errors |
| Status/info | --status-info | #0969DA | #79A7FF | Informational |

### Rules

- Accent blue is reserved for links, focus rings, and primary actions.
- Warm accent appears only in small identity details and topic tags.
- Never introduce raw page colors outside this table.

## 3. Typography

### Scale

| Level | Size | Weight | Line Height | Tracking | Usage |
|-------|------|--------|-------------|----------|-------|
| Display | 56px | 760 | 1.05 | 0 | Main name |
| H1 | 40px | 720 | 1.15 | 0 | Page sections |
| H2 | 28px | 680 | 1.2 | 0 | Section headers |
| H3 | 20px | 680 | 1.35 | 0 | Card titles |
| Body/lg | 18px | 420 | 1.7 | 0 | Lead copy |
| Body | 16px | 420 | 1.65 | 0 | Default text |
| Body/sm | 14px | 450 | 1.55 | 0 | Secondary info |
| Caption | 12px | 650 | 1.4 | 0.04em | Labels, metadata |
| Overline | 11px | 700 | 1.3 | 0.08em | Section labels |

### Font Stack

- Primary: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif
- Mono: ui-monospace, "SFMono-Regular", "SF Mono", Consolas, monospace

### Rules

- Letter spacing is 0 for normal text.
- Display text uses clamp() to preserve mobile wrapping.
- Body text never drops below 14px.

## 4. Spacing & Layout

### Base Unit

All spacing derives from a base of 4px.

| Token | Value | Usage |
|-------|-------|-------|
| --space-1 | 4px | Tight inline gaps |
| --space-2 | 8px | Compact item gaps |
| --space-3 | 12px | Tag and button padding |
| --space-4 | 16px | Default inline spacing |
| --space-5 | 20px | Compact section spacing |
| --space-6 | 24px | Card padding |
| --space-8 | 32px | Group spacing |
| --space-10 | 40px | Section inner spacing |
| --space-12 | 48px | Major spacing |
| --space-16 | 64px | Page rhythm |
| --space-20 | 80px | Hero rhythm |
| --space-24 | 96px | Maximum section spacing |

### Grid

- Max content width: 1120px
- Column system: 12-column desktop, single-column mobile
- Breakpoints: 640px, 768px, 1024px, 1280px, 1536px

### Rules

- Sections use full-width bands with constrained inner content.
- Repeated cards use CSS grid with stable minmax tracks.
- No nested cards.

## 5. Components

### Button Link

- Structure: anchor with text label and optional arrow glyph.
- Variants: primary, secondary.
- Spacing: --space-3 vertical, --space-4 horizontal.
- States: hover, active, focus-visible.
- Accessibility: real href, visible focus ring, minimum 44px tap target.
- Motion: 180ms transform and color transition.

### Project Card

- Structure: article with topic label, title, summary, and link.
- Variants: standard only.
- Spacing: --space-6 padding, --space-4 inner gap.
- States: hover border-color and slight translate.
- Accessibility: title link is the main action.
- Motion: 200ms transform and border-color transition.

### Publication Entry

- Structure: ordered-list item with date, linked paper title, and venue metadata.
- Variants: standard only.
- Spacing: --space-6 padding, --space-4 internal gap.
- States: linked title hover and focus-visible.
- Accessibility: semantic ordered list, machine-readable time element.
- Motion: link color transition only.

## 6. Motion & Interaction

### Timing

| Type | Duration | Easing | Usage |
|------|----------|--------|-------|
| Micro | 120ms | ease-out | Button press |
| Standard | 200ms | ease-in-out | Card hover |
| Emphasis | 480ms | cubic-bezier(0.16, 1, 0.3, 1) | Page entry |
| Scroll-driven | tied to scroll | linear | Not used |

### Rules

- Animate only transform and opacity.
- Respect prefers-reduced-motion.
- Every link-style control has hover, active, and focus-visible states.

## 7. Depth & Surface

### Strategy

Borders-only with light tonal shifts.

| Type | Value | Usage |
|------|-------|-------|
| Default | 1px solid var(--border-default) | Cards, dividers |
| Subtle | 1px solid var(--border-subtle) | Soft separations |
