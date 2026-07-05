# Stanzi Studio — Site

**`index.html` is the entire site** — fully self-contained (inline CSS + JS, logos embedded as base64 data URIs). No build step, no backend. Deploy the single file anywhere, or just open it in a browser.

> `styles.css`, `main.js`, and `logos/` are leftovers from the v1 multi-file build — `index.html` no longer references them. Kept per no-delete rule; safe to archive. (`logos/` mono PNGs are still the source files for the embedded logos.)

## Design system (v3)

- **Palette — strict two-color.** Deep navy `#05070F` base, `#0A0E1C` lifted panels. Warm off-white `#F4F1EA` at 100% (headlines) / 55% (sublines) / 35% (meta, eyebrows). Hairlines `rgba(244,241,234,0.10)`. No black, no gray, no accent color anywhere.
- **Type.** Display: **Archivo** variable (Google Fonts), weight 900, `font-variation-settings: "wdth" 112` (semi-expanded — the wide muscular-grotesque look), `-0.02em` tracking, via the shared `.display` class. Oswald for tracked-out sublines/labels, Inter for rare body.
- **Hero.** "STANZI STUDIO" single line, centered, fills viewport width; wraps to a balanced two-line stack only on narrow screens (`text-wrap: balance`).

## Page order (v4 copy — systems-architect positioning, no kitchen framing)

Hero → tagline → **What We Do** (Ventures / Systems & Ops / Brand & Growth / Software w/ Opstable named) → marquee → **How We Work** ("We don't advise. We operate.") → In-House Ventures → **Selected Work** ("Operators trust us to build.") → About ("Based in Miami. Built on systems.") → Talent Pool (secondary CTA, mailto w/ subject) → **Become a Client** ("Let's make your idea reality." — the dominant CTA) → footer.

Positioning rule: restaurants are evidence, not identity. No chef/kitchen/craftsman language.

## Logos

Embedded as base64 (mono, CSS-inverted to off-white): **Barrio, Brightline, Kiki, Pucci, SCAD**. Sources: `~/Downloads/stanzi-logos-package/mono/`.

Text placeholder slots (`.logo-slot` spans, labeled via `title`): Stanzione 87, Ash Pizza, Thoroughbred, Stanzione Italian Specialties, Opstable, Art Basel, HKTB, The Foundry, Sunshine Coffee, Mutto, MB Botanical Garden. Swap: `base64 -i logo.png`, replace the span with `<img src="data:image/png;base64,..." alt="Name">`.

## Open items

- Brightline consulting scope is a guess ("Hospitality operations consulting") — search `TODO` in `index.html`.
- Footer social links are `#` placeholders (IG / X / LinkedIn).
