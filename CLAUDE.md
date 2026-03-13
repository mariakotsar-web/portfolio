# Portfolio Project

## Overview
Personal portfolio website for Maria Kotsar, Product Designer based in Toronto.

## Tech Stack
- HTML/CSS/JS (single-page, no framework)
- Fonts: Inter (body), Space Grotesk variable wght@300..700 (headings), JetBrains Mono (labels/tags) via Google Fonts
- Dark theme with CSS custom properties
- Scroll-reveal animations via Intersection Observer
- Smooth scroll, sticky nav with backdrop blur

## Project Structure
- `index.html` — Single-page portfolio (Hero, Case Studies, About, Contact)

## Development
- **Serve locally:** `python3 -m http.server 8080` then open `http://localhost:8080/index.html`
- **Figma capture script** is embedded in index.html (`https://mcp.figma.com/mcp/html-to-design/capture.js`)

## Conventions
- CSS custom properties for all design tokens in `:root`
- Fluid typography using `clamp()` for responsive sizing
- Dark-first design (background `#09090B`)
- **Accent color: `#FF7A5C` (warm coral)** — signature brand color
- Accent secondary: `#FFF1DB` (warm cream)
- Three-font system: Space Grotesk (headings), Inter (body), JetBrains Mono (labels/tags)
- BEM-ish class naming: `.section-header`, `.case-card`, `.hero-cta`
- `.reveal` class + Intersection Observer for scroll animations
- `.stagger` class for sequential child reveals
- Dot grid background overlay on aurora gradient
- Custom cursor: coral dot + delayed ring, expands on hover over interactive elements
- Aurora gradient: 3 animated blobs (coral/warm tones) with 20s drift cycle
- Card hover: 3D tilt (perspective 800px, max 6deg) + accent border glow
- Marquee ticker between hero and case studies with design principles
- Hero text scramble/decode animation on load
- Nav links: animated underline on hover
- `::selection` styled with accent color
- Scroll progress bar: 3px fixed top bar, accent-to-cream gradient, `--scroll-pct` CSS var
- Section dot nav: fixed right edge, 4 dots (hero/work/about/contact), active dot pulses coral with glow
- Kinetic hero typography: scroll-reactive letter-spacing widening + "Kotsar" stroke fill + 0.4x parallax
- Asymmetric case study grid: `1.4fr 1fr` with 3rd card full-width span, directional reveal (odd=left, even=right)
- SVG section dividers: wavy line between all sections, mouse-proximity amplitude (1–8px), phase drift animation, accent glow on approach
- Contact heading: gradient text (`--accent` to `--accent-secondary`) with mouse-tracked angle
- CTA button: radial cursor-following glow (`--mx`/`--my` CSS vars)
- Footer DJ equalizer: 3-bar bounce animation on hover
- Footer "Design lead" hover: accent underline animation
- Touch device fallbacks: cursor hidden, dot-nav hidden, mouse-proximity effects disabled
- Mobile responsive: single-column grid at 768px, smaller container padding

## Installed Skills
- **visual-design-foundations** — Typography, color theory, spacing systems, and iconography principles. Use when refining design tokens, building visual identity, or improving visual hierarchy. Reference files in `~/.agents/skills/visual-design-foundations/references/`.
- **implement-design** — Translates Figma designs into production-ready code with 1:1 visual fidelity. Use when implementing UI from Figma URLs or building components matching Figma specs. Requires Figma MCP server connection.

## Design Changelog
<!-- Track all visual/design changes: colors, typography, spacing, layout, components, identity updates -->
| Date | Change | Details |
|------|--------|---------|
| 2026-02-23 | Initial design | Dark theme, Inter + Space Grotesk, accent `#6E56CF`, 2-column grid layout |
| 2026-02-23 | Body text accessibility fix | `--text-secondary` changed from `#8E8E93` to `#B0B0B8` (~7.5:1 contrast ratio, WCAG AAA) |
| 2026-02-23 | Visual language overhaul: "Structured Warmth" | New accent `#FF7A5C` (warm coral), added JetBrains Mono for labels/tags, fluid typography with `clamp()`, scroll-reveal animations, card hover effects with accent glow, sticky nav with blur, dot grid background, animated underline nav links, pulsing availability dot, experience timeline in About, personal footer touch, `::selection` styling, staggered grid reveals |
| 2026-02-23 | Creative enhancements | Custom cursor (dot + ring with lerp), aurora gradient background (3 animated blobs), 3D tilt cards (perspective + rotateX/Y), marquee ticker strip (design principles), magnetic CTA button, hero text scramble/decode reveal animation. Removed Behance link. |
| 2026-02-23 | Hero redesign: bold centered typography | Removed tag badge, old tagline, CTA button, stats section, magnetic CTA JS. New layout: "Hey! I'm" greeting in JetBrains Mono, massive display name "Maria Kotsar" (clamp 4.5–9rem) with stroke/outline effect on surname that fills with accent on hover, centered description about Manulife role, social links row (LinkedIn/Dribbble/Email). 85vh min-height, vertically centered. |
| 2026-02-23 | 2026 trend integration: "Structured Warmth, Elevated" | 5 enhancements: (1) Scroll progress bar (3px accent gradient) + section dot nav (fixed right, pulsing active dot); (2) Kinetic hero typography (scroll-reactive letter-spacing -0.04→0.08em, progressive stroke fill, 0.4x parallax) with variable Space Grotesk; (3) Asymmetric case study grid (1.4fr 1fr, 3rd card full-width, directional stagger reveals from left/right, 0→0.45s delays); (4) Interactive SVG section dividers replacing flat borders (mouse-proximity wave amplitude 1–8px, slow phase drift, accent glow on approach); (5) Reactive contact CTA (gradient heading with mouse-tracked angle, radial cursor glow on primary button) + personality footer (DJ equalizer bounce animation, design lead accent underline). Added touch/mobile fallbacks, consolidated scroll handler with rAF gating. |

## Figma Publish Log
<!-- Each time something is published from this project to Figma, log it here -->
| Date | What was published | Figma file/link | Notes |
|------|-------------------|-----------------|-------|
| 2026-02-23 | Home page (Hero, Case Studies, About, Contact) | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL) | Dark & minimal style. Placeholder content. Captured via HTML-to-Figma. |
| 2026-02-23 | Updated home page with real content | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL) | Real content from mariakotsar.com: bio, 4 case studies, work history, social links. |
| 2026-02-23 | 2026 trend enhancements capture | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL) | Scroll progress bar, dot nav, kinetic hero, asymmetric grid, SVG dividers, reactive contact CTA, personality footer. |
| 2026-03-09 | Restructured portfolio capture | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=206-813) | New structure: hero + 2 tiles (Watch My Reel + AI Case Study) replacing 4 case study cards, removed marquee ticker. |
| 2026-03-10 | "NEON VOID" redesign — Home (full) | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=212-813) | Full-page capture with all sections visible: hero, work tiles, about/experience, contact, footer. Accessibility fixes applied. |
| 2026-03-10 | "Built With AI" case study (full) | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=213-813) | Full case study page: all 7 sections, tool cards, process timeline, stats, quotes, footer visible. |
| 2026-03-10 | "NEON VOID" Home — full page recapture | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=222-813) | Complete full-page capture with all content visible: hero (MARIA KOTSAR), work tiles, about/experience, contact (LET'S TALK), footer. |
| 2026-03-10 | Component States & Interactions | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=225-813) | 9 component state pairs (default/hover/focus/active): hero name, reel tile, case tile, experience entry, skill tags, contact buttons, gradient heading keyframes, video overlay, footer links. |
| 2026-03-10 | NEON VOID Design System Style Guide | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=226-813) | Full style guide: 10 sections — colors (core + accents + surfaces), typography (3 fonts, full type scale), spacing system, grid/layout, effects/surfaces, borders, all components with states, animation specs, accessibility, iconography. |
| 2026-03-12 | "ATELIER" Plum & Gold redesign — Home | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=234-813) | New ATELIER design: Plum & Gold palette (#CBB674 accent, #734F96 secondary), Instrument Serif headings, floating hero bento cards, case studies "Coming Soon" tile, editorial minimalist layout. |
