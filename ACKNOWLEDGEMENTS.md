# Acknowledgements

Thank you to the people who build open source.

Most of the software below was written by people who will never meet the people it now helps, and who were paid nothing for it. Some of them worked evenings for years. Some of them are one person answering their own email. Tāne exists because they shared their work instead of keeping it.

This page names every open-source project the harness really uses, what it does in Tāne, and the licence it comes under. If a project is missing from this list, that is a mistake on our part and we would like to hear about it.

Two things are said plainly. **Hermes 3** is an open model under a community licence, not an OSI licence. **Obsidian** and the AI models that helped build the app are free or paid services, not open source. They are named here anyway, because they are part of the truth of how this was made.

---

## The platform underneath everything

| Project | What it does in Tāne | Licence |
|---|---|---|
| [Node.js](https://nodejs.org) | Runs the Home Node: the orchestrator, the job pipeline, the relay and the local HTTP/WebSocket server. | MIT |
| [Python](https://www.python.org) | Runs Voicebox, Tāne's speech server. | PSF-2.0 |
| [SQLite](https://sqlite.org) | The Home Node's durable memory: conversations, tasks and notes, all on your own machine. Tāne uses Node's own `node:sqlite`, so there is nothing to install. | Public domain |
| [ffmpeg](https://ffmpeg.org) | Audio conversion on the Home Node, so Tāne's voice arrives in the format the phone can play. | LGPL-2.1-or-later |

## The phone app

| Project | What it does in Tāne | Licence |
|---|---|---|
| [React Native](https://reactnative.dev) | The app itself, drawn once and running on the phone. | MIT |
| [React](https://react.dev) | The way every screen is described and updated. | MIT |
| [Expo](https://expo.dev) | Builds and ships the app. | MIT |
| [expo-secure-store](https://docs.expo.dev/versions/latest/sdk/securestore/) | Keeps the phone's keys in the phone's own keystore, never in a plain file. | MIT |
| [expo-crypto](https://docs.expo.dev/versions/latest/sdk/crypto/) | Random numbers and hashing, from the platform's own crypto. | MIT |
| [expo-file-system](https://docs.expo.dev/versions/latest/sdk/filesystem/) | Files on this phone, and nothing outside it. | MIT |
| [expo-audio](https://docs.expo.dev/versions/latest/sdk/audio/) | Plays Tāne's voice and records yours. | MIT |
| [expo-haptics](https://docs.expo.dev/versions/latest/sdk/haptics/) | The small physical tick when a drop is pressed. | MIT |
| [expo-font](https://docs.expo.dev/versions/latest/sdk/font/) | Loads the fonts the design depends on. | MIT |
| [expo-asset](https://docs.expo.dev/versions/latest/sdk/asset/) | Bundles Tāne's carved face, the kete and the other art. | MIT |
| [expo-document-picker](https://docs.expo.dev/versions/latest/sdk/document-picker/) | Lets you choose a file from your own phone. | MIT |
| [expo-screen-orientation](https://docs.expo.dev/versions/latest/sdk/screen-orientation/) | Holds the phone upright, the way the design is drawn. | MIT |
| [expo-splash-screen](https://docs.expo.dev/versions/latest/sdk/splash-screen/) | The first moment of the app, before Tāne appears. | MIT |
| [expo-build-properties](https://docs.expo.dev/versions/latest/sdk/build-properties/) | Build settings that let the app run fully offline on Android. | MIT |
| [@shopify/react-native-skia](https://shopify.github.io/react-native-skia/) | The living water, Tāne's face, the gold halo, the garden and Hawaiki Hōu sky. | MIT |
| [react-native-reanimated](https://docs.swmansion.com/react-native-reanimated/) | Movement on the UI thread, so nothing stutters while Tāne works. | MIT |
| [react-native-worklets](https://docs.swmansion.com/react-native-reanimated/) and [react-native-worklets-core](https://github.com/margelo/react-native-worklets-core) | The small pieces of work that run off the main thread for the animations. | MIT |
| [react-native-gesture-handler](https://docs.swmansion.com/react-native-gesture-handler/) | Every drag, hold, swipe and long press, including "Hold to send". | MIT |
| [react-native-svg](https://github.com/software-mansion/react-native-svg) | The marks on the drops, drawn as vectors so they stay sharp. | MIT |
| [react-native-safe-area-context](https://github.com/AppAndFlow/react-native-safe-area-context) | Keeps every control inside the screen's safe area. | MIT |
| [react-native-audio-api](https://docs.swmansion.com/react-native-audio-api/) | The low-level audio graph: microphone in, voice out. | MIT |
| [react-native-webrtc](https://github.com/react-native-webrtc/react-native-webrtc) | The live link between the phone and your Home Node. | MIT |
| [react-native-filament](https://github.com/margelo/react-native-filament) | The 3D stages Tāne is rendered in. | MIT |
| [react-native-nitro-modules](https://nitro.margelo.com) | The native module layer the other native packages ride on. | MIT |
| [react-native-openwakeword](https://github.com/crossplatform-dev/react-native-openwakeword) | Listening for his wake word on the phone, locally. | Apache-2.0 |
| [react-native-webview](https://github.com/react-native-webview/react-native-webview) | The small browser inside the app that ARCeye's augmented-reality view runs in — over files on your own phone, never the internet. | MIT |
| [@expo/vector-icons](https://docs.expo.dev/guides/icons/) | A few small interface marks. | MIT |
| [toqr](https://github.com/kareemf/toqr) | Draws the real QR code a student shows their supervisor. | MIT |

## The typefaces

Both faces ship inside the app. Hanken Grotesk is also embedded in the PDF the app binds, so a thesis in
te reo Māori keeps every macron when it is printed or sent. The licence text sits beside each font in
`mobile/assets/fonts/`.

| Typeface | What it does in Tāne | Licence |
|---|---|---|
| [Hanken Grotesk](https://github.com/marcologous/hanken-grotesk) | Every word you read and every word in your bound PDF. | [SIL OFL 1.1](https://openfontlicense.org) — the OFL allows a font to be "bundled, embedded, redistributed and/or sold with any software", and the face is embedded unchanged (no subset, no renamed derivative) with its notice and licence kept beside it. |
| [Rajdhani](https://github.com/itfoundry/rajdhani) | The small tracked labels above every page's words. | [SIL OFL 1.1](https://openfontlicense.org) — bundled unchanged with its notice and licence. |

## Keys and encryption

| Project | What it does in Tāne | Licence |
|---|---|---|
| [@noble/ciphers](https://github.com/paulmillr/noble-ciphers) | Locks your words before they are stored or sent home. | MIT |
| [@noble/curves](https://github.com/paulmillr/noble-curves) | The key agreement that pairs your phone and your Home Node. | MIT |
| [@noble/hashes](https://github.com/paulmillr/noble-hashes) | The fingerprints that prove nothing was changed on the way. | MIT |

## The Home Node and its memory

| Project | What it does in Tāne | Licence |
|---|---|---|
| [ws](https://github.com/websockets/ws) | The WebSocket the phone and the Home Node talk over. | MIT |
| [sqlite-vec](https://github.com/asg017/sqlite-vec) | Searches Tāne's notes by meaning, on your own disk. | MIT or Apache-2.0 |
| [@deepseek-ai/dsh](https://www.npmjs.com/package/@deepseek-ai/dsh) | The agent harness that runs Tāne's work on the Home Node. | MIT |

## Tāne's voice

| Project | What it does in Tāne | Licence |
|---|---|---|
| [Voicebox](https://github.com/agjs/voicebox) | Tāne's own speech server: one local HTTP API for hearing and speaking. | MIT |
| [faster-whisper](https://github.com/SYSTRAN/faster-whisper) | Speech to text, fast, on your own machine. | MIT |
| [distil-whisper](https://github.com/huggingface/distil-whisper) | The small English model Voicebox runs for that speech to text. | MIT |
| [Whisper](https://github.com/openai/whisper) | The speech-recognition model all of the above build on. | MIT |
| [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) | The voice that speaks Tāne's words. | Apache-2.0 |
| [kokoro-onnx](https://github.com/thewh1teagle/kokoro-onnx) | Runs Kokoro on the machine, offline. | MIT |
| [Piper](https://github.com/rhasspy/piper) | A second text-to-speech engine, for voices Kokoro does not have. | MIT |
| [ONNX Runtime](https://onnxruntime.ai) | The engine both voice models run in. | MIT |
| [numpy](https://numpy.org) | The number work under the audio. | BSD-3-Clause |
| [soundfile](https://github.com/bastibe/python-soundfile) | Reading and writing the audio files. | BSD-3-Clause |
| [PyAV](https://github.com/PyAV-Org/PyAV) | Unpacks the audio the phone sends. | BSD-3-Clause |
| [FastAPI](https://fastapi.tiangolo.com) | The small local HTTP server Voicebox answers on. | MIT |
| [uvicorn](https://www.uvicorn.org) | Runs that server. | BSD-3-Clause |
| [httpx](https://www.python-httpx.org) | Calls the voice models. | BSD-3-Clause |
| [huggingface-hub](https://github.com/huggingface/huggingface_hub) | Fetches the model files, once, to the Home Node. | Apache-2.0 |
| [python-multipart](https://github.com/Kludex/python-multipart) | Parses the audio upload. | Apache-2.0 |

## Tāne's local brain

| Project | What it does in Tāne | Licence |
|---|---|---|
| [Ollama](https://github.com/ollama/ollama) | Runs Tāne's local model on your own computer, with no cloud. | MIT |
| [Hermes 3](https://huggingface.co/NousResearch/Hermes-3-Llama-3.1-8B) | The model itself: Tāne's thinking when he stays home. | Llama 3.1 Community Licence (Nous Research) — an open model under a community licence, not an OSI one |

## ARCeye — the eye that sees your prints

ARCeye is the screen where Tāne looks through the phone's camera. Point it at one of Thomas's ARC prints and
the story attached to that print plays over the live view. Its augmented-reality view is Thomas's own page,
and the two libraries that make it work are open source and bundled INSIDE the app, so the screen needs no
internet at all.

| Project | What it does in Tāne | Licence |
|---|---|---|
| [A-Frame 1.3.0](https://aframe.io) | The 3D scene the AR view is composed in: the film is placed over the live camera and drawn in one canvas, so a recording of the screen holds both. | MIT |
| [MindAR 1.2.2](https://github.com/hiukim/mind-ar-js) (mindar-image-aframe) | Image tracking on the phone: it recognises an ARC print in the camera picture and tells the page which film to play. Nothing about the print, the film or the picture is sent anywhere. | MIT |
| [three.js](https://threejs.org) | The 3D engine A-Frame itself is built on. | MIT |

## Notes, plainly read

| Project | What it does in Tāne | Licence |
|---|---|---|
| [Obsidian](https://obsidian.md) | The plain-markdown notes Tāne reads by path on the Home Node — the reason his memory is a folder you can open, change or delete yourself. | Free to use, but **not open source** |

## The AI that helped build it

These are services, not open-source projects, and they are named so the record is honest.

| Tool | What it did | Terms |
|---|---|---|
| [DeepSeek](https://www.deepseek.com) | Built the app and the backend alongside me, and is Tāne's optional cloud thinker (off by default, never used for anything tapu). | Commercial service |
| [Claude](https://www.anthropic.com) (Anthropic) | The design, the prototype and every design review. | Commercial service |
| [Gemini](https://gemini.google.com) (Google) | Research and early development. | Commercial service |

## Yours to hold us to

Every design decision, the cultural direction and the purpose behind Tāne are mine, Dr Thomas Clark. The code is open so you can check our work, improve it, and hold us to our promises.

If you build something here, or fix something here, thank you. You are part of this now.

[← Back to the front page](README.md)
