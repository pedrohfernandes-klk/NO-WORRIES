# NO WORRIES

A one-minute, browser-based audiovisual installation — an independent short film trapped inside a browser, where search behaviour, sound, language, weather, figures and system pressure become one escalating event.

It opens on the phrase **NO WORRIES**. You hold a button to begin. For sixty seconds you move forward through a hazy liminal hall, meeting silhouetted figures who are gradually watched, selected and targeted, while a private search box types familiar, banal queries whose suggestions drift quietly toward dread. The phrase **NO WORRIES** crashes down twice as a failing system slogan, language glitches and morphs, the field floods with noise — then the storm recedes and the screen returns, quietly, to **NO WORRIES / WHAT REMAINS / YOU ARE HERE NOW**.

> **Photosensitivity warning:** this piece contains sustained flashing, strobing, glitch and high-contrast motion, especially in its final third. It is not suitable for viewers with photosensitive epilepsy.

---

## Run it

It is a **single, self-contained `.html` file**. There is no build step, no server, no dependencies.

- **Locally:** double-click the file, or open it in any modern browser.
- **Projection / gallery:** open it, press **GO**, and let it play fullscreen (`F11` on most desktop browsers).
- **Sound is essential.** The piece is sound-led; play it with audio on. Browsers require a user gesture before audio can start — the press-and-hold on **GO** provides that gesture, so audio unlocks reliably on every run, including restarts.

Everything — code, fonts and audio — is embedded directly in the file as text and base64. You can copy it to a USB stick, email it, or host it as a static page; it will behave identically.

---

## Controls

| Action | What it does |
| --- | --- |
| **Press & hold GO (~1s)** | Begins the piece and unlocks audio. The same hold gesture is used to start and to replay. |
| **MUTE** (top corner) | Toggles sound. Small and unobtrusive by design. |
| **GO** (end screen) | Replays from the beginning. Audio restarts cleanly with no duplicated loops. |

The piece is designed to loop reliably: every restart resets the timeline, the figures, the search box, the title bursts and the audio graph from scratch.

---

## What's inside

- **A 60-second authored timeline** — calm "eye", system field, corridor, target field / broken broadcast, and a cleared afterimage.
- **A scrolling liminal hall** — receding pillars, streaming orbs, fog at the vanishing point and a perspective interior floor, all rendered to `<canvas>` and scrolling toward the viewer so you feel you are moving through the space.
- **Rim-lit figures** that approach from depth, are acquired by targeting reticles, and dissolve into rising ash — understated, systemic, never video-game-like.
- **A two-tier phrase system.** A few bold messages resolve clearly in reserved, non-overlapping lanes; behind them a faint ghost layer thickens into a confusing private-noise wall as the narrative escalates. Phrases sometimes glitch and morph into other phrases.
- **A realistic search box.** The typed query stays familiar and banal; the dropdown suggestions escalate in dread while never resolving into anything specific. Shameful private searches — adult, crypto, betting — flash by for a fraction of a second as ghosts.
- **A generative audio engine** built on the Web Audio API: a vast, airy, near-empty bed early that floods into confusion and rupture late, with two huge **NO WORRIES** drops and a collapse-then-regenerate ending.

---

## Technical notes

- **Stack:** plain HTML, CSS and JavaScript. No frameworks, no libraries, no build tooling.
- **Rendering:** a single full-screen `<canvas>` (2D context) for scenery, figures and atmosphere; the DOM for the title bursts, phrases, search card and HUD.
- **Audio:** the Web Audio API, with a bus mixer, generative percussion/noise/impact synthesis and a handful of embedded source tracks. Levels are shaped continuously across the timeline.
- **Typography:** Archivo (Black) and IBM Plex Mono are embedded as base64 `woff2` `@font-face` so the piece looks identical on any machine, online or offline.
- **Self-contained:** all audio and fonts are base64-embedded. No external CSS, JS, audio, image or font requests are made at runtime.

### Large screens, 4K and TV / casting

The installation is hardened for big displays and for casting to a TV:

- **No clipped or overlapping text on any aspect ratio.** Phrase sizes are capped against viewport **height**, so the relationship between glyph height and the layout lanes is constant whether the display is 16:9, ultrawide, 4K or a letterboxed cast signal. Rows cannot collide and letters cannot cut, regardless of screen shape.
- **Overscan-safe HUD.** The timer and mute control are kept clear of the screen edges that many TVs crop.
- **Performance on cast devices.** The canvas backing store is capped (~4.2M pixels) so 4K TVs and Chromecast-class hardware stay smooth, while normal displays render at full resolution.

> Tip for casting: where possible, **cast the browser tab from a desktop/laptop** (the source machine does the rendering) rather than relying on a low-power streaming stick to render the page itself. Always play with audio enabled.

### Browser support

Designed for current Chrome, Edge, Safari and Firefox. It relies on standard, widely-supported features (Canvas 2D, Web Audio, CSS `clamp()`/`min()`, pointer events). A modern browser from 2020 onward is recommended.

---

## Project structure

```
no_worries_impact.html   # the entire installation — open this
README.md                # this file
```

That's it. One file is the whole work.

---

## Verifying a build

If you edit the file, a few quick checks before showing it:

- It opens locally and the **GO** button starts the piece.
- The full 60-second sequence plays and the ending appears.
- **GO** on the end screen restarts cleanly — audio restarts, with no duplicated loops or stacked timers.
- JavaScript passes a syntax check.
- It reads correctly at several window shapes (try a normal 16:9 window, a very wide/short window, and a large 1440p/4K display) with no cut or overlapping text.

---

## Credits & license

Concept and direction by the author. Built as a self-contained web installation.

Embedded typefaces are open-source: **Archivo** and **IBM Plex Mono** (SIL Open Font License). Add your chosen license for the work itself here (e.g. `LICENSE` file).
