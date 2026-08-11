# Novara Materials — Design System

> Built to disappear. Designed to deliver.

This project is the design system for **Novara™ Materials**, an advanced materials company that makes ultra-thin, flexible **heating and protective** technologies. It contains the brand's color and type foundations, the official logo, reusable React UI components, a marketing-site UI kit, and a slide-template set — everything needed to produce on-brand interfaces, decks, and assets.

The compiler bundles the components into a runtime library (`window.NovaraMaterialsDesignSystem_4f47f9`) and indexes the tokens. The **Design System tab** renders every `@dsCard`-tagged HTML file in the project.

---

## Source materials

Built from the supplied brand assets:

- **`uploads/NOVARA LOGO - FINAL.png`** — primary lockup (layered mark + black wordmark) → `assets/novara-logo.png`
- **`uploads/NOVARA LOGO - WHITE.png`** — white wordmark for dark backgrounds → `assets/novara-logo-white.png`
- **`uploads/NOVARA LOGO - COLOR-01.png`** — all-red lockup → `assets/novara-logo-red.png`
- The **layered-sheets mark** was cropped from the primary lockup → `assets/novara-mark.png`
- **`uploads/NOVARA LOGO AND COLORS-...pdf`** — brand sheet defining the palette.
- **`uploads/Novara Master Messaging Framework_Final.docx`** — the master messaging framework (pillars, mission/vision, positioning, audience messaging, taglines, voice & tone, boilerplate). This drives the **Content fundamentals** below.
- **`uploads/Novara_SeriesA_June2026.pptx`** — the real Series A investor deck (18 slides). The exemplar for the **Slides** templates and the source of the product specifics, real metrics, and the live data-viz palette (red `#EF4638`, near-black `#1A1A1A`, success green `#3DBE7A`, amber `#F5A623`). Three images were extracted from it → `assets/img-cnt.jpg` (CNT lattice render), `assets/img-facility.jpg` (entrotech cleanroom, de-rotated), `assets/img-applications.jpg` (ember-glow heated walkway/bench).

**Confirmed palette:** Brand red `#EF4638` (PMS 179C, from the brand sheet) · Black `#000000` · Gray `#989898` · Gray light `#CCCCCC`. *(The Series A deck uses a slightly warmer red `#EF4638` in practice; the brand sheet value is treated as canonical `--brand`, and the deck's exact green/amber were adopted for status/data-viz tokens.)*

No codebase, Figma file, or font files were supplied. Typography and the extended color ramps are brand-consistent extensions; the logo, product positioning, copy, metrics, and slide imagery are drawn from the supplied assets. See **Caveats**.

---

## Company & product context

**Novara™** is an advanced materials company based in **Columbus, OH**. Its core technology is **carbon-nanotube (CNT) thin-film heaters** — the "HeatCoat" platform originating from **Battelle** (65+ patents, >$60M of Battelle + USAF R&D) and manufactured on **entrotech's** $70M roll-to-roll thin-film facility. The films are ~10 mil thick, ~1.2 oz/ft², run from 6VDC to 480VAC, and deliver uniform heat at ~90% less weight and ~50% less power than nichrome wire.

The brand frames this customer-side as the **performance layer** — "ultra-thin, flexible heating and protective technologies that integrate seamlessly inside other companies' products." Marketing/messaging speaks of a platform of **thermal / protective / adaptive layers**:

- **Thermal layer** — uniform CNT heat on any surface, low energy demand.
- **Protective layer** — durable, dependable protection for performance and safety.
- **Adaptive layer** — ultra-thin, flexible film that conforms to complex parts.

**Who they sell to:** OEMs, ODMs, and product-development / innovation teams.
**Markets (per the Series A deck), by horizon:** Consumer / foodservice (now — delivery bags, flameless chafers, outdoor furniture) · Architecture (2–3 yrs — snow/ice melt, hangar radiant heat) · Mobility (3–4 yrs — EV battery warming, seat/cabin; Hyundai-HATCI & BorgWarner traction) · Aerospace / energy (5+ yrs — surface de-icing, wind-turbine protection; Honeywell, GE).

**Core brand pillars:** Precision · Flexibility · Protection · Excellence · Trust.
**Mission:** *"We enable products to perform better and last longer, bringing trusted warmth, protection, and performance to every surface…"*
**Purpose:** *"to transform how the world makes and uses heat."*

(Specific metrics and customer names come from the supplied Series A deck. The customer-facing "layer" framing comes from the messaging framework.)

---

## Content fundamentals (voice & copy)

Sourced from the master messaging framework. How Novara writes:

- **Tone:** professional, approachable, knowledgeable. **Voice:** clear & authentic (avoids jargon, focuses on performance and value), confident, respectful. Confident — never hype, no exclamation marks, no emoji.
- **Casing:** **sentence case** for body and UI; headline taglines are written as crisp two-beat statements with periods (*"Built to disappear. Designed to deliver."*).
- **Person:** "we" / "Novara"; addresses customers as "you" / "your products" / "your systems."
- **The "invisible but invaluable" theme** is central: the product *disappears* into the customer's product while delivering performance. Lead with seamless integration, warmth, protection, design freedom, and efficiency — not raw specs.
- **Recurring vocabulary:** *seamless, integrate, ultra-thin, flexible, any surface, warmth, protection, performance, durability, design freedom, every layer, invisible.* Prefer **"warmth"** (approachable) alongside "heat."
- **Modular message format:** Headline + Subhead + Support point + Proof.

**Signature lines (use verbatim):**
- Primary descriptor: *"Advanced materials that deliver seamless warmth and protection to any product."*
- Taglines: *"Built to disappear. Designed to deliver."* · *"The performance layer behind what's next."*
- Audience headlines: OEM — *"Performance where it matters. Seamless where it doesn't."* · ODM — *"Heat. Protect. Perform."* · Product developers — *"Build better from the inside out."*
- CEO sound bite: *"At Novara, we make the invisible, invaluable."*

**Boilerplate:** *"Novara™ is an advanced materials company based in Columbus, OH, delivering ultra-thin, flexible heating and protective technologies that power breakthrough product performance…"*

---

## Visual foundations

**Color.** A single hot **brand red (`#EF4638`, "ember")** against a deep neutral **"carbon"** ramp (brand grays + black). Red is used sparingly and with intent — the logo mark, a heat field, one CTA — never as large flat fills. Neutrals carry the bulk of every surface. Status colors (green/amber/azure) are muted and kept distinct from the brand red; *danger* uses a deepened red so it doesn't read as "brand."

**Logo & mark.** The lockup is the **layered-sheets mark** (light-gray / red / dark-gray offset sheets — literally "every layer") + the rounded **NOVARA** wordmark. Three official variants: black wordmark (light bgs), white wordmark (dark bgs), all-red. The mark alone works as a bug/favicon and reads on both light and dark. Use the `Logo` component; never recolor or redraw the mark.

**Type.** Three families for a precise yet approachable feel:
- **Display / headings — Space Grotesk** (700/600), tight tracking. *(The official wordmark is a softer rounded geometric face — see Caveats.)*
- **Body / UI — Archivo** (400/500/600), 16px base, 1.55 line-height.
- **Mono / data — Space Mono** for figures, units, and uppercase eyebrows (`.novara-overline`).

**Backgrounds.** Mostly flat — white (`--surface-page`) or near-black `#1A1A1A`. The signature flourish is the **"heat field"**: a soft radial ember gradient bleeding from a corner of dark sections (hero, CTA, cover slide). Avoid bluish-purple gradients — the only gradient is ember-red on carbon.

**Imagery.** Three flavors, all in `assets/` (from the Series A deck): (1) **science** — the CNT lattice glowing orange/red on pure black (`img-cnt.jpg`); use full-bleed behind dark, technical sections. (2) **product-in-context** — photoreal scenes with an **ember-orange heat glow** rendered into cold/snowy environments (`img-applications.jpg`); the warmth-in-cold motif. (3) **facility** — bright, clean, white roll-to-roll cleanroom (`img-facility.jpg`); credibility/scale. Photography is warm-accented (ember glow) against cool/neutral environments; pair with a dark scrim when overlaying text.

**Shape & elevation.** Restrained, industrial — *not* bubbly. Card radius tops out at 10px (`--radius-lg`), controls at 6px (`--radius-md`). Borders are crisp 1px hairlines. Shadows are low-spread, cool carbon (`--shadow-sm → xl`). A single warm **`--glow-ember`** exists for rare heat moments — use almost never.

**Motion.** Quick and mechanical. 120–360ms on `--ease-standard`. Fades + short rises for modals; buttons nudge down 0.5px on press. No bounces or decorative loops.

**Interaction states.** Hover: primary → darker, secondary/ghost → subtle carbon tint, cards lift 2px. Press: darkest + 0.5px translate. Focus: 3px ember ring (`--ring`). Disabled: 50% opacity.

**Transparency & blur.** Two places only: the sticky nav (blurs once scrolled) and the modal scrim (~55% carbon). Otherwise opaque.

**Layout.** 1200px max width, 32px gutters, 4px spacing base, ~96px section rhythm. Data framed with vertical hairline dividers rather than boxes.

---

## Iconography

- **System:** [**Lucide**](https://lucide.dev) — clean, 2px-stroke, rounded-join line icons; approachable yet precise. Loaded from CDN and wrapped by `ui_kits/website/Icon.jsx` (`<Icon name="layers" size={22} />`).
- **No bundled icon font or SVG sprite** was supplied; Lucide is a flagged substitution chosen for stroke-weight fit.
- **Emoji:** never used.
- **The brand mark** (`assets/novara-mark.png`) — the layered sheets — is the only bespoke glyph; used as a logo bug, never as a UI icon.
- Pick icons with literal meaning (`layers`, `shield-check`, `thermometer-sun`, `car-front`, `building-2`, `stethoscope`). Avoid playful or abstract icons.

---

## Index / manifest

**Foundations**
- `styles.css` — root entry (import this one file). `@import`s everything below.
- `tokens/colors.css` · `typography.css` · `spacing.css` · `effects.css` · `base.css`
- `guidelines/*.card.html` — foundation specimen cards (Colors, Type, Spacing, Brand).

**Assets**
- `assets/novara-logo.png` · `novara-logo-white.png` · `novara-logo-red.png` — official lockups.
- `assets/novara-mark.png` — layered-sheets mark.
- `assets/img-cnt.jpg` · `img-facility.jpg` · `img-applications.jpg` — brand imagery (from the Series A deck).
- `components/brand/logoData.js` — the lockups inlined as data URIs for the `Logo` component.

**Components** (`window.NovaraMaterialsDesignSystem_4f47f9`)
- `components/brand/` — **Logo**
- `components/core/` — **Button, IconButton, Badge, Tag, Avatar, Card, StatCard**
- `components/forms/` — **Input, Textarea, Select, Checkbox, Radio, Switch**
- `components/feedback/` — **Alert**
- `components/navigation/` — **Tabs**
- Each has `.jsx`, `.d.ts`, `.prompt.md`; each directory has one `@dsCard` card.

**Templates** (consumer starting points)
- `templates/landing-hero/` — **Landing hero** (`LandingHero.dc.html`), a Design Component importing the system's Logo + Button.

**UI kits**
- `ui_kits/website/` — Novara marketing homepage (interactive: nav, smooth-scroll, request-a-sample modal). See its `README.md`.

**Slides** (modeled on the Series A deck)
- `slides/*.card.html` — six 1280×720 templates: cover, section divider, metrics/proof, technology split, comparison table, market timeline. Eyebrow + big colored stat callouts + ✓ tables + "Proprietary & Confidential" footers.

**Skill**
- `SKILL.md` — makes this system usable as a downloadable Agent Skill.

---

## Caveats

- **Fonts:** no brand font files were provided. Space Grotesk / Archivo / Space Mono are a **flagged Google Fonts substitution** (CDN `@import` in `tokens/typography.css`). The official **NOVARA wordmark is a softer rounded geometric typeface** that the headline font (Space Grotesk) doesn't perfectly match — *if you'd like headings to echo the wordmark, share the brand typeface and I'll swap the display family (e.g. to a rounded geometric like the wordmark).*
- **Extended color ramps** (ember 50–900, carbon 0–1000) were derived to harmonize with the confirmed brand colors — confirm they're acceptable. Status/data-viz tokens (green, amber) were matched to the Series A deck.
- **The deck uses Calibri/Arial**; this system sets slides in the brand display/body fonts (Space Grotesk / Archivo) for an elevated, consistent direction while keeping the deck's structure (eyebrows, stat callouts, ✓ tables, confidential footers). Say the word if you'd rather the templates match the deck's exact typeface.
- **Website UI kit** is the customer-facing brand site built from the messaging framework (thermal/protective/adaptive "layers"); the **slides** carry the investor-facing specifics (CNT, Battelle, entrotech, real metrics) from the Series A deck.
