# DX7 Chillboot 🎛️

*A little synth boot dream.*

DX7 Chillboot is a small, browser-based audiovisual experiment inspired by the look and feel of the Yamaha DX7. It combines an animated, retro-style patch-loader graphic with a looping audio track and a subtle glow that reacts to the sound.

**[▶ Launch Chillboot on GitHub Pages](https://hoffamania.github.io/dx7-chillboot/)**  
[View the source on GitHub](https://github.com/Hoffamania/dx7-chillboot)

## Features

- Animated DX7-inspired patch-loader artwork built with SVG.
- Looping audio with a **Toggle DX7 Sound** button.
- Audio-reactive pink glow driven by the Web Audio API's frequency analyser.
- Responsive, minimal interface with a retro terminal/synth aesthetic.
- Static site: HTML, CSS, JavaScript, SVG, and MP3 files, with no build step or backend.

## Try it locally

Clone the repository and serve the folder with a small local web server:

```bash
git clone https://github.com/Hoffamania/dx7-chillboot.git
cd dx7-chillboot
python3 -m http.server 8000
```

Then visit **http://localhost:8000** and click **Toggle DX7 Sound** to start or pause the audio. Playback starts on a button click to work with browser autoplay restrictions.

## How it works

The page embeds an animated SVG and plays an MP3 loop through an HTML audio element. JavaScript connects that audio to a Web Audio `AnalyserNode`, reads frequency data on each animation frame, and changes the SVG's pink `drop-shadow` intensity in response.

This is a visual/audio tribute—not a DX7 emulator, MIDI instrument, or functional patch loader.

## Project files

| File | Purpose |
| --- | --- |
| `index.html` | Page layout, audio control, and reactive glow logic |
| `dx7_patch_loader_looped_final.svg` | Animated patch-loader artwork used by the page |
| `dx7_patch_loader.svg` | Additional SVG artwork |
| `loop1_clean_loopable_slowed_30_percent.mp3` | Audio loop used by the page |
| `loop1_clean_loopable.mp3` | Additional audio loop |

## About

A small creative coding project combining an interest in vintage synthesizers, audio, and browser-based visuals.

Made by [@Hoffamania](https://github.com/Hoffamania).
