[Fully vibe-coded, does not reflect me as a developer]

# headline-animator

Live demo: https://programming-with-julius.github.io/headline-animator/

`headline-animator` is a single-file HTML tool that recreates a rapid “headline flicker” effect where many different headlines share a single keyword (e.g. `AI`). Each frame is rendered with a different typographic preset, but the keyword is always positioned at the same spot on screen (centered) by measuring the keyword’s bounding box and translating the whole headline accordingly.

To avoid visible jumps or dark frames, the animation uses a double-buffer approach: the next headline is laid out and aligned while hidden, then crossfaded in while the previous frame fades out.

## Features

- Keyword-locked positioning (the shared keyword is centered every frame)
- Rapid cycling at a configurable FPS
- Double-buffered crossfade to prevent flashes/jitter
- Editable lists for:
  - headlines
  - font families
  - weights, styles, sizes
  - letter spacing and text transform
- Controls for FPS, crossfade duration, random vs sequential order, pause
- Black/white stage toggle
- Stage area is reserved at the top so you can screen-record clean output

## Usage

1. Open the live demo link above, or open `index.html` locally in a browser.
2. Edit the options in the textareas (one option per line) and tweak the numeric inputs/toggles.
3. Record only the top stage area for clean captures.

## How it works (high level)

- The current headline string is converted into HTML where the first keyword match is wrapped in a dedicated `.anchor` span.
- The next frame is rendered into a hidden layer (back buffer), measured, and translated so the `.anchor` is centered in the stage.
- Once positioned, the back buffer is made visible and crossfaded in while the front buffer fades out.

## License

MIT. See `LICENSE`.
