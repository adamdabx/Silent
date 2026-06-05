# 🔊 Silent — Noise Monitor

A simple, privacy-friendly noise level monitor that runs entirely in your browser — no server, no account, no data collection.

**[▶ Open live app](https://adamdabx.github.io/Silent/)**

---

## What it does

Silent uses your device's microphone to measure ambient noise in real time and gives you instant visual feedback:

| Status | Colour | Indicator |
|--------|--------|-----------|
| Quiet — acceptable level | 🟢 Green | OK |
| Slightly too loud | 🟠 Orange | Warning |
| Too loud | 🔴 Red | Flashing alert banner |

Thresholds are fully adjustable with two sliders, or choose from a set of predefined profiles tuned to common environments.

---

## Features

- **Real-time microphone monitoring** — volume bar + dB readout updated ~60×/s
- **Visual traffic-light indicator** — green / orange / red lamp with glow effect
- **Flashing alert** — unmissable when noise exceeds the loud threshold
- **6 preset profiles** — Night at home, Library, Home, Office, Warehouse, Construction site
- **Custom thresholds** — fine-tune with two sliders
- **Day / Night theme** — toggle between dark and light mode
- **3 languages** — English (default), Norwegian, Polish
- **Works offline** — pure HTML/CSS/JS, zero dependencies
- **Mobile-friendly** — designed for phones and tablets

---

## Privacy

> **No data ever leaves your device.**

Silent processes all audio **locally in your browser**. The microphone stream is used only to compute a real-time volume level — it is never stored, recorded, or transmitted anywhere. No analytics, no tracking, no cookies.

---

## How to use

1. Open the [live app](https://adamdabx.github.io/Silent/) in any modern browser (Chrome, Safari, Firefox)
2. Select a **profile** that matches your environment
3. Tap **Start microphone** and allow microphone access when prompted
4. Watch the lamp — green is good, orange means slow down, red means stop!

---

## Preset noise profiles

| Profile | Ok → Warning | Warning → Loud | Typical use |
|---------|-------------|----------------|-------------|
| 🌙 Night at home | very low | very low | Sleeping hours, babies |
| 📚 Library | low | low | Study rooms, quiet zones |
| 🏠 Home | moderate | moderate | General home use |
| 💼 Office | moderate | moderate-high | Open-plan offices |
| 📦 Warehouse | high | high | Storage, logistics |
| 🚧 Construction site | very high | very high | Loud work environments |
| ⚙️ Custom | — | — | Set manually with sliders |

---

## Self-hosting

The entire app is a **single `index.html` file** with zero external dependencies — just open it.

```bash
# Open directly in browser
open index.html

# Or serve locally (microphone requires HTTPS or localhost)
npx serve .
# or
python3 -m http.server 8080
```

> **Note:** Microphone access requires HTTPS or `localhost`. [GitHub Pages](https://pages.github.com/) provides HTTPS automatically.

**Deploy to GitHub Pages:**
1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Source: `Deploy from a branch` → `main` → `/ (root)` → Save
4. Your app will be live at `https://<your-username>.github.io/Silent/`

---

## Tech stack

| Layer | Technology |
|-------|------------|
| UI | Vanilla HTML + CSS |
| Logic | Vanilla JavaScript |
| Audio | [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) (`getUserMedia` + `AnalyserNode`) |
| Hosting | [GitHub Pages](https://pages.github.com/) |

No frameworks. No build step. No dependencies. One file.

---

## Browser support

| Browser | Support |
|---------|---------|
| Chrome / Edge 66+ | ✅ Full |
| Firefox 76+ | ✅ Full |
| Safari 14.1+ | ✅ Full |
| Samsung Internet | ✅ Full |

---

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-improvement`)
3. Commit your changes
4. Open a Pull Request

---

## License

[MIT](LICENSE) — free to use, modify, and distribute.
