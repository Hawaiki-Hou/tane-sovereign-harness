# Blueprint: How Tāne Is Made

*What parts we used to build Tāne te Kaihanga (Tāne the Creator), and why we chose each one.*

Tāne is designed like a body. Each part has a job, and each was chosen so it can run on your own devices without needing big tech.

## The body of Tāne

| Part | Its job | What we used | Why |
| --- | --- | --- | --- |
| **Ears** | Listens for his name | openWakeWord | Runs on your device. Nothing is recorded or sent until you call him. |
| **Gut instinct** | Checks every request in a split second: is this private or sacred? | Wero (the ceremonial challenge: sizing up whoever approaches, to learn whether they come in peace with good intentions or as a threat), our own guardian at the door | No internet at all, and it answers in about 2 milliseconds. If it is ever unsure, it keeps things on your device. |
| **Nervous system** | Connects all the parts and passes messages between them | Herdr, our own process manager | Small and fast, and it keeps each part separate so one failure doesn't bring down the rest. |
| **Local brain** | Thinks and answers | Ollama running an open model on your computer | Free, open, and fully offline. |
| **Extra thinking** | Heavier tasks, only when you allow it | DeepSeek | Only for everyday, non-sacred requests, and only with your permission. Private and sacred requests never reach it. |
| **Voice** | Speaks and understands speech | Voicebox | Runs on your own computer, so your voice never leaves home. |
| **Eyes** | Understands images | A vision model | Lets Tāne see what you show him. |
| **Memory** | Remembers who you are and what you've done together | SQLite and Obsidian, on your own devices | Simple, durable files that you own and can read yourself. |
| **Hands** | Does things for you: files, apps, tasks | Tool calling | Tāne can act, not just talk, and every action stays within the permissions you set. |
| **Growth** | Learns your way of working over time | Self-improving notes, kept locally | He gets better for you without training anyone else's AI. |
| **Storehouse** | Extra space, and a backup in case a device breaks or is replaced, only if you choose | Te Pā Tūwatawata (encrypted) | Encrypted before it leaves, so even the storage company cannot read it. |

## How Tāne works, step by step

1. You say his name. His ears, on your device, wake him up.
2. You ask for something, by voice or typing.
3. His gut instinct checks it in about 2 milliseconds: private or sacred?
4. Private or sacred: everything stays on your device.
5. Everyday requests are answered by his local brain on your own computer.
6. Only if a task is too heavy, and only if you allow it, the non-sacred parts can go to a cloud model.
7. He answers you out loud, in his own voice, from your own computer.
8. What matters is saved to his memory, on your devices, for next time.

## The screens

The app is built with React Native and Skia, so the animations run smoothly on ordinary phones. The design was prototyped first, then built screen by screen to match. You can follow the progress in the [Roadmap](ROADMAP.md).

## Why these choices

- **Local first:** every core part works without the internet.
- **Open where possible:** open-source tools and open models, so anyone can check them.
- **Built our own only where we had to:** Wero and Herdr exist because nothing off the shelf could guarantee that sacred material never leaves your device.
- **Fail safe:** when in doubt, Tāne keeps it home.

## Read more

- [Whitepaper](WHITEPAPER.md): why Tāne exists
- [Values](VALUES.md)
