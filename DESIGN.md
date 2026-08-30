# Aster reusable landing-page system

## Product and register

- Product: Aster, a fictional guided-learning workspace used to demonstrate a reusable marketing template.
- Primary user: an ambitious learner who feels scattered and wants a clear path forward.
- Primary job: make the product feel emotionally expansive while proving that its interface is concrete and useful.
- Register: expressive marketing page with deterministic product evidence.
- Density: quiet hero, balanced product sections, compact proof and FAQ.

## Visual thesis

For curious people facing an uncertain next step, Aster feels like a warm observatory at the edge of a vast landscape so progress feels discoverable rather than administrative. It prioritizes narrative depth and clarity over decorative spectacle, expressed through layered miniature scenery, editorial serif headlines, precise sans-serif UI, warm mineral color, and one winding path motif. It succeeds when the hero creates wonder and the next scroll immediately proves a credible product.

## Reference ledger

| Exact URL | Observation | Use | Avoid / depart |
|---|---|---|---|
| https://unive.ai/ | Layered panoramic hero, restrained parallax, local proof scrim, deterministic dashboard, alternating feature worlds, comparison, reviews, FAQ, closing CTA. | Section rhythm, still-layer depth, evidence after emotion, purposeful warm palettes. | No Unive name, copy, school setting, people, logos, proprietary UI, or artwork. Aster uses an observatory world, different hierarchy, different product model, and original graphics. |

## High-impact system

### Composition and responsive behavior

- Hero reading order: navigation → eyebrow → headline → support → action → landscape → proof.
- Content width: 1180px; editorial copy measures 12–18 words per line.
- The hero art breaks the content container but preserves a center path and stable copy-safe upper field.
- Desktop uses three panorama layers. Narrow screens use the same alpha masters with stronger center cropping and reduced movement; production reuse can replace them through `<picture>` without changing markup.
- Product proof alternates between wide evidence and focused feature worlds rather than repeating a card grid.

### Typography

| Direction | Choice | Decision |
|---|---|---|
| Neutral neo-grotesk everywhere | System sans | Rejected: too product-generic for the observatory thesis. |
| High-fashion display serif | Didot/Bodoni analogues | Rejected: elegant but too brittle and editorially aloof. |
| Humanist book serif + precise sans | Iowan Old Style / Palatino with Avenir Next / system sans | Chosen: warm narrative voice with reliable interface metrics and no external font dependency. |

### Color, rhythm, and material

- Canvas: warm cream `#f4efe5`; dark field `#15211b`; ink `#17201b`; moss `#485b3e`; coral `#d8755a`; brass `#b28a42`.
- Spacing unit: 4px; section gaps use 24/40/72/112/160.
- Radius vocabulary: 14px controls, 24px product modules, 36px worlds, full pills only for compact labels/actions.
- Elevation comes from tonal surfaces and one soft shadow system; borders define UI evidence.
- Motion uses transform/opacity, restrained deceleration, bounded scroll values, and a zero-motion final state.

## Brand invariants

- Always: keep the path/orbit motif traceable; pair wonder with product evidence; keep live text deterministic.
- Usually: one warm accent per section; large areas remain quiet.
- Only: use glass blur in the floating navigation and proof badge.
- Never: copy Unive assets/copy, generate UI text into imagery, animate every layer, use generic purple SaaS gradients, or hide meaning inside decorative video.

## Proof

- Default viewport: 1440×900.
- Minimum viewport: 390×844.
- Alternate state: reduced motion.
- Pass conditions: no horizontal overflow; readable first action; hero path/focal point visible; all product labels exact; FAQ keyboard-operable; animations preserve final content; decorative media does not carry unique meaning.

