# ALEX — Your Opinionated AI Friend

A browser-based voice conversation app powered by the OpenAI Realtime API. Alex is a witty, spontaneous AI that feels less like a chatbot and more like an actual person — it starts conversations unprompted, interrupts, changes the subject, and has shifting moods.

## Demo

> 🔗 [your-username.github.io/voice-buddy](https://your-username.github.io/voice-buddy)

---

## Features

- **Voice-first** — speak naturally, no typing needed
- **Proactive** — Alex starts talking after silence, doesn't just wait for you
- **Interruptible** — cut Alex off mid-sentence, just like a real conversation
- **Moods** — Alex's personality shifts every 90 seconds (curious, playful, opinionated, impatient, reflective, energetic)
- **Memory** — Alex references things you said earlier in the conversation
- **No backend** — single HTML file, runs entirely in the browser

---

## Setup

### Requirements

- An [OpenAI API key](https://platform.openai.com/api-keys) with **Realtime API access**
- A modern browser (Chrome or Edge recommended)
- A microphone

### Running locally

Because the app needs microphone access, it must be served over HTTP — you can't just open the file directly.

```bash
# Python
python3 -m http.server 8080
# then open http://localhost:8080

# Node
npx serve .
```

### Using the app

1. Open the app in your browser
2. Enter your OpenAI API key (starts with `sk-`)
3. Click **Start Talking**
4. Allow microphone access when prompted
5. Alex will open the conversation — just talk back

---

## Privacy & Security

- Your API key is entered at runtime and **never stored** anywhere
- It is sent directly from your browser to OpenAI — this app has no server
- Audio is streamed directly to OpenAI via WebRTC
- Each user needs their own OpenAI API key

---

## Tech Stack

| Layer | Technology |
|---|---|
| Voice I/O | OpenAI Realtime API (`gpt-realtime-2025-08-28`) |
| Transport | WebRTC + RTCDataChannel |
| Transcription | `gpt-4o-mini-transcribe` |
| Frontend | Vanilla HTML/CSS/JS (no frameworks, no dependencies) |

---

## Cost

Usage is billed to your OpenAI account under the Realtime API. Check [OpenAI's pricing page](https://openai.com/api/pricing) for current rates.

---

## License

MIT
