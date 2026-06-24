# Jeongjin Shin Design System

## 1. Atmosphere & Identity

A restrained academic personal site inspired by the `msaveski/www_personal` structure: text header, thin section navigation, concise bio, education, publication entries, and links. The signature is low-friction readability: narrow measure, simple typography, thin rules, and almost no decorative styling.

## 2. Color

### Palette

| Role | Token | Light | Dark | Usage |
|------|-------|-------|------|-------|
| Surface/primary | --surface-primary | #FFFFFF | #111111 | Page background |
| Surface/secondary | --surface-secondary | #F7F7F7 | #181818 | Quiet fills |
| Text/primary | --text-primary | #222222 | #F2F2F2 | Main text and titles |
| Text/secondary | --text-secondary | #555555 | #C8C8C8 | Body support text |
| Text/tertiary | --text-tertiary | rgba(0, 0, 0, 0.48) | rgba(255, 255, 255, 0.5) | Footer, time labels |
| Border/default | --border-default | #EEEEEE | #303030 | Section rules |
| Accent/primary | --accent-primary | #1F77B4 | #76B7E8 | Links |
| Accent/hover | --accent-hover | #0F5F96 | #9ACCF0 | Link hover |

### Rules

- Use white as the default surface.
- Use thin neutral rules for structure.
- Accent appears only on links and focus states.

## 3. Typography

### Scale

| Level | Size | Weight | Line Height | Tracking | Usage |
|-------|------|--------|-------------|----------|-------|
| Display | 44px | 400 | 1.25 | 0 | Name |
| H1 | 36px | 400 | 1.25 | 0 | Mobile name |
| H2 | 18px | 600 | 1.25 | 0.1rem | Section labels |
| H3 | 18px | 600 | 1.25 | 0 | Project titles |
| Body | 16px | 400 | 1.6 | 0 | Paragraphs |
| Body/sm | 14px | 400 | 1.5 | 0 | Footer and metadata |
| Nav | 11px | 600 | 1 | 0.16rem | Uppercase nav |

### Font Stack

- Primary: Raleway, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif

### Rules

- Keep text narrow and direct.
- Section headings are uppercase labels, not marketing headlines.
- Body text never drops below 14px.

## 4. Spacing & Layout

### Base Unit

All spacing derives from a base of 4px.

| Token | Value | Usage |
|-------|-------|-------|
| --space-1 | 4px | Tight detail spacing |
| --space-2 | 8px | Inline gaps |
| --space-3 | 12px | Compact groups |
| --space-4 | 16px | Default spacing |
| --space-5 | 20px | Header detail spacing |
| --space-6 | 24px | Group spacing |
| --space-8 | 32px | Header and content gaps |
| --space-10 | 40px | Mobile section spacing |
| --space-12 | 48px | Section padding |
| --space-16 | 64px | Large rhythm |

### Grid

- Max content width: 800px
- Header layout: text-only academic identity block
- Mobile layout: single column with horizontally scrollable nav

### Rules

- No nested cards.
- Sections are separated by rules, not panels.
- Publication and education entries are lists of text, not tiles.

## 5. Components

### Profile Header

- Structure: name, role, research area, and profile links.
- Variants: standard only.
- Accessibility: real links, text-first identity.

### Section Nav

- Structure: sticky horizontal anchor nav.
- States: hover, focus-visible.
- Accessibility: real anchors to section ids.

### Paper

- Structure: article with linked title, author line, venue line, and button links.
- Variants: standard only.
- Accessibility: linked title plus explicit Paper button.

### Education Entry

- Structure: ordered-list item with date range and institution/program details.
- Variants: standard only.
- Accessibility: text-first, no decorative logo dependency.

## 6. Motion & Interaction

### Timing

| Type | Duration | Easing | Usage |
|------|----------|--------|-------|
| Micro | 120ms | ease-out | Link color changes |

### Rules

- Avoid animation except link hover feedback.
- Respect prefers-reduced-motion.

## 7. Depth & Surface

### Strategy

Borders-only.

| Type | Value | Usage |
|------|-------|-------|
| Default | 1px solid var(--border-default) | Nav, section dividers, footer |
