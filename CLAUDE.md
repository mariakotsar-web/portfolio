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
- Light design (background `#F4F2EC` cream paper, ink `#1A1812`) — flipped from dark `#0E0F0E` on 2026-05-24
- **Accent color: `#7B8CFF` (periwinkle)** — signature brand color
- Accent companion: `#C9B3FF` (lavender) — gradient blob secondary
- Acid yellow `#E8FF3D` kept as a token but no longer used (the "About me" intro block is now periwinkle, not yellow)
- Four-font system: Inter (body/display), Fraunces (italic serif display, "Maria"), Newsreader (serif fallback), JetBrains Mono (labels/tags)
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
| 2026-05-04 | "Soft Dark / Acid Yellow" pivot — Home rewrite from Claude Design handoff | Full visual pivot: paper `#0E0F0E`, accent acid yellow `#E8FF3D`, Inter + JetBrains Mono only (Instrument Serif removed). Hero: "Hi, I'm Maria. I make ~~complex~~ systems feel *human.*" with strike-through accent bar on "complex" + italic "human." 3-tile bento work grid (payments app feature, "off the canvas" hobbies card with snowboarding SVG / piano / DJing chips, coming-soon wide). Footer: scrolling "EMAIL ME ✦ COFFEE? ✦ DM ME" marquee, 3 pill social links with arrow puck, back-to-top circle. ATELIER design (DJ mode, drawing easter egg, polaroid, fun-fact card) replaced wholesale. Tweaks panel skipped. |
| 2026-05-18 | "Periwinkle Glass" pivot — Home rewrite from Claude Design handoff | Accent shifted acid yellow → **periwinkle `#7B8CFF`** with lavender companion `#C9B3FF` for gradient blobs. Yellow `#E8FF3D` retained only as the intro section contrast block. Fonts added: **Fraunces** (italic display) + **Newsreader** (serif fallback). Hero replaced with editorial wide layout: massive "Hi, I am *Maria*" name (Maria in Fraunces italic, clamp 72→240px), 3-column body (left blurb · empty centerpiece · right blurb), vertical 33%/66% guide lines, two animated periwinkle/lavender gradient blobs with 20–22s drift, scroll-parallax. Nav rebuilt as **sticky transparent** with center-positioned glass pill (Work/About/Contact) and accent **Resume** pill+puck (opens in new tab). On scroll a liquid-glass panel fades in; over the yellow intro section the nav swaps to `on-light` dark text. New full-bleed yellow **"A little about me"** contrast section between hero and work (paragraph + meta strip). **Liquid-glass** (Apple-style frosted) applied to nav links, footer social pills, and back-to-top. Footer marquee retained, copyright line "Vibecoded with Claude · Toronto". **Loading splash** with pulsing periwinkle dot. Scroll-reveal via `data-reveal` + IntersectionObserver. Mobile breakpoints at 980/560px. Work bento grid (payments / hobbies / coming-soon) preserved with periwinkle accent throughout (including hobbies SVG snowboarding scene). |
| 2026-05-18 | Periwinkle Glass — recent-changes patch | (1) Hero gradient blobs now **follow cursor**: pointermove handler with rAF-throttled 120px range, blob 1 tracks cursor, blob 2 drifts opposite, smooth 900ms cubic-bezier translate easing; disabled on touch (`pointer: coarse`). (2) Intro section dividers (left rail, row separators, mobile top rail) lightened to **`#E0E0E0`** for cleaner contrast on yellow. (3) Nav: **"Work" link removed**; only About and Contact remain (Contact still anchors to the footer where Email/LinkedIn/Dribbble live). |
| 2026-05-24 | "Periwinkle Glass — Light" pivot + Projects/About rebuild (from Claude Design handoff `Home.html`) | Implemented the latest Claude Design handoff into `index.html`. **Theme flipped dark → light** (user-confirmed): paper `#F4F2EC` cream, ink `#1A1812`, surfaces `#ECE9E0` / `#D7D3C5` hairlines; periwinkle `#7B8CFF` accent retained. **Intro/About block** now periwinkle (was acid yellow). **Hero blobs** upgraded to drift + morph + breathe (3 parallel animations, `b3` reserved/hidden), blend `screen`→`normal` for light visibility. **Nav**: pulsing ✦ glyph (was dot circle), added **Projects** link, **Resume pill removed** (per handoff). **About** rebuilt: tag "About me", new copy (Big 4 / FMCG emphasis), "How I work" values list (ringed checkmarks), experience **timeline** (Manulife Financial Corporation / Trinetix / DataArt, external links new tab). **Projects** section added (single **Generative AI Portal** card, placeholder cover, `href="#case-gen-ai"`); **work bento hidden** (`display:none`, kept in markup). Footer pills re-tuned for light + real contact links (marykotsar@gmail.com · linkedin.com/in/maria-kotsar · dribbble.com/marykotsar). Case study page (`Generative AI Portal.html`) is in the bundle but not yet implemented. |

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
| 2026-03-13 | Latest ATELIER with DJ mode & updates | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=248-813) | Updated hero ("Hello, I'm Maria"), drawing easter egg, DJ mode toggle, polaroid photo, fun fact card, mobile fixes, deployed to GitHub Pages. |
| 2026-05-04 | "Soft Dark / Acid Yellow" Home — full page | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=321-2) | Full Home capture from `design-handoff/project/Home.html`: nav, hero (strike-bar "complex" + italic "human."), 3-tile bento (payments / off-the-canvas hobbies / coming-soon), Where I've worked experience list (Manulife / Trinetix / DataArt), footer marquee + pill socials. Captured via HTML-to-Figma capture script. |
| 2026-05-18 | "Periwinkle Glass" Home — full page | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=474-2) | Initial capture from current `index.html`. Superseded by node-id=478-2 (full body re-capture). |
| 2026-05-18 | "Periwinkle Glass" Home — full body re-capture | [Portfolio-2026](https://www.figma.com/design/mbDADywgFdeKdLsB8k2OBL?node-id=478-2) | Full-page capture from current `index.html` using `figmaselector=body` + 3.5s delay so splash, hero blobs, and scroll-reveal animations all settle. Sticky transparent nav (About · Contact + Resume pill), hero "Hi, I am *Maria*" + cursor-following periwinkle/lavender gradient blobs, full-bleed yellow "A little about me" intro with `#E0E0E0` dividers, work bento (payments / hobbies / coming-soon), liquid-glass footer (Email/LinkedIn/Dribbble pills + marquee + back-to-top). |
