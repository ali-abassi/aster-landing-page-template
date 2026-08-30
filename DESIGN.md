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
| https://unive.ai/ | Rating pill above the headline; layered panoramic hero at ~94dvh; press row over the artwork; deterministic dashboard; six features as a 3x2 card grid (389x447 cards, tinted panel + cropped mockup, name and description below); comparison; a dense review wall; FAQ; closing CTA. Whole page 7,747px at 1440x900. | Section rhythm, still-layer depth, evidence after emotion, proof inside the first fold, compact feature grid, review density, warm purposeful palettes. | No Unive name, copy, school setting, people, logos, proprietary UI, or artwork. Aster uses an observatory world, its own product model, and original graphics. |

## Reference contrast after rendered QA

| Design subject | Unive observation | Aster v1 defect | Aster decision |
|---|---|---|---|
| Hero reading aperture | The central headline, support line, and action sit entirely above the detailed landscape. | The observatory dome climbed into the lede and secondary action. | Lower the architectural plane, keep the horizon below the action row, and reserve the upper field for live copy. |
| Scale hierarchy | Display type is large once, then settles to a materially smaller product-section scale. | Three consecutive sections repeated near-hero headline scale. | Preserve the expressive hero, compress the promise into a bridge band, and cap the workspace heading at 4.75rem. |
| Proof cadence | Emotional scenery hands off quickly to a concise platform introduction and product screenshot. | The promise section delayed the dashboard with another near-full-screen statement. | Reduce bridge padding and dashboard offset so product evidence enters the next viewport. |
| Media coherence | One cohesive scenic composition hides the mechanics of its depth treatment. | Separate alpha planes exposed their construction when focal objects shared the copy zone. | Give horizon, architecture, and foreground distinct resting positions and narrower motion ranges; composition must work before parallax. |
| Visual language | Restrained monochrome interface and one pastoral metaphor foreground the product claim. | Warm editorial typography, multiple accent colors, and fantasy scenery competed at equal intensity. | Keep Aster's more expressive observatory identity, but ration coral and use quieter product-section typography and spacing. |

## Second cross-reference, after measuring the reference

| Design subject | Unive measurement | Aster v2 defect | Aster decision |
|---|---|---|---|
| Page budget | 7,747px total at 1440x900. | 13,062px — six full-bleed feature worlds spent ~6,000px on content the reference delivered in 1,359px. | Collapse the six worlds into one 3x2 grid. Page now 9,387px, with the expressive hero and review density intact. |
| Feature anatomy | 389x447 card: tinted panel, product mockup cropped by the panel edge, then name and 3-line description below. | Alternating left/right copy beside a 640px stage, one section each. | Adopt the card anatomy verbatim in structure; keep Aster's original stages and palette as the content. |
| Hero height | `h-[94dvh]` — viewport-relative, so the landscape meets the fold at any height. | Fixed 1080px; at 1280x720 only 338px of artwork was visible and the proof bar never entered the first fold. | Track viewport height with `clamp(980px, calc(880px + 24svh), 1130px)`, verified so the artwork clears the CTA at every tested viewport. |
| Social proof placement | Rating pill sits above the headline. | Rating lockup sat at the hero's base, 1,032px down — below the fold at every desktop size. | Move the rating to a pill above the headline; leave the press row over the artwork. |
| Review volume | ~17 short reviews in a dense multi-column wall. | Four large cards in a horizontal rail. | A 12-review, three-column masonry wall with one featured card. |

## High-impact system

### Source artwork

The three hero panoramas were generated with OpenAI's image generation, prompted for transparent-background (alpha) plates rather than one flat picture — a separate plate per depth plane (horizon, midground, foreground). The parallax only reads as depth because the plates are separable and carry real transparency; a single generated image cannot produce the see-through relationship between near foliage and distant mountains. Masters are kept locally as PNG and shipped as WebP.

### Composition and responsive behavior

- Hero reading order: navigation → eyebrow → headline → support → action → landscape → proof.
- Content width: 1180px; editorial copy measures 12–18 words per line.
- The hero art breaks the content container but preserves a center path and stable copy-safe upper field.
- Desktop uses three panorama layers. Narrow screens use the same alpha masters with stronger center cropping and reduced movement; production reuse can replace them through `<picture>` without changing markup.
- Product proof runs wide first (the dashboard), then compact: six features in a 3x2 grid of tinted panels, each holding one scaled product stage above its name and description.
- Each feature stage is authored at a fixed 620x560 and scaled into its card through `--stage-scale`, so stage internals never need re-tuning per breakpoint.
- Social proof appears twice: a rating pill above the headline (always inside the first fold) and a press row over the artwork at the hero's base.

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

Checked at 1440×900, 1440×780, 1280×720, 1280×633, 834×1112, 390×844, and 320×568.

Pass conditions, all currently green:

- No horizontal overflow at any viewport or scroll depth.
- The primary action sits inside the first fold.
- The hero artwork reaches the fold and its opaque mass clears the action row (measured by alpha sampling, not bounding box — the panoramas carry wide transparent margins).
- Navigation is reachable at every width; below 1000px through a menu that opens, closes on Escape, on link choice, and on outside click.
- FAQ is keyboard-operable; no decorative control sits in the tab order.
- Reduced motion leaves no revealed element stranded at zero opacity.
- No console errors and no failing requests across a full-page scroll.
