<div align="center">

# Twin Studio

### The desktop AI agent for Mac. Built in India. Free, forever — no subscription.

[![Release](https://img.shields.io/badge/Release-v2.6.0-2DD4BF)](https://github.com/oneneuralent/twin-desktop-releases/releases/tag/v2.6.0)
[![Platform](https://img.shields.io/badge/Platform-macOS%2012%2B-blue)](https://github.com/oneneuralent/twin-desktop-releases/releases)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)
[![Website](https://img.shields.io/badge/Web-thesocialtwin.com-purple)](https://thesocialtwin.com)

**[Download v2.6.0](https://github.com/oneneuralent/twin-desktop-releases/releases/tag/v2.6.0)** · `curl -fsSL https://thesocialtwin.com/install | bash`

Apple Silicon (`Twin-2.6.0-arm64.dmg`) · Intel Mac (`Twin-2.6.0.dmg`)

</div>

---

## The story

Most AI agents are built by engineers who are great at technology but have never made anything with their hands. Twin Studio is not that.

Twin Studio was built by **Rayhaan Patni** — a music video director who spent years on sets with some of India's biggest artists: **Ankit Tiwari, Emiway Bantai, Talwiinder, Shreya Ghoshal**. He directed videos. He lit sets. He sat in edit bays at 3 AM. He knows what it costs to turn an idea into something watchable — in money, in time, in the part of your soul you give up to get the shot.

Then he spent **a year and a half** building this.

Not a ChatGPT wrapper. Not a demo. A real, signed, installable, auto-updating Mac application that lives on your desktop and does the work of a crew — because the person who built it was the crew.

**This is India's first Creative Tech.** Not an LLM company. Not a wrapper. A desktop AI agent with an agentic-agnostic model — it doesn't care which LLM you use, it cares about the output. It routes the right model to the right task, the way a director routes the right person to the right job.

Other agents are built by engineers. This one has soul. Soul comes from purpose and art, and purpose comes from having done the work yourself.

---

## What it is

Twin Studio is a desktop-resident AI agent for macOS. It lives on your Mac. It controls your Mac. It browses the web. It generates images and video. It writes screenplays. It builds presentations. It runs terminal commands. It reads your screen. It posts to Instagram. It manages your calendar, your mail, your files, your reminders.

You don't switch between 5 apps. You create your Twin — and your Twin does the rest.

**Free. No subscription. No monthly bill.** Bring your own LLM provider (OpenRouter, OpenAI Direct, Requesty, OpenCode Zen, or any custom OpenAI-compatible endpoint). Agent thinking is always free — you only pay for image/video generation, and only when you choose to generate.

---

## Install

### Option 1 — One command (recommended)

```bash
curl -fsSL https://thesocialtwin.com/install | bash
```

This detects your Mac's architecture (Apple Silicon or Intel), downloads the latest release via curl (which bypasses macOS Gatekeeper quarantine), mounts the DMG, copies Twin to `/Applications`, strips Gatekeeper attributes, and launches it. No manual steps. No "Twin is damaged" error.

The installer fetches the latest release automatically — you always get the newest version.

### Option 2 — Manual download

1. Go to [releases](https://github.com/oneneuralent/twin-desktop-releases/releases/tag/v2.6.0)
2. Download the right DMG for your Mac:
   - **Apple Silicon** (M1/M2/M3/M4): `Twin-2.6.0-arm64.dmg`
   - **Intel Mac**: `Twin-2.6.0.dmg`
3. Open the DMG, drag Twin to Applications
4. Launch Twin

### If macOS says "Twin is damaged" or "can't be opened"

This only happens with the manual download (Option 2). The curl installer (Option 1) bypasses this entirely.

If you hit it, open Terminal and run:

```bash
xattr -cr /Applications/Twin.app
```

Then launch Twin normally. You only need to do this once.

### Add your LLM provider key

1. Open Twin
2. Go to Settings → Provider Keys
3. Paste your OpenRouter / OpenAI / Requesty / custom provider key
4. Keys are stored in macOS Keychain — never in plaintext

That's it. Agent thinking is free. You only pay for image/video generation when you choose to generate.

---

## Every feature — the full macro

### Native Mac control (Computer Use)

Twin controls your Mac the smart way — via **AppleScript and native accessibility APIs**, not screenshots and vision models. This is ~1000x faster than the vision-based approach used by Claude Computer Use and OpenAI Operator.

| What | How |
|---|---|
| Click any element | Native UI tree lookup — no screenshot needed |
| Click coordinates | Pixel-precise |
| Type text into any app | Injects into the frontmost app |
| Read the UI tree | Structured accessibility tree, not a screenshot |
| Get selected text | Reads what you've highlighted |
| Replace selected text | Inline edit in any app |
| Press keys / scroll | Full keyboard control |
| Screenshot (window/region/full) | When vision is actually needed |
| Detect frontmost app | Knows what you're looking at |
| Get native context | Extracts URL, email body, file paths, selected text from the frontmost app via AppleScript. No vision model needed. |

**Why this beats Claude Computer Use and OpenAI Operator:** They take a screenshot, send it to a vision model, wait for the model to identify a button, then click. Twin reads the accessibility tree directly — it knows the button exists without looking. Faster, cheaper, more reliable.

### Built-in browser

A full Chromium browser panel lives inside Twin. Not a separate window — embedded in the agent.

- Navigate, open, close, switch tabs
- Click, type, submit, scroll
- Read page text, elements, state
- Screenshot any page
- Fill and detect logins
- Save / load credentials
- Browser memory — Twin remembers sites
- Upload files to web forms
- Top sites, history

### Terminal

Run shell commands directly from the agent. Full terminal panel with output streaming.

### File operations

Read, write, edit, move, open, reveal files. List directories. Upload local files. Read files as base64.

### Productivity

| What | How |
|---|---|
| Calendar | Create and read events |
| Reminders | Native macOS Reminders |
| Todos | Full todo system — add, list, complete, update, delete, sync |
| Scheduler | launchd-based scheduled tasks |
| Mail | Send and read email |
| Clean desktop | Organize your Desktop |
| Organize downloads | Tidy your Downloads folder |
| Open apps | Open, list, close any app |
| Clipboard | Read and write clipboard |
| System info | Full system info |

### Creative — image & video generation

This is the core. The agentic creative harness for filmmaking.

| What | How |
|---|---|
| Image generation | Routes across 40+ models — Nano Banana, Flux, Kling, Google Gemini, Cloudflare Workers AI |
| Video generation | Kling V3 Omni, Seedance 2, WAN 2.6, and more — routed per shot |
| Filmmaking pipeline | Screenplay → Storyboard → Character Refs → Shot Breakdown → Hero Frames → Video Clips → Audio → Export |
| Screenplay export | Industry-standard screenplay format |
| Instagram posting | Publish directly to Instagram |
| Avatar generation | PhotoMaker-based avatar creation |
| Video editor | Built-in timeline editor — trim, cut, export MP4 |

### Presentations (PPT)

AI-powered slide decks. 10 palette presets, 5 slide layouts, topic-matched color schemes. Generate a full `.pptx` from a prompt.

### Voice

Speech recognition (talk to your Twin) and text-to-speech (your Twin talks back, native macOS TTS).

### Security & keys

API keys stored in the **macOS Keychain** — never in plaintext, never in the cloud. Native OpenAI OAuth flow supported.

### Projects

Full project management — list, create, load, save, rename, delete. Project files, references, and automatic state sync.

### Desktop pet — the Twin Orb

A floating companion that lives on your desktop. Move it, resize it, click it to send commands. It shows live badge counts for scheduler, todos, scratch notes, and mail. Global shortcut: `Cmd+Shift+T` — summon Twin from anywhere.

### Auto-updates

Silent, background updates via GitHub Releases. No manual download needed. The app checks for new versions and installs them on restart.

### Multi-platform publishing

Publish directly from Twin:
- **Instagram** — feed posts, reels
- **LinkedIn** — text and image posts
- **YouTube** — video uploads
- **Threads** — text posts
- **Facebook** — page posts

---

## Modes — each one is a specialist

Twin Studio has surfaces and modes. Each is built for a specific job. This is why Twin beats Claude and GPT for real work — they're generalists. Twin has specialists.

### Chill (Chat)

Lightweight chat with web search and DeepWiki integration. Ask anything, get answers with citations. Your everyday assistant — fast, no agent overhead.

**USP vs Claude/GPT:** Claude and GPT are trapped in a browser tab. Chill lives on your desktop with a global shortcut (`Cmd+Shift+T`). One keystroke, you're talking. No tab switching, no context loss.

### Twin (Work)

The agentic workbench. This is where Twin controls your Mac — browser, terminal, files, apps, calendar, mail. Full agent loop with tool calls, approvals, and streaming. Auto-approve mode for power users.

**USP vs Claude Computer Use:** Claude Computer Use takes screenshots and sends them to a vision model to figure out what's on screen. Twin reads the native accessibility tree via AppleScript — it knows what's on your screen without looking. ~1000x faster, ~1000x cheaper, and it doesn't hallucinate buttons that don't exist.

**USP vs OpenAI Operator:** Operator runs in a cloud browser. Twin runs on your Mac, with access to your files, your terminal, your Keychain, your native apps. It's not a remote session — it's your machine.

### Plan

Plan your video before you generate. Twin writes the screenplay, breaks it into shots, and routes the right AI model to each shot. You review the plan, tweak it, then generate.

**USP vs Claude/GPT:** Claude and GPT can write a screenplay. They can't route it to 40+ generation models, plan shot-by-shot, and execute the pipeline. Plan mode isn't a text generator — it's a pre-production department.

### Create (Cinema)

The filmmaking mode. This is the soul of Twin Studio. Brief it in one sentence — "a perfume film in monsoon Mumbai, intimate, strange, unforgettable" — and Twin turns it into a treatment, a screenplay, a shot list, and generated footage.

Built by a director who directed music videos for Ankit Tiwari, Emiway Bantai, Talwiinder, and Shreya Ghoshal. This mode knows what a shot is. It knows what a cut is. It knows what a treatment is. Claude and GPT know what a screenplay looks like. Twin knows what a film feels like.

**USP vs Claude/GPT:** They generate text about film. Twin generates film. Image generation, video generation, storyboard, screenplay export, timeline editing — all in one mode, all from one sentence.

### Generate

Quick generation mode. Describe what you want, get an image or video immediately. No agent loop, no planning — just fast output.

**USP vs Claude/GPT:** Claude and GPT can't generate video. They can't generate images natively. Twin routes across 40+ models and picks the right one for the job.

### PPT

AI-powered slide decks. 10 palette presets, 5 slide layouts, topic-matched color schemes. Generate a full `.pptx` from a prompt.

**USP vs Claude/GPT:** They can write slide content as text. Twin generates an actual `.pptx` file you can open in PowerPoint, with designed slides, color palettes, and layout variety.

### Messages

A B&W typewriter messenger — native to the agent dock. For when you want to draft messages, scripts, or notes in a focused, distraction-free surface.

### Rizz

A creative mode with image reference slots. Drop in a first frame and reference images, and Twin generates with visual context — it can see your references via vision. For creative work where you need to match a look, a style, or a face.

---

## Everything under one umbrella

Before Twin Studio, this is what your workflow looked like:

| Task | Tool |
|---|---|
| Write a screenplay | Notion / Google Docs |
| Plan shots | Spreadsheet / your head |
| Generate images | Midjourney / DALL-E / a separate app |
| Generate video | Runway / Kling / a separate website |
| Edit the video | Premiere / DaVinci / a separate app |
| Make a presentation | PowerPoint / Canva / a separate app |
| Post to Instagram | Instagram app / a scheduler |
| Research the web | Browser + ChatGPT tab |
| Manage your calendar | Calendar app |
| Send an email | Mail app |
| Run a script | Terminal |

After Twin Studio:

| Task | Tool |
|---|---|
| All of it | Twin Studio |

**All you gotta do is create your Twin.**

---

## Brain Models — Bring Your Own Key (BYOK)

Twin is **agentic-agnostic** — it doesn't lock you into one LLM provider. You bring the keys, Twin does the work. Agent thinking is always free.

Supported providers:
- **OpenRouter** — access every model with one key
- **OpenAI Direct** — native OAuth login, no key management
- **Requesty** — cost-optimized routing
- **OpenCode Zen** — open routing
- **Custom providers** — any OpenAI-compatible endpoint

### Flagship Models

| Model | Company | Context | Vision | Tools | Reasoning |
|---|---|---|---|---|---|
| **Gemini 2.5 Flash** | Google | 1M | Yes | Yes | Yes |
| **Gemini 3.1 Flash Lite** | Google | 1M | Yes | Yes | Yes |
| **GPT-5.5 (ChatGPT)** | OpenAI | 400K | Yes | Yes | Yes |
| **GPT-5.6 Luna** | OpenAI | 1M | Yes | Yes | Yes |
| **Claude Haiku 4.5** | Anthropic | 200K | Yes | Yes | Yes |
| **Kimi K3** | Moonshot AI | 1M | Yes | Yes | Yes |
| **MiniMax M3** | MiniMax | 1M | Yes | Yes | Yes |

### Free Models

| Model | Company | Context | Tools |
|---|---|---|---|
| **Laguna M.1** | Rizz | 256K | Yes |
| **Laguna XS 2.1** | Rizz | 256K | Yes |
| **Nemotron Ultra 550B** | NVIDIA | 1M | Yes |
| **Nemotron Super 120B** | NVIDIA | 262K | Yes |
| **Nemotron Nano 30B** | NVIDIA | 256K | Yes |
| **Llama 3.3 70B** | Meta | 128K | Yes |
| **Qwen3 Next 80B** | Qwen | 262K | Yes |
| **GPT-OSS 120B** | OpenAI | 128K | Yes |
| **GPT-OSS 20B** | OpenAI | 128K | Yes |
| **Cohere North Mini Code** | Cohere | 256K | Yes |
| **Gemma 4 31B** | Google | 262K | Yes |
| **Gemma 4 26B** | Google | 262K | Yes |

Keys are stored in the **macOS Keychain** — never in plaintext, never in the cloud.

---

## Generation Models

### Image

| Model | Best For |
|---|---|
| **Nano Banana 2** | Character consistency, 14 reference images |
| **Nano Banana 2 Lite** | Fast, budget-friendly hero frames |
| **Nano Banana Pro** | Maximum quality, magazine-cover stills |
| **Flux Fast** | Quick concept art, text-to-image |

### Video

| Model | Best For |
|---|---|
| **Kling V3** | Cinematic motion, character consistency |
| **Kling V3 Omni** | All-in-one generation |
| **Seedance 2** | Multi-reference, audio-ready, dialogue scenes |
| **WAN 2.6 I2V** | Budget image-to-video, simple motion |
| **WAN 2.5** | Fast generation |
| **Luma Modify Video** | Video-to-video modification |

### Audio

| Model | Best For |
|---|---|
| **Music Generator** | Original score, ambient tracks |
| **Kling Lipsync** | Dialogue lipsync from screenplay |

---

## System Requirements

| Requirement | Minimum |
|---|---|
| **OS** | macOS 12 (Monterey) or later |
| **RAM** | 8 GB (16 GB recommended for video generation) |
| **Storage** | 500 MB app + cache |
| **Internet** | Required for AI model calls |

---

## Privacy

- API keys (BYOK) are stored locally in macOS Keychain — never sent to our servers
- Browser panel cookies are imported locally from Chrome — never transmitted
- Project data (screenplays, shots, media) is stored in Supabase (PostgreSQL)
- We do not train on your data

---

## Built by

**Rayhaan Patni** — music video director turned creative technologist.

Directed videos for Ankit Tiwari, Emiway Bantai, Talwiinder, Shreya Ghoshal. Then spent a year and a half building India's first desktop AI agent — because the tools he needed didn't exist, and the ones that did were built by people who'd never been on a set.

**O.N.E Neural Entertainment** — Made in India.

---

## License

Copyright (c) 2026 One Neural Ent. All rights reserved. See [LICENSE](LICENSE) for details.

---

<div align="center">

**[Download Twin Studio v2.6.0](https://github.com/oneneuralent/twin-desktop-releases/releases/tag/v2.6.0)**

Free. No subscription. Bring your own LLM. Make your first film today.

</div>
