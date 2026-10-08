---
name: STRATUM
description: Calm industrial intelligence, expressed through purple surfaces and expansive real photography.
colors:
  ink: "#282032"
  paper: "#faf9fc"
  white: "#fff"
  muted: "#68606f"
  line: "#ddd7e4"
  acid: "#d9c9f2"
  purple: "#7042a0"
  violet-dark: "#302340"
  focus: "#8255be"
  reel-surface: "#f0edf4"
  industry-surface: "#eee9f4"
  diagram-surface: "#eee8f5"
  closing-surface: "#e2d5f1"
  hero-button: "#e6d5ff"
  hero-button-hover: "#f3eaff"
  button-hover: "#66428e"
  button-disabled: "#6e6179"
  recommendation: "#f4eef9"
  sidebar: "#f5f1f8"
  asset-hover: "#eae2f3"
  status-surface: "#ece1f8"
  status-text: "#563075"
typography:
  display:
    fontFamily: "Manrope, sans-serif"
    fontSize: "clamp(3.3rem, 6.3vw, 5.6rem)"
    fontWeight: 400
    lineHeight: 1.07
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "Manrope, sans-serif"
    fontSize: "clamp(2.6rem, 5.3vw, 5rem)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.04em"
  body:
    fontFamily: "Manrope, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  button:
    fontFamily: "Manrope, sans-serif"
    fontSize: "14px"
    lineHeight: 1.5
rounded:
  tab: "4px"
  outline-link: "5px"
  title-plaque: "6px"
  panel: "8px"
  container: "12px"
  pill: "30px"
spacing:
  page-gutter: "clamp(24px, 5.4vw, 88px)"
  section-block: "110px"
  mobile-section-block: "70px"
  mobile-gutter: "24px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
    padding: "13px 27px"
    typography: "{typography.button}"
  button-primary-hover:
    backgroundColor: "{colors.button-hover}"
  button-hero:
    backgroundColor: "{colors.hero-button}"
    textColor: "{colors.violet-dark}"
    rounded: "{rounded.pill}"
    padding: "13px 27px"
  button-disabled:
    backgroundColor: "{colors.button-disabled}"
    textColor: "{colors.white}"
  reel-tab-selected:
    backgroundColor: "{colors.purple}"
    textColor: "{colors.white}"
    rounded: "{rounded.tab}"
    padding: "9px 15px"
---

# Design System: STRATUM

## Overview

STRATUM combines the supplied Palantir reference's topic tabs and oversized photographic panels with Mercury's centered, calm sans-serif hero and rounded controls. The user's purple direction is authoritative. Industrial scale comes from real refinery, wind-turbine, and open-pit mining photographs; clarity comes from generous spacing, restrained typography, and explicit controls.

This is a descriptive record of `dist/styles.css`, `dist/index.html`, and `dist/app.js`. Resolve the entire CSS cascade, including the appended “Reference blend” rules: earlier hero positioning, square buttons, and header rules are superseded. PRODUCT.md records the invented brand and synthetic demo context.

- Expansive photography with dark plum overlays.
- Warm off-white and lavender surfaces, purple selected states.
- Regular-weight Manrope headlines, limited semibold utility text.
- Calm rounded controls alongside crisp dividers and operational data.

## Colors

The normative palette above preserves source CSS values. `--acid` is the incumbent variable name for pale lavender, not a green accent. `--lavender: #eee7f6` is declared but currently unused; do not mistake it for a rendered surface.

Primary purple marks selected reel tabs and text-link hover. Ink is the main text and standard dark button color; violet-dark anchors the perspective section and photographic panel fallback. Paper covers the page and light panels; muted supports descriptive text, while line separates rows and cards. The closing section has its own stronger lavender surface.

Additional component colors: header `rgba(37,27,47,.89)` with `#ffffff20` border; logo icon `#dfc9fc`; header CTA `#f7f0ff` with `#ddc5fa` hover; inactive reel tabs `#faf8fd` / `#716579`; reel outline link border `#94869f`; reel plaque `#382645eb` and link `#e6d4fa`; reel arrows `#302340aa` / `#ffffff77`; perspective body `#d3c9df`. Diagram rules use `#d1c5df`, `#cbbbdc`, `#bba2d4`, and `#e7dfee`, with secondary diagram text `#685877`.

Hero overlay: `linear-gradient(180deg,rgba(34,21,49,.52),rgba(37,19,56,.5) 50%,rgba(27,16,40,.55))`. Reel overlay: `linear-gradient(180deg,#3320450d,#2b16393d)`. Preserve image legibility and white text contrast when changing photography.

## Typography

Use self-hosted Manrope: regular TTF at 400 and semibold TTF declared for 600–800, both `font-display:swap`; fallback is sans-serif. There is no separate serif or monospace family. Headings use balanced wrapping and regular weight.

| Role | Desktop treatment | At ≤700px |
| --- | --- | --- |
| Hero | Frontmatter display; max-width 1050px | `clamp(2.6rem,9.6vw,4rem)` |
| Section h2 | Frontmatter headline | Same fluid clamp |
| Story h3 | 32px / 1.08, −.04em | 28px |
| Reel h2 | `clamp(2rem,3.2vw,3rem)` / 1.15, −.03em | 29px |
| Industry h3 | `clamp(2rem,3.5vw,3.2rem)` | 36px |
| Perspective h2 | `clamp(2.5rem,3.6vw,3.5rem)` | 38px |
| Closing h2 | `clamp(2.8rem,5.8vw,5.5rem)` | 44px |
| Hero supporting text | 18px / 1.5 | 16px |
| Body | 16px / 1.6, maximum 65ch | Section supporting copy 15px |
| Data readings | 23px, regular, tabular numerals, −.03em | 18px |

Utility text is typically 12–14px; industry description and evidence copy are 15px. Section-heading description uses 1.7 line-height and max-width 470px; story description max-width is 450px. Desktop header wordmark is 22px / 600 with .04em tracking, becoming 19px at ≤1000px. Asset names and demo brand use 600; data values remain 400.

## Layout

Shared gutter is `clamp(24px,5.4vw,88px)`. Sections use 110px block padding. At ≥1600px, sections, header, footer, and the unused sector-strip selector receive horizontal padding `max(var(--space),calc((100vw - 1500px)/2))`; later header padding overrides this for the header. Do not implement a new global max-width wrapper based on this rule.

Header floats absolutely at top 20px, left/right 24px, height 72px, padding 0 28px, z-index 10. It is not sticky. Hero is 90svh, min-height 690px, max-height 950px; centered content starts at 175px and reserves 110px below. Photograph uses cover and `center 59%`. The hero caption sits on a bottom divider. Hero body and CTA form a centered column with 27px gap.

Reel section uses 70px top / 80px bottom padding. Tabs and outline link share a row with 30px space before the 570px-tall image panel. Plaque is inset 25px, max-width 560px, padding 26px 30px. Bottom controls sit 25px from bottom, 30px from left, 25px from right.

Section-heading grid is `1.2fr 1fr`, gap 80px, margin-bottom 70px. Platform grid is two equal columns with 9vw gap. Industry grid is `1.1fr 1fr`, min-height 490px, image max-height 560px, copy padding 50px. Demo grid is `270px 1fr`, detail padding 36px. Readings stay in three equal columns. Perspective is two equal columns, image max-height 650px, text padding 80px by the shared gutter. Closing is a horizontal flex composition.

At ≤1000px: major grid gaps become 40px; industry copy 32px; demo rail 220px; detail padding 25px; detail title stacks; perspective text 55px 35px; reel panel 500px. Footer wraps.

At ≤700px: ordinary sections become 70px 24px; section-heading, platform, industry, demo, and perspective become one column. Section-heading gap is 28px and bottom margin 38px. Header becomes top/left/right 14px, height 62px, padding 0 17px; navigation becomes a toggle-controlled overlay below it. Hero becomes 85svh with 650px minimum and 950px maximum inherited from the later base rule; content padding 150px 24px 85px; image position `57% center`. Hero caption's second span is hidden. Reel padding is 40px 20px 45px, panel 460px; top controls stack, tabs stay on one row and share width; plaque is inset 16px with 22px padding. Industry image is 280px tall and copy padding 28px. Asset selector becomes a horizontal row; secondary small labels hide; detail padding is 22px 17px. Perspective image is 340px tall, copy padding 55px 24px. Closing and footer stack.

## Elevation & Depth

Surfaces use tonal separation, borders, and translucent image plaques; there are no box shadows. Hero text retains `text-shadow:0 2px 20px #14252c33`. Hero and reel establish isolated stacking contexts with full-cover images and overlays. Avoid adding floating card shadows to the operational sections.

## Shapes

Use 30px pill radii for primary actions; 12px for header, asset diagram, industry panel, demo frame, and status badge; 8px for reel, recommendation, and selected asset row; 6px for reel plaque and mobile menu; 4px for reel tabs; 5px for the outline reel link. Reel arrows are 42px circles. Borders are generally 1px; selected industry tabs use a 2px underline. Asset-core top and asset-record bottom corners are 8px. Inline icons use 1.5px strokes and no fill.

## Components

**Buttons and links.** Standard buttons have 49px minimum height, 13px 27px padding, transparent 1px border, and .2s background/color transitions. Light buttons use paper/ink and lavender hover; hero uses its special lavender pair. The demo review button is smaller: 40px minimum height, 9px 16px, 12px text. Disabled review buttons use the explicit disabled palette and default cursor. Text links have a bottom border and 8px bottom padding; header/footer links underline on hover.

**Topic reel.** Three tab buttons drive one photographic panel; changing selection updates image, alt text, title, link label, count, and panel label. Arrow buttons wrap cyclically. No automatic advance. Inactive tabs are quiet pale rectangles; selected tab is purple with white text. All reel links currently lead to the working example.

**Industry tabs.** Three underlined text tabs update a shared image/copy panel and three capability rows. Desktop gap is 40px with 34px below the tab strip; mobile gap 16px and labels at 12px. Both tabsets use `role=tablist/tab/tabpanel`, `aria-selected`, `aria-controls`, dynamic `aria-labelledby`, and roving tabindex; Left/Right wrap and Home/End select endpoints.

**Asset diagram.** Lavender rounded container, minimum 520px desktop / 490px mobile, joins three source tags through thin lavender connectors into an ink core and paper asset record. It is explanatory, not interactive.

**Operational demo.** A bordered white frame combines a pale sidebar, selected white asset row, three readings, evidence tags, and lavender recommendation block. Asset buttons expose `aria-pressed`; changes update a polite live region. “Mark as reviewed” stores state per asset in a page-session `Set`, disables the button, and displays a status confirmation. Reload resets it. Preserve the visible synthetic-data disclosure. There are no inputs or backend persistence.

**Disclosure and navigation.** Capability rows use native `details/summary`, top dividers, and plus/minus indicators; the first is initially open and multiple can stay open. Mobile menu is 44px square, toggles `aria-expanded` and its label, closes after navigation, and supports Escape with focus returned to the toggle. Desktop CTA hides at ≤700px.

**Accessibility and motion.** Keep the skip link, landmark labels, descriptive image alt text, text status labels, and native buttons. Keyboard focus uses a 3px solid focus-purple outline with 5px offset. Hero image is high priority; below-fold images are lazy-loaded. Hero image settles for 1.5s using `cubic-bezier(.16,1,.3,1)`, scaling 1.04→1 and saturation .5→1 before resting at its CSS saturation .65. Reduced-motion preference disables all animations/transitions and switches smooth scroll to auto. Anchor offset is 88px desktop and 20px mobile. This documents implemented behavior, not a formal accessibility certification.

## Do's and Don'ts

- Do retain the centered calm hero, purple palette, real industrial imagery, and oversized tabbed reel as the defining blend.
- Do derive new screens from the final cascade and these role-specific values.
- Do use whitespace and typography to distinguish marketing narrative from the denser operational demo.
- Do preserve keyboard behavior, focus visibility, reduced-motion support, and truthful concept/sample-data labeling.
- Don't restore the superseded green/charcoal direction or left-aligned cinematic hero.
- Don't introduce invented customers, numerical outcomes, production commitments, or copied reference-brand assets.
- Don't turn this visual system into generic shadowed cards, ornamental dashboards, or autoplay imagery.
