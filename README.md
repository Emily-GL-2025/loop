<div align="center">

# Vocabulary Loop Studio

**A lightweight browser-based tool for detecting, repeating, and exporting spoken vocabulary from audio recordings.**

[![Website](https://img.shields.io/website?url=https%3A%2F%2Femily-gl-2025.github.io%2Floop%2F&label=Live%20Site)](https://emily-gl-2025.github.io/loop/)
[![GitHub License](https://img.shields.io/github/license/Emily-GL-2025/loop)](LICENSE)


</div>

## Overview

Vocabulary Loop Studio turns vocabulary-list recordings into repeatable word-by-word practice audio.

Load an MP3 or MP4 file, detect spoken words from the silence between them, choose how many times each word should repeat, and play or export the resulting sequence.

Everything runs locally in the browser. Audio files are not uploaded to a server.

## Features

- MP3 and MP4 audio input
- Automatic word segmentation using silence detection
- Manual or automatic intro bypass
- Adjustable silence threshold and minimum silence duration
- Configurable pre/post speech padding
- Repeat count and gap controls
- Waveform overview and individual word preview
- Play, pause, stop, and volume controls
- MP3 export with WAV fallback
- Light and dark themes
- No installation or backend required

## Usage

1. Open the [live web app](https://emily-gl-2025.github.io/loop/), or open `index.html` locally.
2. Load an MP3 or MP4 vocabulary recording.
3. Set the end of any spoken introduction manually or with **Auto-find**.
4. Adjust the detection settings if needed.
5. Select **Analyze words**.
6. Set the repeat count and gap between repetitions.
7. Play the sequence or export the repeated audio.

## How It Works

The app decodes audio in the browser and calculates an energy measurement every **10 ms**.

Periods below the selected silence threshold are used to separate spoken words. Each detected segment can be padded slightly before playback or export.


## Run Locally

```bash
git clone https://github.com/Emily-GL-2025/loop.git
cd loop
```

Then open `index.html` in a modern browser.

No package installation or build step is required.

## Technology

- HTML5
- CSS
- Vanilla JavaScript
- Web Audio API
- Canvas
- lamejs for browser-side MP3 encoding

## Privacy

Audio processing is performed locally in the browser. Selected audio files are not uploaded by the application.

## License

Licensed under the [Apache License 2.0](LICENSE).
