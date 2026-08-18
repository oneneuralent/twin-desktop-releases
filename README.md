<div align="center">

# Twin Desktop

### The AI agent that does all the work. You direct.

[![Release](https://img.shields.io/badge/Release-v1.16.0%20Beta-orange)](https://github.com/oneneuralent/twin-desktop-releases/releases)
[![Platform](https://img.shields.io/badge/Platform-macOS%2013%2B-blue)](https://github.com/oneneuralent/twin-desktop-releases/releases)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)
[![Website](https://img.shields.io/badge/Web-thesocialtwin.com-purple)](https://www.thesocialtwin.com)

</div>

---

## The Mission

> **Filmmaking democracy. Agentic democracy.**
>
> Every person with a story should be able to make cinema -- without a crew, without a budget, without a film school. The Twin is the agent that sits beside you, reads your screenplay, plans every shot, generates every frame, animates every clip, scores the audio, and assembles the final cut.
>
> You direct. The Twin does the work.
>
> This is not a tool you operate. It is an agent that operates for you -- across research, writing, browsing, coding, and creation.

---

## Install

### 1. Download

| Mac Type | Chip | Download |
|---|---|---|
| Apple Silicon | M1 / M2 / M3 / M4 | `Twin-1.16.0-arm64.dmg` |
| Intel | Intel Core | `Twin-1.16.0.dmg` |

### 2. Install

1. Open the downloaded `.dmg`
2. Drag Twin to your Applications folder
3. Launch -- macOS may say "unidentified developer"
4. Right-click -> Open -> Open Anyway (first launch only)
5. You are in.

### 3. Update

Twin auto-updates. When a new build drops, you will get a notification inside the app. Or just download the latest `.dmg` and replace.

---

## What the Twin Does

### Filmmaking Pipeline

The Twin runs the full pipeline -- from idea to final cut:

```
Screenplay -> Storyboard -> Character Refs -> Shot Breakdown -> Hero Frames -> Video Clips -> Audio -> Export
```

| Stage | What Happens |
|---|---|
| **Screenplay** | Twin writes or refines your screenplay -- the source of truth for everything |
| **Storyboard** | One image, entire screenplay -- vibe check before committing |
| **Character Refs** | Generate, approve, lock in the Project Bible -- consistency from shot 1 to 100 |
| **Shot Breakdown** | Every shot gets lens, lighting, cast, duration, prompt |
| **Hero Frames** | Magazine-quality stills -- approve before motion |
| **Video Clips** | Image-to-video with character consistency and motion control |
| **Audio** | Music, dialogue, ambient -- lipsync when the screenplay calls for it |
| **Export** | Assemble the final cut |

### Browser Panel

A native browser sidecar -- browse the web alongside your conversation.

- **Tabbed browsing** with thumbnail previews on the right edge
- **Minimize** (yellow) -- hides panel, keeps tab thumbnails. Hover right edge to reveal
- **Close** (red) -- closes all tabs
- **Auto sign-in** -- sign in to Google/YouTube in your system browser, Twin imports your session automatically
- **Per-tab close** -- X icon above each thumbnail

### Code Mode

The Twin reads, writes, and edits files on your machine -- like Claude Code or Cursor.

- Read any file, write new files, apply targeted string replacements
- Terminal access for running commands
- Tree-sitter powered code understanding (Go, JavaScript, Python, Rust, TypeScript)

### Multi-Platform Publishing

Publish directly from the Twin:

- **Instagram** -- feed posts, reels, stories
- **LinkedIn** -- text and image posts
- **YouTube** -- video uploads
- **Threads** -- text posts
- **Facebook** -- page posts

---

## Brain Models

The Twin supports **BYOK (Bring Your Own Key)** -- use your own API keys, or use our hosted credits. Switch models anytime.

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
| **OS** | macOS 13 (Ventura) or later |
| **RAM** | 8 GB (16 GB recommended for video generation) |
| **Storage** | 500 MB app + cache |
| **Internet** | Required for AI model calls |

---

## Privacy

- Your conversations are processed on our servers and sent to the AI model providers you select
- API keys (BYOK) are stored locally on your machine, never sent to our servers
- Browser panel cookies are imported locally from Chrome -- never transmitted
- Project data (screenplays, shots, media) is stored in Supabase (PostgreSQL)
- We do not train on your data

---

## License

Copyright (c) 2026 One Neural Ent. All rights reserved. See [LICENSE](LICENSE) for details.

---

## Links

- **Website**: [thesocialtwin.com](https://www.thesocialtwin.com)
- **Releases**: [Latest builds](https://github.com/oneneuralent/twin-desktop-releases/releases)
- **Support**: Through the in-app feedback channel

---

<div align="center">

**The Twin does all the work. You direct.**

</div>
