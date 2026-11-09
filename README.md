# WAVR

**Layered granular synthesis, in your browser.** Load a sound and sculpt it into grains: freeze a single moment, stretch it, stack several readings of the same sound until you get a texture nobody has heard before.

**▶ Try WAVR: https://olivierelbhar.github.io/wavr/**

WAVR is part of a collection of playable audio tools (BREAKR, SCANR, TRACR, DRIFTR…): one production technique, one tool, one interface that teaches it while you play.

> Status: work-in-progress prototype. Everything lives in a single HTML file, with no dependencies and no server.

## Try it

Open the [live demo](https://olivierelbhar.github.io/wavr/), or open `index.html` in any recent browser (Chrome, Safari, Firefox), then hit **▶ Play**. An example sound (a breakbeat and a pad) is preloaded; load or drop your own audio file to make it yours. Nothing is uploaded: everything runs in the browser.

## The problem

Granular synthesis produces sounds no other technique can, but existing tools (plugins, hardware like the Torso S-4, apps like GrainHeads) are built for sound designers who already speak the language: playheads, spray, envelopes. For a curious musician, the door is closed.

## Product decisions

- **Families, not "playheads".** Multi-playhead granular exists elsewhere; WAVR frames it as named layers (Cloud, Freeze, Glitch, Rewind, Octaves, Random) you switch on and stack. Each layer remembers its own settings.
- **Every control explains itself in one sentence**, instead of a manual.
- **Zero install.** One link, one click, sound. That is what makes it shareable.
- **Scales designed for the ear, not the engine.** Scan speed is logarithmic, so most of the slider is devoted to extreme slow motion (down to 1/1000), where the interesting sounds live.

## Features

- 7 independent granular layers, each with its own playhead
- Per layer: size, density, spray, scan (freeze, slow motion, reverse), random sweep, pitch, detune, reverse, stereo width, envelope, jitter, volume
- Per layer effects chain: saturation → flanger → phaser → echo → reverb
- Settings saved in the browser

## Roadmap

- [ ] Record: WAV export, then short video clips for sharing
- [ ] Modulation (assignable LFOs on position and size)
- [ ] Keyboard play: one note = one transposed layer
- [ ] Plugin version (VST3/AU) for the most-used layers

## Under the hood

Plain HTML, CSS and JavaScript, no framework. Sound runs on the Web Audio API: each grain is a short slice of the file, played with its own envelope, pitch and stereo position.

---

Built by [Olivier Elbhar](https://olivierelbhar.com), product manager and music producer.
