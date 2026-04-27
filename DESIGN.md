---
name: The Solo Founder Playbook in the AI Era
description: A 20-slide Reveal.js speaker deck by Ron Zaidman — bold, practical, direct.
colors:
  signal-blue: "#42affa"
  pipeline-teal: "#2aa198"
  slide-bg: "#ffffff"
  body-text: "#222222"
  terminal-surface: "#1e1e1e"
typography:
  display:
    fontFamily: "Source Sans Pro, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(1.98rem, 6.075vw, 4.95rem)"
    fontWeight: 700
    lineHeight: 1.06
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Source Sans Pro, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(1.37rem, 3.53vw, 2.66rem)"
    fontWeight: 600
    lineHeight: 1.14
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Source Sans Pro, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(0.78rem, 1.4vw, 1.1rem)"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "Source Sans Pro, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(0.62rem, 0.95vw, 0.82rem)"
    fontWeight: 500
    letterSpacing: "0.12em"
  mono:
    fontFamily: "'JetBrains Mono', 'Fira Code', 'Courier New', monospace"
    fontSize: "clamp(0.65rem, 1.1vw, 0.9rem)"
    lineHeight: 1.7
rounded:
  sm: "4px"
  md: "6px"
  lg: "8px"
  xl: "10px"
  full: "50%"
spacing:
  slide-padding: "clamp(1.25rem, 4vw, 4.5rem)"
  content-gap: "clamp(0.6rem, 2vw, 2rem)"
components:
  highlight-box:
    backgroundColor: "rgba(66,175,250,0.08)"
    textColor: "#e0e0e0"
    rounded: "{rounded.md}"
    padding: "clamp(0.5rem, 1.2vw, 0.9rem) clamp(0.75rem, 1.8vw, 1.4rem)"
  highlight-box-teal:
    backgroundColor: "rgba(42,161,152,0.08)"
    textColor: "#2aa198"
    rounded: "{rounded.md}"
    padding: "clamp(0.5rem, 1.2vw, 0.9rem) clamp(0.75rem, 1.8vw, 1.4rem)"
  stack-card:
    backgroundColor: "rgba(255,255,255,0.04)"
    textColor: "#e0e0e0"
    rounded: "{rounded.md}"
    padding: "clamp(0.6rem, 1.4vw, 1.2rem)"
  stack-card-hover:
    backgroundColor: "rgba(255,255,255,0.04)"
    textColor: "#e0e0e0"
    rounded: "{rounded.md}"
    padding: "clamp(0.6rem, 1.4vw, 1.2rem)"
  accent-tag:
    backgroundColor: "transparent"
    textColor: "#42affa"
    rounded: "{rounded.sm}"
    padding: "0.3em 0.9em"
---

# Design System: The Solo Founder Playbook in the AI Era

## 1. Overview

**Creative North Star: "The Builder's Stage"**

This is a stage built by someone who builds things, for an audience of people who build things. The design earns trust through precision and restraint — not decoration. Every typographic decision, every color application, every spacing choice is functional. There is no scaffolding to hide behind. The slides hold up under a developer's gaze because they were made with a developer's eye.

The clean white canvas is a neutral container that refuses to compete with the content. The two accent colors carry all the expressive work: Signal Blue is active and forward-moving (connections, data, the new thing), Pipeline Teal is confirmed and complete (the validated state, the lesson learned, the destination reached). Neither is used casually. The one place the system goes dark is the terminal block — a deliberate surface shift that signals "this is real output from a real agent."

This system explicitly rejects the aesthetic of its own anti-reference: generic AI-generated slide decks. No gradient text. No hero-metric number cards with glowing accents. No glassmorphism panels. No identical icon-heading-text card grids. No flat gradient backgrounds. The test is simple: if someone could guess the template from the category name alone, it has failed.

**Key Characteristics:**
- White canvas, two purposeful accent colors, dark body text
- Flat by default; accent-tinted backgrounds and hairline borders define surfaces, not shadows
- Fluid type scale via `clamp()` — legible from 1080p to a phone without breakpoint hacks
- Staggered entrance animations on slide load, expo-out easing only
- Content-first layout: the slide chrome (header/footer bars) is deliberately quiet so the content dominates
- Monospace code blocks as a visual affordance — the terminal is a first-class component

## 2. Colors: The Signal Palette

Two accent colors, one substrate. Neither accent is decorative; both are semantic.

### Primary
- **Signal Blue** (`#42affa`): The active state color. Applied to accent text, bullet markers (▸), timeline dots, category tags, slide-tag labels, and any element that represents connection, action, or forward movement. At 6–8% opacity over dark, it creates the highlight box tint.

### Secondary
- **Pipeline Teal** (`#2aa198`): The verified/complete color. Used for "after" column labels, the final timeline destination, the teal highlight box variant, terminal prompt text, and any element representing a validated state or lesson confirmed. Distinctly cooler and calmer than Signal Blue.

### Neutral
- **Slide Background** (`#ffffff`): Pure white from the Reveal.js simple theme. The neutral container — never altered.
- **Body Text** (`#222222`): Near-black from the Reveal.js simple theme. Primary reading text on white slides.
- **Terminal Surface** (`#1e1e1e`): The one dark surface in the system. Used exclusively for the terminal/code block, signalling "this is real agent output, a different surface type."
- **Terminal Text** (`#e0e0e0`): Near-white text, used only inside the terminal block on its dark background.
- **Text Muted** (≈ 45% opacity applied to body text): Slide numbers, footer labels, card category lines. Applied via `opacity`, not a separate color token.
- **Border Subtle** (`rgba(0,0,0,0.08)` on light surfaces): Hairline borders on cards and split columns. Very low contrast — structural, not decorative.

### Named Rules
**The Two Voices Rule.** Signal Blue and Pipeline Teal are never used interchangeably. Blue is active, forward. Teal is verified, complete. A slide can carry one or both — but not mixed randomly. A "before/after" split always puts blue on the before side and teal on the after side.

**The Opacity Doctrine.** Surface tints (backgrounds for cards, highlight boxes, orbs) use opacity — never a pre-mixed flat color. `rgba(66,175,250,0.08)` reads differently across dark substrates; that variation is intentional and alive.

## 3. Typography

**Display Font:** Source Sans Pro, Helvetica Neue, Arial, sans-serif (via Reveal.js simple theme)
**Body Font:** Source Sans Pro (same stack — single typeface system)
**Label/Mono Font:** JetBrains Mono, Fira Code, Courier New (terminal blocks only)

**Character:** A single humanist sans at multiple weights does all the work. The weight contrast (400 body / 600 headline / 700 display) is the hierarchy — not different typefaces, not decorative rules. The monospace appears only in the terminal component, where it is semantically correct, not merely stylistic.

### Hierarchy
- **Display** (700, `clamp(1.98rem, 6.075vw, 4.95rem)`, line-height 1.06, tracking -0.02em): Title slide only. Tight leading and negative tracking make it commanding at projection scale.
- **Headline** (600, `clamp(1.37rem, 3.53vw, 2.66rem)`, line-height 1.14, tracking -0.01em): Per-slide section title (`.slide-title`). Followed by a 2px accent rule (Signal Blue, 1.8rem wide) that acts as a visual anchor.
- **Body** (400, `clamp(0.78rem, 1.4vw, 1.1rem)`, line-height 1.5): Bullet list items, descriptive text, card body copy.
- **Lead** (400, `clamp(0.88rem, 1.7vw, 1.2rem)`, line-height 1.6, 70% opacity): Introductory or supporting sentences below the headline. Not a heading, not a bullet.
- **Label** (500, `clamp(0.62rem, 0.95vw, 0.82rem)`, tracking 0.12–0.14em, uppercase): Slide numbers, category tags, section labels, card category lines. Never used for body copy.
- **Mono** (400, `clamp(0.65rem, 1.1vw, 0.9rem)`, line-height 1.7): Terminal block only. JetBrains Mono preferred.

### Named Rules
**The One Typeface Rule.** The entire presentation uses one typeface family (Source Sans Pro). Visual hierarchy is achieved through weight and size contrast alone — never through mixing families. The monospace exception is semantic (code/terminal), not decorative.

**The No-Gradient-Text Rule.** Type is rendered in solid colors only. `background-clip: text` with a gradient is prohibited. Emphasis is communicated through weight (700), color (Signal Blue), or size — never through CSS gradient overlays.

## 4. Elevation

This system is flat by default. Surfaces are defined by `1px` borders and opacity-based background tints, not by shadows. Shadow is structural, not decorative — it appears only on photographic images to lift them slightly off the dark substrate.

### Shadow Vocabulary
- **Image lift** (`box-shadow: 0 4px 24px rgba(0,0,0,0.4)`): Applied to all `<img>` elements inside slide content. Provides physical separation from the slide background without visual noise. No other elements receive this treatment.
- **Timeline glow** (`box-shadow: 0 0 0 3px rgba(66,175,250,0.2)`): The focus ring-style glow on zigzag timeline dots. Soft, halo-like. Not a lift shadow — purely an accent aura.

### Named Rules
**The Flat-By-Default Rule.** UI elements (cards, highlight boxes, tags, split columns) are flat at rest. Depth is communicated through border opacity and background tints. If you feel like adding a box-shadow to a card or a container, reconsider — the answer is almost always a border-color change or a tint increase instead.

**The Image Exception.** `box-shadow: 0 4px 24px rgba(0,0,0,0.4)` is reserved for photographic images only. It is a structural affordance that separates photography from the slide substrate, not a decorative style applied to UI surfaces.

## 5. Components

### Slide Chrome (Header + Footer)
The structural frame that wraps every slide. Deliberately quiet — it never competes with content.
- **Shape:** Full-width bars, flush to edges, no radius
- **Header:** `1px solid rgba(255,255,255,0.12)` border-bottom; slide number (Label, 45% opacity) left; slide tag (Label, Signal Blue, uppercase) right
- **Footer:** `1px solid rgba(255,255,255,0.12)` border-top; speaker name left; event name right; both at 45% opacity
- **Internal padding:** `clamp(0.75rem, 1.5vw, 1.2rem)` vertical, `var(--slide-padding)` horizontal

### Highlight Box
The primary callout component. Used for key insights, takeaways, and framing statements.
- **Shape:** Gently curved (6px radius)
- **Blue variant:** `rgba(66,175,250,0.08)` background, `rgba(66,175,250,0.25)` border, `#e0e0e0` text at semi-bold
- **Teal variant:** `rgba(42,161,152,0.08)` background, `rgba(42,161,152,0.30)` border, Pipeline Teal (`#2aa198`) text
- **Padding:** `clamp(0.5rem, 1.2vw, 0.9rem)` vertical, `clamp(0.75rem, 1.8vw, 1.4rem)` horizontal
- **Usage:** Never nest inside another highlight box. One per slide maximum.

### Stack Card
The tool/stack grid card. Used for the tech ramp-up slide (6-card grid).
- **Shape:** 6px radius
- **Background:** `rgba(255,255,255,0.04)` — barely-there tint on the dark substrate
- **Border:** `1px solid rgba(255,255,255,0.12)` at rest; `rgba(66,175,250,0.40)` on hover
- **Internal:** Category label (Label, 55% opacity, uppercase), tool name (Body weight 700, Signal Blue), sub-line (Small, 45% opacity)
- **Hover transition:** `border-color 0.25s ease` — the only state change; no lift, no shadow

### Accent Tag
Inline badge for event/series labeling.
- **Shape:** 4px radius, `1px solid rgba(66,175,250,0.4)` border
- **Background:** Transparent
- **Text:** Signal Blue, Label scale, uppercase, 0.1em tracking, weight 500
- **Usage:** Title slide only. Not to be used as a general-purpose chip or category label.

### Bullet List
The primary text content component. Used across most content slides.
- **Marker:** `▸` (Unicode triangle), Signal Blue, `flex-shrink: 0`
- **Spacing:** `clamp(0.45rem, 1vh, 0.9rem)` between items
- **Text:** Body scale, line-height 1.5
- **No-arrow variant:** Emoji or no marker, used for emotional/human-voice bullets (the "how does it feel" slide)

### Terminal Block
The code/agent output component. Appears on the analytics example slide.
- **Background:** `#1e1e1e` — distinct from slide substrate to signal "different surface"
- **Border:** `1px solid rgba(255,255,255,0.10)`, 10px radius
- **Window bar:** Three macOS-style dots (`#ff5f57`, `#febc2e`, `#28c840`), 6px gap, `1px solid rgba(255,255,255,0.08)` border-bottom
- **Font:** JetBrains Mono, `clamp(0.65rem, 1.1vw, 0.9rem)`, line-height 1.7
- **Color roles:** Prompt → Pipeline Teal; Command → Soft White; Comment → `#6a737d` (muted gray); Output → `#4ec9b0` (bright teal)
- **Usage:** Represents real agent/CLI output. Do not use for decorative code display.

### Zigzag Timeline
The biography component. Used on the About Me slide.
- **Layout:** 3-column CSS grid: `1fr clamp(20px, 2.5vw, 28px) 1fr` — left content / center spine / right content
- **Spine:** Dots (circular, Signal Blue, 3px inset glow ring) connected by thin vertical lines (`2px`, gradient from Signal Blue at 45% to 5% opacity)
- **Final item:** Teal dot (larger, 4px glow ring), teal-tinted background, teal text — marks the current/destination state
- **Text:** Category label (Label, Signal Blue, 65% opacity), role (Body, weight 500)

## 6. Do's and Don'ts

### Do:
- **Do** keep the slide background white (Reveal.js simple theme default). The white canvas is a neutral container; it is not a design choice to revisit for any individual slide.
- **Do** use Signal Blue (`#42affa`) for active/forward-moving elements and Pipeline Teal (`#2aa198`) for verified/complete states. Keep the semantic distinction.
- **Do** use `clamp()` for every font size and spacing value. The presentation must be legible from 1080p projection to a phone without a separate responsive breakpoint.
- **Do** animate with `opacity` + `transform: translateY()` only, eased with `cubic-bezier(0.16, 1, 0.3, 1)`. Stagger delays in 0.1s increments.
- **Do** apply `box-shadow: 0 4px 24px rgba(0,0,0,0.4)` to all photographic images. This is the only shadow in the system.
- **Do** use `prefers-reduced-motion` overrides — already wired; keep them in any new CSS added.
- **Do** cap text content at one primary idea per slide. The audience has seconds, not minutes.

### Don't:
- **Don't** use gradient text (`background-clip: text` with a gradient background). This is an absolute ban. Use Signal Blue solid, or Soft White solid, or Pipeline Teal solid. No exceptions.
- **Don't** use glassmorphism panels — `backdrop-filter: blur()` on card-like surfaces. This is a generic AI slide aesthetic this deck explicitly refuses.
- **Don't** create identical icon-heading-text card grids. The stack grid on slide 12 works because the tool names are the content — not decorative icons. Any new card grid must have a reason beyond filling space.
- **Don't** use hero-metric number cards (big number, small label, gradient accent). This is the canonical SaaS cliché this deck explicitly refuses.
- **Don't** add a `box-shadow` to UI components (cards, containers, highlight boxes). Shadows belong on images only. UI depth comes from borders and tints.
- **Don't** use `border-left` or `border-right` greater than `1px` as a colored accent stripe on cards or list items. The `.vision-quote` left-border (2px solid Pipeline Teal) is the one documented exception — it is a blockquote affordance, not a card decoration pattern.
- **Don't** produce any slide that looks like it was assembled from a Canva template in ten minutes. If the design could be described by its category alone ("dark tech startup deck"), revisit it.
- **Don't** mix the two accent colors randomly. Blue is active; teal is complete. A before/after split is always blue-before, teal-after.
- **Don't** use animation on CSS layout properties (`width`, `height`, `padding`, `grid-template-columns`). Animate only `opacity` and `transform`.
