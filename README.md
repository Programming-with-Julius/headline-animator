# Headline Animator

Create a fast headline montage with one steady focal point. The text and typography change while a shared keyword stays centered on the stage.

**[Open the live editor](https://programming-with-julius.github.io/headline-animator/)**

![Animated headlines changing around the centered keyword AI on a black stage.](docs/headline-animator.gif)

## Features

- Keep the first matching keyword centered in every headline.
- Mix font families, weights, styles, sizes, letter spacing, and text transforms.
- Cycle headlines in random or sequential order, with adjustable FPS and crossfade duration.
- Choose a black or white stage and set its height.
- Pause the animation and use **Reroll now** to inspect another combination.

## Using it

1. Open the [live editor](https://programming-with-julius.github.io/headline-animator/), or open [`index.html`](index.html) in a browser.
2. Set **Keyword** and enter **Headlines**, one per line. Include the keyword in each headline you want to align.
3. Edit the typography lists below the stage. Each line is one available option.
4. Adjust **FPS**, **Crossfade (ms)**, and **Stage height (vh)**. Toggle **Random order**, **Paused**, or **White stage** as needed.
5. Screen-record the top stage area for clean output. **Reset defaults** restores the starting controls.

Use **Paused** to check the framing: long headlines or large fonts can extend beyond the stage. The supplied headlines are editable demo text.

## How it works

The editor measures the first keyword match and translates the entire headline until that keyword sits at the stage center. A second hidden layer prepares the next frame, and the two layers crossfade to keep the montage moving smoothly.

Everything lives in a single HTML file. There is no build step or application server; the editor styling loads Bootstrap from a CDN.

## Related tool

[`network-animator`](https://github.com/Programming-with-Julius/network-animator) creates glowing network diagrams with animated connections and PNG export.

## Project note and license

> Fully vibe-coded, does not reflect me as a developer.

MIT. See [`LICENSE`](LICENSE).
