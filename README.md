# NO WORRIES

A one-minute, browser-based audiovisual installation: an independent short film trapped inside a single HTML file.

**NO WORRIES** turns politeness, search behaviour, sound, weather, social pressure, passive aggression, silhouetted figures and a changing sun into one escalating event. It begins with candid optimism — light, routine, the possibility of a good day — then slowly converts that optimism into dread, pressure, accusation, system language, refusal and collapse.

The work is designed as a projection-grade browser piece: part audiovisual poem, part liminal corridor, part private search history, part failed social script.

## Description

The piece opens on **NO WORRIES**.

You hold **GO** to begin. For sixty seconds, the viewer moves through a hazy liminal space where phrases appear like fragments of overheard thought, small social injuries, automated messages, old disappointments, polite evasions and things people almost said.

At first the language is familiar and hopeful: a normal morning, a clean day, a small plan. Then the phrases become stranger: missed meanings, indirect blame, soft refusals, passive-aggressive courtesy, social exhaustion and system pressure. A search box appears with banal, recognisable queries whose suggestions drift toward dread. Figures approach from depth. Some are watched, selected and targeted. The phrase **NO WORRIES** crashes down as a failing slogan.

The sun remains present across the whole piece. It begins as a bright, almost naïve morning sun, then gradually reddens, sickens and becomes infernal. Near the end, it ruptures into a blast of light before the storm clears back to **NO WORRIES** and **GO**.

The loop is simple: **GO / NO WORRIES / GO**.

## Photosensitivity warning

This piece contains sustained flashing, strobing, glitch effects, high-contrast motion, rapid text changes and bright light bursts, especially in the final third.

It is not suitable for viewers with photosensitive epilepsy or strong sensitivity to flashing light.

## Run it

This is a single, self-contained `.html` file.

There is:

* no build step
* no server requirement
* no external dependencies
* no external font, image, audio, CSS or JavaScript requests at runtime

To run locally, double-click the HTML file or open it in any modern browser.

For projection or gallery use, open the file, switch the browser to fullscreen, press and hold **GO**, and let the sixty-second sequence play.

Sound is essential. The piece is sound-led: the audio, impacts, noise beds, search pulses and final rupture are part of the structure, not decoration. Browsers require a user gesture before audio can start; the press-and-hold **GO** interaction provides that gesture, including on replay.

Because everything is embedded directly in the HTML file, the work can be copied to a USB stick, emailed, archived or hosted as a static page.

## Controls

| Action                     | What it does                                    |
| -------------------------- | ----------------------------------------------- |
| Press and hold **GO**      | Begins the piece and unlocks audio.             |
| **MUTE**                   | Toggles sound. Small and unobtrusive by design. |
| **GO** on the final screen | Replays the piece from the beginning.           |

The work is designed to restart cleanly. Each replay resets the timeline, phrase field, search card, title bursts, figures, sun state and audio graph.

## What is inside

### A 60-second authored timeline

The piece moves through distinct emotional phases:

1. candid optimism
2. early unease
3. pressure and self-management
4. social miscommunication
5. passive-aggressive injury
6. institutional/system language
7. refusal
8. inferno/blow-up
9. cleared afterimage

### A narrative sun

The sun is not just background scenery. It functions as an emotional clock:

* early: bright, hopeful, almost innocent
* middle: warmer, unstable, increasingly wrong
* late: red, infernal, hostile
* final: rupture, blast, afterimage

### A phrase system

The phrase bank is phase-weighted. It mixes:

* familiar half-said sentences
* social fragments
* passive-aggressive formulations
* small domestic hostilities
* “sad but true” hard truths
* system messages
* refusal language
* final quiet residue

The phrases are not intended as quotes. They behave like fragments: things someone said, nearly said, typed, deleted, swallowed, misheard or received too late.

### A realistic search box

A familiar search box appears throughout the sequence. Its typed queries stay banal and recognisable, while the suggestions gradually become more private, ashamed, frantic or corrupted.

The search layer functions like thought leakage: the public interface of a private collapse.

### Figures and targeting

Silhouetted figures approach from depth. Later, they are watched, selected, targeted and removed. The effect should feel systemic rather than game-like: a field of attention, selection and disappearance.

### Generative audio

The audio engine is built with the Web Audio API. It uses embedded sources and generated synthesis/noise layers to create:

* low atmospheric beds
* radio-like interference
* rhythmic stress pulses
* impact sounds
* search-box tension
* title crashes
* final rupture

Sound levels evolve continuously across the timeline.

## Technical notes

**Stack:** plain HTML, CSS and JavaScript.
**Rendering:** Canvas 2D for scenery, atmosphere, figures, sun, stars and rupture effects; DOM for UI, phrases, search card and title events.
**Audio:** Web Audio API with embedded audio and generated layers.
**Typography:** embedded web fonts, including Archivo-style display typography and IBM Plex Mono-style interface text.
**Deployment:** static file only.

No frameworks or build tooling are used.

## Large screens, projection and casting

The piece is designed for large displays and gallery projection.

Recommended setup:

* fullscreen browser window
* sound enabled
* desktop/laptop playback when possible
* avoid browser zoom changes
* test once on the actual projector or display before showing

For casting, it is usually better to cast the browser tab from a desktop/laptop, letting the source machine do the rendering, rather than relying on a low-power streaming stick.

The interface is designed to keep the timer, mute control and phrase field away from unsafe overscan edges.

## Browser support

Designed for current versions of:

* Chrome
* Edge
* Safari
* Firefox

A modern browser from 2020 onward is recommended.

The piece relies on standard browser features:

* Canvas 2D
* Web Audio API
* CSS animations
* CSS `clamp()`
* pointer events

## Project structure

```text
no_worries.html   # the entire installation
README.md         # this file
```

One file is the whole work.

## Verifying a build

Before showing or publishing an edited version, check that:

* the HTML opens locally
* the **GO** hold interaction starts the piece
* audio starts correctly
* the full sixty-second sequence plays
* the final screen appears
* **GO** on the final screen restarts cleanly
* audio does not duplicate on replay
* the timer resets
* the sun appears throughout and ruptures near the end
* phrases do not clip or collide badly
* the search card appears and clears correctly
* JavaScript passes a syntax check
* the piece reads well in 16:9, ultrawide and large-display formats

## Credits and license

Concept and direction by the author.

Built as a self-contained web installation.

Embedded open-source typefaces remain subject to their original licenses, including the SIL Open Font License where applicable.

Add the chosen license for the work itself here, or include a separate `LICENSE` file.
