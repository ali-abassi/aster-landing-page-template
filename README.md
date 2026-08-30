# Aster landing-page template

An original reusable homepage study derived from the structural lessons of Unive—not its branding, copy, UI, or artwork.

## Preview

```sh
python3 -m http.server 4173 --directory .
open http://localhost:4173
```

## Reuse

1. Replace brand copy and links in `index.html`.
2. Change palette, type, spacing, radii, and section rhythm through the tokens at the top of `styles.css`.
3. Replace the three alpha hero masters in `assets/`; retain their filenames or update the three `<img>` elements.
4. Add or remove `data-reveal` and `data-parallax` attributes without changing the animation engine.
5. Keep exact UI, text, charts, and controls in HTML/CSS/SVG. Reserve generated images or MiniMax video for organic media plates.
6. If adding decorative video, follow the source-selection hook documented in `script.js`: poster first, skip video for reduced motion/data saver, and load only the chosen viewport source.

The template has no runtime dependencies or build step.

