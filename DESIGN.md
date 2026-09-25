---
name: Aegis Guard Gateway
description: "An ink-and-gold ledger interface: near-black chambers, a brass-gold seal accent, serif authority over monospace precision."
colors:
  chambers-ink: "#0A0A0C"
  ink-deep: "#050506"
  ledger-panel: "#131318"
  lit-panel: "#1B1B22"
  code-well: "#08080A"
  hairline: "#29292F"
  hairline-lit: "#3A3A44"
  seal-gold: "#C9A14A"
  bright-gold: "#E4BF6E"
  brass-rule: "#8E6C2E"
  parchment: "#F2EFE9"
  parchment-dim: "#A8A29A"
  parchment-muted: "#6B655D"
  signal-red: "#E85D5D"
  caution-amber: "#E8A33D"
  sage-green: "#5FB58A"
typography:
  display:
    fontFamily: "'Source Serif 4', Georgia, serif"
    fontSize: "clamp(2.4rem, 5.4vw, 4.1rem)"
    fontWeight: 600
    lineHeight: 1.06
    letterSpacing: "-0.015em"
  headline:
    fontFamily: "'Source Serif 4', Georgia, serif"
    fontSize: "clamp(1.75rem, 3.2vw, 2.6rem)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  title:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 700
    lineHeight: 1.4
  body:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  button:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, sans-serif"
    fontSize: "0.92rem"
    fontWeight: 600
  label:
    fontFamily: "'SF Mono', 'Fira Code', 'Fira Mono', 'Cascadia Code', monospace"
    fontSize: "0.72rem"
    fontWeight: 400
    letterSpacing: "0.14em"
rounded:
  xs: "2px"
  sm: "3px"
  md: "4px"
  lg: "6px"
  full: "50%"
spacing:
  xs: "0.5rem"
  sm: "0.75rem"
  md: "1rem"
  lg: "1.5rem"
  xl: "2rem"
  section: "7rem"
  section-compact: "4.5rem"
components:
  button-primary:
    backgroundColor: "{colors.seal-gold}"
    textColor: "{colors.ink-deep}"
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: "0.85rem 1.5rem"
  button-primary-hover:
    backgroundColor: "{colors.bright-gold}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.parchment}"
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: "0.85rem 1.5rem"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.parchment-dim}"
    rounded: "{rounded.sm}"
    padding: "0.65rem 1.1rem"
  card-ledger:
    backgroundColor: "{colors.ledger-panel}"
    textColor: "{colors.parchment-dim}"
    rounded: "{rounded.lg}"
    padding: "1.9rem"
  tag:
    textColor: "{colors.parchment-dim}"
    rounded: "{rounded.sm}"
    padding: "0.35rem 0.7rem"
  tier-badge-prohibited:
    backgroundColor: "rgba(232, 93, 93, 0.12)"
    textColor: "{colors.signal-red}"
    rounded: "{rounded.xs}"
    padding: "0.25rem 0.55rem"
  tier-badge-high-risk:
    backgroundColor: "rgba(232, 163, 61, 0.12)"
    textColor: "{colors.caution-amber}"
    rounded: "{rounded.xs}"
    padding: "0.25rem 0.55rem"
  tier-badge-minimal:
    backgroundColor: "rgba(95, 181, 138, 0.12)"
    textColor: "{colors.sage-green}"
    rounded: "{rounded.xs}"
    padding: "0.25rem 0.55rem"
---

# Design System: Aegis Guard Gateway

This document describes the ink-and-gold system defined in `index.html` and `404.html`.

## Overview

**Creative North Star: "The Chambers Ledger"**

The interface reads as a barrister's record book rendered in a terminal's dark: near-black pages, hairline rules, numbered entries, and one brass-gold accent used the way a seal is used, rarely and to mean something. Source Serif 4 gives headings the gravity of a printed authority. Inter carries running text. Monospace, set small, uppercase and widely tracked, supplies the precision of a register: eyebrows, identifiers, field labels, status.

The mood is rigorous, restrained and forensic. Sections breathe (7rem of vertical rhythm) while the panels inside them are tight, ruled and numbered, so the page alternates between calm and exact. Structure comes from tone and 1px lines, never from decoration. The system rejects the look of a generic cyber-security vendor or gradient-SaaS page.

**Key Characteristics:**
- Near-black ground with tonal layering (Chambers Ink, then Ledger Panel, then Lit Panel); no pure black and no pure white.
- One accent, Seal Gold, plus a four-colour status set used only to signal tier or state.
- Serif headings at weight 600, Inter body, monospace labels; the three roles never blur.
- Sharp corners: 2-3px on controls and badges, 6px on panels.
- Hairline borders carry structure; shadows are rare and structural.
- One easing curve for every transition: `cubic-bezier(0.16, 1, 0.3, 1)`.
- Enumerated content gets mono numerals (01, 02, ...), not icons or emoji.

## Colors

A near-black ledger palette with a single brass-gold accent and a warm, slightly yellow off-white for text. Neutrals lean warm; the accent is the only chroma on most screens.

### Primary
- **Seal Gold** (#C9A14A): the accent. Primary action fills, eyebrow labels, identifiers, numerals, focus outlines, selected states, emphasised words in headings (`em` set upright in gold).
- **Bright Gold** (#E4BF6E): the lit state of Seal Gold. Primary button hover and highlighted hash text; nothing else.
- **Brass Rule** (#8E6C2E): the dim end of the accent. The 2-3px "step" under the primary button, outlines on badges and the hero eyebrow, the gold divider before a major sub-section.

### Secondary
- **Signal Red** (#E85D5D): the Prohibited tier, and inline error text.
- **Caution Amber** (#E8A33D): the High-Risk tier, and the Transitional status border.
- **Sage Green** (#5FB58A): the Minimal tier, and the Active status border and live indicator dot.

The Transparency tier reuses Seal Gold rather than adding a fifth hue.

### Neutral
- **Chambers Ink** (#0A0A0C): the page background. The nav uses it at 86% opacity over a blur.
- **Ink Deep** (#050506): text on gold fills only.
- **Ledger Panel** (#131318): every raised surface: cards, panels, the stat strip, the trust strip.
- **Lit Panel** (#1B1B22): the hover state of a panel row.
- **Code Well** (#08080A): the recessed ground of code samples, inline code and progress tracks.
- **Hairline** (#29292F): default 1px borders and row dividers.
- **Hairline Lit** (#3A3A44): borders on interactive controls, outline buttons and the stat rule.
- **Parchment** (#F2EFE9): primary text.
- **Parchment Dim** (#A8A29A): secondary text and card body copy.
- **Parchment Muted** (#6B655D): tertiary text, captions, unselected mono labels.

### Named Rules
**The Seal Rule.** Solid Seal Gold marks the one thing that matters in a view: the primary action, an identifier, a selected state. Broad areas of gold appear only as ambient wash at 10% opacity or less (the CTA glow, a highlighted card, the selected option), never as a full-strength fill.

**The Tier Signal Rule.** Status colour arrives as a 3px left border or a 12%-tint badge with coloured text. It is never a full-colour block.

**The Warm Neutral Rule.** Text and surfaces come from the ink-to-parchment ramp above. No #000, no #FFF, no cool grey.

## Typography

**Display Font:** Source Serif 4 (with Georgia, serif), loaded 400-700 with the optical-size axis
**Body Font:** Inter (with -apple-system, BlinkMacSystemFont, sans-serif), loaded 400-800
**Label/Mono Font:** the system monospace stack, `'SF Mono', 'Fira Code', 'Fira Mono', 'Cascadia Code', monospace`; no web mono font is loaded

**Character:** A printed-authority serif over a neutral grotesque, with monospace reserved for anything that is an identifier, a label or a value. The serif speaks, the sans explains, the mono records.

### Hierarchy
- **Display** (600, clamp(2.4rem, 5.4vw, 4.1rem), 1.06, -0.015em): the hero headline only, at a maximum width of 780px.
- **Headline** (600, clamp(1.75rem, 3.2vw, 2.6rem), 1.15, -0.01em): section titles. Larger statement headings use clamp(2rem, 4.2vw, 3.2rem) and clamp(2rem, 4.5vw, 3rem) at the same 1.15 line-height.
- **Title** (Inter 700, 1.05rem, 1.4): card and item headings, set in the sans rather than the serif so dense cards stay legible.
- **Body** (Inter 400, 1rem, 1.6): running text. Section lead-ins run 1.05rem at 1.7 and cap at 680px; the hero sub runs 1.15rem at 1.7 and caps at 640px. Card copy is 0.92rem at 1.65.
- **Label** (mono 400, 0.72rem, 0.14em tracking, uppercase, Seal Gold): the eyebrow above every section title and hero. Field labels run the same 0.72rem with 0.06em tracking in Parchment Muted; the smallest badges run 0.62-0.68rem.
- **Stat numeral** (Source Serif 4 600, 2.1rem, line-height 1, Seal Gold): the figures in the stat strip, over a 0.68rem uppercase mono caption.

### Named Rules
**The Three Voices Rule.** Serif for headings and stat numerals, Inter for sentences, mono for identifiers, labels and values. A heading never appears in mono and a value never appears in serif.

**The Tracked Label Rule.** Uppercase mono is always letter-spaced (0.06em to 0.14em). Untracked uppercase mono is not part of the system.

## Layout

A single centred column: content sits in a 1180px container with 2rem side gutters (1rem at 640px and below). The sticky nav is wider on purpose, 1560px, so the full logo, byline and call to action fit at large desktop widths. Sections are separated by 7rem of vertical padding (4.5rem at 720px and below) and by 1px Hairline top borders.

Inside sections, content is grid-based with generous gaps: two-column cards at 1.5rem gap collapsing to one at 820px; five-across registry cards collapsing to three at 1024px and two at 620px; a four-across stat strip collapsing to two at 720px. Anchor scrolling clears the 80px nav (`scroll-padding-top: 92px`).

The nav degrades in stages: byline and badge drop out between 981px and 1499px, the ghost action drops out at 1120px and below, links collapse into a toggle at 980px, and the wordmark drops to an icon at 400px. At 640px and below every button and link target is at least 44px tall. Breakpoints in use: 400, 620/640, 720, 820, 900/980, 1024, 1120 and 1499px.

## Elevation & Depth

Flat and ruled. Depth is conveyed by tonal steps (Chambers Ink, Ledger Panel, Lit Panel) and 1px borders. Shadows are rare, structural, and never decorative; there is no card hover-lift on anything that does not link anywhere.

### Shadow Vocabulary
- **Float** (`box-shadow: 0 30px 80px rgba(0,0,0,0.55), 0 0 0 1px rgba(201,161,74,0.06)`): the code sample panel only, lifted from the page it sits on.
- **Brass step** (`box-shadow: 0 2px 0 var(--gold-dim)`, 3px on hover): the hard, blur-free underline that makes the primary button feel pressable.
- **Point glow** (`box-shadow: 0 0 6px` to `0 0 10px` in Seal Gold or Sage Green): indicator dots only.
- **Nav glass** (`background: rgba(10,10,12,0.86)` with `backdrop-filter: blur(12px)`): the sticky nav.

### Named Rules
**The Flat-By-Default Rule.** Surfaces are flat at rest. A shadow appears only where an element genuinely floats (the code panel), where an action must feel pressable (the primary button), or where a dot must read as lit.

## Shapes

Sharp and small. Badges, eyebrows and tier badges use a 2px radius; buttons, tags, toggles and progress tracks 3px; choice options 4px; cards and panels 6px; dots and step numerals are circles. Nothing is pill-shaped.

Registry-style cards carry a 3px left border in their status colour. Row totals and stat footers are separated by 1px dashed rules in Hairline Lit. Callout notes keep a square left edge with 4px right corners and a 2px Seal Gold left rule. The audit-chain graphic is the one three-dimensional moment and the one 8px exception: 92px square links with a Brass Rule border and a 10% gold wash, alternating a slight Y-axis rotation (-18deg) and straightening and scaling to 1.08 on hover.

## Components

### Buttons
Small-radius, unornamented, one solid action per view.
- **Shape:** 3px radius (`rounded.sm`), 1px transparent border, Inter 600 at 0.92rem; large variant 1rem x 1.75rem padding.
- **Primary:** Seal Gold fill, Ink Deep text, 0.85rem x 1.5rem padding, with the 2px Brass step underneath.
- **Hover / Focus:** primary lifts 1px and brightens to Bright Gold as the step deepens to 3px; outline buttons turn their border and text Seal Gold. All transitions run 0.2s on the shared ease.
- **Outline:** transparent, 1px Hairline Lit border, Parchment text. **Ghost:** Parchment Dim text, 1px Hairline border, 0.85rem type, 0.65rem x 1.1rem padding.
- **Disabled:** 50% opacity, not-allowed cursor, no lift and no step shadow.

### Cards / Containers
Ruled record cards rather than marketing tiles.
- **Corner Style:** 6px.
- **Background:** Ledger Panel, with a 1px Hairline border.
- **Signature variant:** Brass Rule border and a 160-degree wash from 6% Seal Gold into Ledger Panel.
- **Registry variant:** 3px left border in the status colour (Sage Green active, Caution Amber transitional, Parchment Muted upcoming).
- **Shadow Strategy:** none; see Elevation.
- **Internal Padding:** 1.9rem for content cards, 1.5rem for score and registry cards, 1.25rem for grid cells.

### Inputs / Fields
Underlined, mono, and quiet.
- **Style:** transparent ground, no box; a 1px Hairline Lit bottom border, mono 0.82rem text, right-aligned in key/value rows over a 0.72rem uppercase label.
- **Focus:** the bottom border turns Seal Gold; the outline is removed only where that border change replaces it. Free-text payload areas take a 3% Seal Gold wash instead.
- **Choice options:** a 1px Hairline Lit bordered row, 4px radius, with an 8px radio dot. Checked: Seal Gold border, 8% gold wash, filled dot. Keyboard focus: a 2px Seal Gold outline with 2px offset.
- **Error:** mono 0.75rem in Signal Red, set directly under the field.

### Navigation
- **Style:** sticky, 80px tall, Nav glass background with a 1px Hairline bottom border; serif 1.3rem wordmark beside a 0.62rem mono badge with a Brass Rule outline.
- **Links:** Inter 0.86rem in Parchment Dim, brightening to Parchment on hover over 0.15s.
- **Mobile treatment:** below 980px the links become a full-width stacked panel behind a 40px toggle (44px at 640px and below), each row separated by a Hairline.

### Tags and Badges
- **Tag:** mono 0.72rem, Parchment Dim, 1px Hairline Lit border, 3px radius.
- **Tier badge:** mono 0.62rem bold uppercase, 0.06em tracking, 2px radius, a 12% tint of the tier colour behind full-strength text of that colour (Prohibited, High-Risk, Transparency, Minimal).

### Stat Strip (signature)
A Ledger Panel band between two Hairlines: four columns, each with a 2px Hairline Lit left rule, a Seal Gold serif numeral and a muted uppercase mono caption.

### Code Panel (signature)
Code Well ground, 1px Hairline Lit border, 6px radius, the only Float shadow in the system. A mono title bar sits over a Hairline with three inert 9px dots. Syntax uses Seal Gold for keywords, Sage Green for strings, Parchment Muted for comments and Bright Gold bold for the emphasised token.

## Do's and Don'ts

### Do:
- **Do** keep one solid Seal Gold action per view; every other action is outline or ghost.
- **Do** run every transition on `cubic-bezier(0.16, 1, 0.3, 1)`.
- **Do** set eyebrows, field labels and identifiers in tracked uppercase mono.
- **Do** number enumerated sets with mono numerals (01, 02, ...) in Seal Gold.
- **Do** signal status with a 3px left border or a 12%-tint badge.
- **Do** give every touch target at least 44px at 640px and below, and honour `prefers-reduced-motion` for any entrance animation.
- **Do** describe depth with tone and 1px lines first; reach for a shadow last.

### Don't:
- **Don't** use #000, #FFF or a cool grey; stay on the warm ink-to-parchment ramp.
- **Don't** fill large areas with Seal Gold at full strength; wash at 10% or less.
- **Don't** add a second accent hue; the only other chroma is the tier status set, and only for status.
- **Don't** add hover-lift or pointer affordances to cards that do not link anywhere.
- **Don't** use emoji or decorative icons to stand in for a numbered set.
- **Don't** use the browser-default `ease` keyword.
- **Don't** round beyond 6px (the 8px audit-chain link is the single exception), set headings in mono, or set a value in serif.
- **Don't** use gradient text or gradient-SaaS glows; a single 10% ambient wash is the ceiling.
