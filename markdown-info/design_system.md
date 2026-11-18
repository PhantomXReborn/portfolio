# 🎨 Design System — Reece Hannah's Galaxy Portfolio

> **Course:** CST3106 — Lab 04
> **Author:** Reece Hannah
> **Project:** Galaxy Portfolio (Minecraft End Dimension theme)
> **Last Updated:** 2026

---

## 1. Overview

The Galaxy Portfolio is a personal developer portfolio built with **vanilla HTML, CSS, and JavaScript**. The visual identity fuses two themes:

- 🌌 **Galaxy / Space** — nebula gradients, twinkling stars, floating particles
- 🟪 **Minecraft End Dimension** — End portal purples, End stone grays, End city gold

This document defines the **design tokens, typography, components, layouts, and responsive behavior** used throughout the project.

---

## 2. Color Palette

All colors are stored as CSS custom properties (variables) in `:root` inside `style.css`.

### 2.1 Core Backgrounds (Void Layer)

| Token | Hex | Usage |
|-------|-----|-------|
| `--end-void` | `#05070a` | Deepest background (body) |
| `--end-bg` | `#0b0e14` | Main page background |
| `--end-dark` | `#0f1118` | Dark panels, cards |

### 2.2 End Dimension Accents

| Token | Hex | Usage |
|-------|-----|-------|
| `--end-purple` | `#6a4c9c` | Primary accent, End portal glow |
| `--end-cyan` | `#4a9e9e` | Secondary accent, End sky teal |
| `--end-teal` | `#2d7a7a` | Darker teal variant |
| `--end-glow` | `#b7a5e0` | Soft lavender, text glow |
| `--end-gold` | `#c9a84c` | End city gold accent |

### 2.3 Structural (End Stone)

| Token | Hex | Usage |
|-------|-----|-------|
| `--end-stone` | `#2a2e3a` | Borders, dividers |
| `--end-stone-light` | `#3a3f4d` | Lighter borders |

### 2.4 Galaxy Accents

| Token | Hex | Usage |
|-------|-----|-------|
| `--galaxy-1` | `#5865f2` | Blue |
| `--galaxy-2` | `#9b59b6` | Violet |
| `--galaxy-3` | `#3498db` | Sky blue |
| `--galaxy-4` | `#1abc9c` | Turquoise |

### 2.5 Text Colors

| Token | Hex | Contrast on `#05070a` | WCAG |
|-------|-----|----------------------|------|
| `--text` | `#e8e6f0` | 15.2:1 | ✅ AAA |
| `--text-muted` | `#9a94b0` | 7.1:1 | ✅ AA+ |

### 2.6 Palette Reference

- [W3Schools CSS Colors](https://www.w3schools.com/css/css_colors.asp)
- [W3Schools Color Palettes](https://www.w3schools.com/colors/colors_palettes.asp)

---

## 3. Typography

### 3.1 Font Families

| Token | Stack | Purpose |
|-------|-------|---------|
| `--font-mono` | `'Fira Code', 'Courier New', monospace` | Code, labels, tags |
| `--font-pixel` | `'Press Start 2P', 'Courier New', monospace` | Headings, logo, section titles |
| `--font-sans` | `'Inter', -apple-system, sans-serif` | Body text |

Loaded from **Google Fonts**:
```html
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600&family=Press+Start+2P&display=swap" rel="stylesheet">
```

### 3.2 Type Scale

| Style | Size | Weight | Font | Usage |
|-------|------|--------|------|-------|
| Display | 2.5rem | 600 | mono | Hero name (h1) |
| H2 | 1.8rem | 600 | pixel | Section headers |
| H3 | 1rem | 600 | mono | Card titles |
| Body | 0.95rem | 400 | sans | Paragraphs |
| Body SM | 0.85rem | 400 | sans | Project descriptions |
| Caption | 0.75rem | 400 | mono | Meta info, dates |
| Label | 0.7rem | 400 | mono | Language tags |
| Pixel SM | 0.8rem | 400 | pixel | Section titles |
| Pixel XS | 0.75rem | 400 | pixel | Filter titles |

### 3.3 Typography Reference

- [W3Schools CSS Fonts](https://www.w3schools.com/css/css_font.asp)

---

## 4. Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | 0.2rem | Tight (lang tag padding-y) |
| `--space-2` | 0.4rem | Icon gaps |
| `--space-3` | 0.5rem | Small gaps |
| `--space-4` | 0.8rem | Button padding, doc gaps |
| `--space-5` | 1rem | Standard padding |
| `--space-6` | 1.2rem | Doc item padding |
| `--space-7` | 1.5rem | Section margins, card padding |
| `--space-8` | 2rem | Menu padding, section gaps |
| `--space-9` | 2.5rem | Hero padding |
| `--space-10` | 3rem | Large gaps |

---

## 5. Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 6px | Menu toggle button |
| `--radius-md` | 10px | Doc items |
| `--radius` | 12px | Cards, menu, panels |
| `--radius-lg` | 20px | Lang tags, doc links |
| `--radius-pill` | 30px | Filter buttons |
| `--radius-full` | 50% | Avatar, particles |

---

## 6. Shadows & Glows

| Token | Value | Usage |
|-------|-------|-------|
| `--shadow` | `0 8px 32px rgba(0,0,0,0.7)` | Base drop shadow |
| `--glow-purple` | `0 0 20px rgba(106,76,156,0.15)` | Menu outer glow |
| `--glow-cyan` | `0 0 15px rgba(74,158,158,0.2)` | Hover glow |
| `--glow-card` | `0 12px 40px rgba(106,76,156,0.25)` | Card hover |

---

## 7. Motion & Animation

| Token | Value | Usage |
|-------|-------|-------|
| `--ease-snap` | `cubic-bezier(0.175, 0.885, 0.32, 1.275)` | Bounce hover |
| `--ease-smooth` | `0.3s` | Standard transitions |
| `--ease-slow` | `0.6s` | Shine sweep |
| Twinkle | 4s / 6s / 8s | Star layers |
| Float Particle | 16s–25s | Floating particles |
| Portal Rotation | 8s | Menu background |
| Logo Pulse | 2s | Logo icon |
| Avatar Glow | 3s | Avatar border |

---

## 8. Components

### 8.1 Header / Navigation (End Portal Style)

![Menu Screenshot](./screenshots/02-menu.png)

- **Background:** Frosted glass (`rgba(10,12,20,0.85)` + `backdrop-filter: blur(12px)`)
- **Border:** 1px purple (30% opacity), 12px radius
- **Effect:** Rotating conic-gradient `::before` (8s loop)
- **Layout:** Flexbox — logo left, links right, hamburger (mobile)
- **Logo:** Pixel font, lavender with purple glow, `fa-cube` icon
- **Nav Links:** Mono font, muted color, animated `::after` underline (0 → 100% width)
- **Link Format:** `// projects`, `// writings`, `// resume`, `// contact`

**States:**
| State | Behavior |
|-------|----------|
| Default | Muted text, no underline |
| Hover | Lavender text, gradient underline expands |
| Active | (Handled via anchor scroll) |
| Mobile ≤900px | Links collapse into dropdown, hamburger visible |

### 8.2 Hero Section

![Hero Screenshot](./screenshots/01-hero.png)

- **Layout:** Flexbox row (desktop) → column (≤600px)
- **Avatar:** 120px gradient circle (purple → cyan), pulsing glow animation
- **Name (h1):** 2.5rem mono, gradient text (lavender → cyan)
- **Subhead:** Mono font, muted color, flex-wrap with icon + text pairs
  - 💻 Advanced Technologies Student
  - 📍 Kanata, ON | Remote
  - ✉️ Contact emails
- **Decorative:** Soft glowing blob in top-right (`::after`, `glowPulse` animation)

### 8.3 Filter Bar

![Filter Bar Screenshot](./screenshots/03-filter-bar.png)

- **Layout:** Flex-wrap row of pill buttons
- **Button:** 30px radius, mono font, transparent bg, purple border
- **States:**
  | State | Style |
  |-------|-------|
  | Default | Muted text, purple border |
  | Hover | Cyan border, lavender text, lift `-2px` |
  | Active | Purple→cyan gradient bg, white text, glow |
- **Behavior:** JavaScript reads `data-filter` attribute, shows/hides project cards

### 8.4 Project Grid

![Project Grid Screenshot](./screenshots/04-project-grid.png)

- **Layout:** CSS Grid `repeat(auto-fill, minmax(280px, 1fr))`
- **Card:**
  - Background: `rgba(15,17,28,0.8)` + backdrop blur
  - Border: 1px purple (20% opacity), 12px radius
  - Padding: 1.5rem
  - Transition: bounce easing `cubic-bezier(0.175, 0.885, 0.32, 1.275)`
- **Card Structure:**
  - `.project-header` — icon + project name
  - `.project-desc` — description (flex: 1 to push links down)
  - `.project-langs` — row of `.lang-tag` pills
  - `.project-links` — Repository + Demo links
- **Hover Effect:**
  - Lift `-6px` + scale `1.01`
  - Cyan border
  - Dual glow (purple + cyan)
  - Shine sweep animation (`::before` slides left → right)

### 8.5 Language Tags

```html
<span class="lang-tag">HTML5</span>
```

- 0.7rem mono font
- Purple-tinted background (15% opacity)
- Purple border (30% opacity)
- 20px radius, 0.2rem / 0.7rem padding
- Lavender text

### 8.6 Resume Section

![Resume Screenshot](./screenshots/05-resume.png)

- **Layout:** CSS Grid `1fr 1fr` (2 columns desktop) → `1fr` (mobile)
- **Card:**
  - Background: `rgba(12,14,24,0.7)` + backdrop blur
  - Border: 1px purple (20% opacity)
  - Padding: 1.5rem
- **Card Header (h3):** Mono font, cyan color, purple icon
- **Job Item:**
  - Title: 0.95rem, weight 600
  - Company: Mono, purple
  - Date: Mono, muted, 0.7rem
  - Description: 0.85rem, muted

### 8.7 Writings & Documents

![Writings Screenshot](./screenshots/06-writings.png)

- **Layout:** Vertical stack of `.doc-item` rows
- **Doc Item:**
  - Flex row, space-between (info left, link right)
  - Background: `rgba(15,17,28,0.7)` + backdrop blur
  - Border: 1px purple (15% opacity), 10px radius
  - Padding: 1rem 1.2rem
- **Doc Info:** Icon (purple, glow) + title + meta
- **Doc Meta:** Mono font, muted, flex gap 0.8rem
- **Doc Link:** Pill button (20px radius), hover cyan

### 8.8 Footer / Status Bar

![Footer Screenshot](./screenshots/07-footer.png)

- **Layout:** Flex row, space-between → column (≤600px)
- **Style:** Mono font, 0.75rem, muted text
- **Background:** `rgba(10,12,20,0.9)` + backdrop blur
- **Border:** 1px purple (20% opacity), 12px radius
- **Content:**
  - Left: ✅ main* · 0 problems · ready to build
  - Right: 🔀 24 repos · 📄 8 docs · ✉️ contact

---

## 9. Layout System

### 9.1 Container

```css
.portfolio {
  max-width: 1300px;
  margin: 2rem auto;
  padding: 0 1.5rem;
  position: relative;
  z-index: 1;
}
```

### 9.2 Background Layers (Z-Index Stack)

| Layer | Class | z-index | Effect |
|-------|-------|---------|--------|
| 1 (bottom) | `.galaxy-bg` | -2 | Nebula radial gradients |
| 2 | `.stars` | -1 | White stars, twinkle 4s |
| 3 | `.stars2` | -1 | Colored stars, twinkle 6s |
| 4 | `.stars3` | -1 | Sparse bright stars, twinkle 8s |
| 5 | `.particles` | -1 | 10 floating purple dots |
| 6 | `.portfolio` | 1 | All content |

### 9.3 Grid System

- **Project Grid:** `repeat(auto-fill, minmax(280px, 1fr))`
- **Resume Section:** `1fr 1fr` (desktop) → `1fr` (mobile)
- **Menu:** Flexbox (logo | links | hamburger)

---

## 10. Responsive Design

![Mobile Screenshot](./screenshots/08-mobile.png)

| Breakpoint | Width | Changes |
|------------|-------|---------|
| **Desktop** | >900px | Full layout, nav links visible, 2-col resume |
| **Tablet** | ≤900px | Hamburger menu, 1-col resume, dropdown nav |
| **Phone** | ≤600px | Stacked hero, 90px avatar, reduced padding, wrapped doc items, stacked status bar |

```css
@media (max-width: 900px) {
  .resume-section { grid-template-columns: 1fr; }
  .nav-links { display: none; /* dropdown when .open */ }
  .menu-toggle { display: block; }
}

@media (max-width: 600px) {
  .hero { flex-direction: column; text-align: center; }
  .avatar { width: 90px; height: 90px; }
  .portfolio { padding: 0 0.8rem; }
  .status-bar { flex-direction: column; }
}
```

---

## 11. Accessibility Notes

| Issue | Location | Recommendation |
|-------|----------|----------------|
| Low contrast | `--end-purple` text | Use for icons/borders only |
| Menu toggle | `.menu-toggle` | Add `aria-expanded` state |
| Focus states | Not defined | Add `:focus-visible` outlines |
| Reduced motion | Not handled | Add `prefers-reduced-motion` media query |

**Recommended additions:**

```css
:focus-visible {
  outline: 2px solid var(--end-cyan);
  outline-offset: 2px;
  border-radius: 4px;
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 12. Component Reference Table

| Component | Class | File Location | Screenshot |
|-----------|-------|---------------|------------|
| Menu Bar | `.menu` | style.css | `02-menu.png` |
| Nav Links | `.nav-links` | style.css | `02-menu.png` |
| Logo | `.logo` | style.css | `02-menu.png` |
| Menu Toggle | `.menu-toggle` | style.css | `08-mobile.png` |
| Hero | `.hero` | style.css | `01-hero.png` |
| Avatar | `.avatar` | style.css | `01-hero.png` |
| Filter Bar | `.filter-bar` | style.css | `03-filter-bar.png` |
| Filter Button | `.filter-btn` | style.css | `03-filter-bar.png` |
| Project Grid | `.project-grid` | style.css | `04-project-grid.png` |
| Project Card | `.project-card` | style.css | `04-project-grid.png` |
| Language Tag | `.lang-tag` | style.css | `04-project-grid.png` |
| Resume Section | `.resume-section` | style.css | `05-resume.png` |
| Resume Card | `.resume-card` | style.css | `05-resume.png` |
| Doc List | `.doc-list` | style.css | `06-writings.png` |
| Doc Item | `.doc-item` | style.css | `06-writings.png` |
| Status Bar | `.status-bar` | style.css | `07-footer.png` |

---

## 13. References

- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [Dillinger Markdown Editor](https://dillinger.io/)
- [W3Schools CSS Colors](https://www.w3schools.com/css/css_colors.asp)
- [W3Schools CSS Fonts](https://www.w3schools.com/css/css_font.asp)
- [Google Fonts](https://fonts.google.com/)
- [Font Awesome](https://fontawesome.com/)
- [GitHub Docs](https://docs.github.com/en)
- Lab example: [Joe Smith Design System](https://github.com/kvhuang23/cst3106_labs/blob/main/lab04/Joe_Smith_design_system.md)

---

## 14. Author & License

**Reece Hannah** — CST3106 Student
MIT License © 2026