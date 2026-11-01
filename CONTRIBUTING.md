# Contributing to Tāne

Kia ora, and thank you for wanting to help.

## What we most need
1. **Reviews and tests** of reliability, safety, security and robustness (see the list below).
2. **Bug reports** with clear steps.
3. **Code fixes** for open issues, small and focused, with tests.

## What to check
- **Reliability:** the app on a real Android phone; offline use; the Home Node restarting; voice turns on a slow network.
- **Safety:** Tāne asks before he touches anyone's files (the seal); he never acts without a hold; private mode stays text-only and on the phone; tamariki mode keeps no voice recordings and has no strangers, ads or purchases.
- **Security:** nothing tapu leaves the device; signed invites and notes (`tane://join`, `tane://ended`, `tane://note`) refuse anything forged, expired or altered; secrets never reach the repo or the logs.
- **Robustness:** bad or huge input, a lost connection, a full disk, a malicious link, a crash in the middle of a save.

Use the **"Review finding"** issue form for what you find, and include how you tested it.

## How to work
- Fork, make a branch, keep each change small, and add a test.
- Run the tests before you open a pull request (`npm test` in `mobile/` and in the backend).
- **No new backend systems.** Tāne routes only through its existing services (Wero, Herdr, Voicebox) and local models (Ollama).
- **Local first.** Nothing may send personal or cultural data to a cloud service by default.
- Follow the design rules: the prototype is the specification, and screens must match it.

## Cultural content
Tāne's face (the mataora), Tāne te Kaihanga, the carvings, the te reo lexicon and the Hawaiki Hōu world designs are **not open source**. Please don't copy, change or add cultural content (images, carvings, moko, karakia, pūrākau, te reo phrasing) without permission. Ask first in an issue. Content from a particular iwi or hapū needs their consent and credit.

## Conduct
Be kind, be patient, and treat this kaupapa and the people in it with respect. See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
