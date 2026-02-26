[README.md](https://github.com/user-attachments/files/25571484/README.md)
<div align="center">

<img src="https://github.com/user-attachments/assets/3a505f99-9af4-4a7f-9852-7322e915fbab" alt="Animo Starter Kit" width="100%" />

# Animo Starter Kit

### Breathe a Soul into Your Character.

The production-ready **Tauri 2** boilerplate for building cross-platform AI desktop companions — with the hardest problems already solved.

[![License](https://img.shields.io/badge/license-Commercial-blue)](#license)
[![Tauri](https://img.shields.io/badge/Tauri-2.10-24C8D8?logo=tauri&logoColor=white)](https://tauri.app)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Rust](https://img.shields.io/badge/Rust-1.77+-DEA584?logo=rust&logoColor=white)](https://rust-lang.org)
[![Live2D](https://img.shields.io/badge/Live2D-Cubism_SDK-FF6699)](https://www.live2d.com)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Windows-lightgrey)](#)

<br />

[**Get on Lemon Squeezy →**](https://roistore.lemonsqueezy.com/checkout/buy/bbd0dbc2-02c9-4442-a810-5e4bc6235d62) | [**Get on Gumroad →**](https://dakju.gumroad.com/l/animo-starter-kit)

<br />

</div>

---

## The Problem

You've got the perfect character design. You've imagined the personality. Now you just need to build a transparent always-on-top desktop app that:

- Lets clicks **pass through** transparent pixels (but NOT the character)
- Works on **both macOS and Windows** from a single codebase
- Renders a **Live2D model** with real-time expression changes
- Connects to **any LLM** and streams dialogue with emotion detection
- Behaves **autonomously** — greeting you, reacting, living on your screen

**Each of these is a multi-week rabbit hole.**

Tauri's transparent window? Undocumented platform quirks. Pixel-perfect click-through? You need a Rust-level alpha mask pipeline with platform-specific cursor monitoring. Live2D + LLM emotion bridge? Custom SSE parser plus expression mapping.

You could spend **3–6 months** piecing it together from Stack Overflow fragments and GitHub issues.

**Or you could start building your product today.**

---

## Core Features

### 1. Cross-Platform Click-Through Transparency

> The #1 hardest problem in desktop pet development — **solved.**

A battle-tested Rust pipeline extracts the alpha mask from your Live2D canvas at **60fps**, monitors cursor position via native APIs (macOS: `Cocoa/NSEvent`, Windows: `Win32`), and dynamically toggles click-through **per pixel**.

Your character is interactive. Everything else is invisible. Works identically on macOS and Windows.

```
Frontend (150ms)                    Rust Backend (60fps)
┌─ generateAlphaMask()              ┌─ GetCursorPos (platform-native)
│  └─ Canvas → 5% downsample       ├─ Check UI regions (priority)
│     └─ Extract alpha channel      ├─ Check alpha mask (pixel-level)
└─ invoke("set_alpha_mask")         ├─ Drag lock (mouse button state)
                                    └─ set_ignore_cursor_events(!inside)
```

### 2. Live2D + LLM Emotion Bridge

> Your character doesn't just talk — it **feels.**

A streaming emotion parser detects `[joy]`, `[sad]`, `[playful]` and 6 other emotion tags (**9 total**) in real-time from any LLM response. These are instantly mapped to your Live2D model's expressions. One sentence from the AI, and your character's face changes mid-word.

### 3. Autonomous Behavior Engine

> Your character has a life of its own.

**8 built-in behavior types** — morning greetings, idle animations, return-to-screen welcomes, night mode awareness, random curiosity, and more. Each with configurable cooldowns and personality weights.

### 4. Eye Tracking

The character's eyes follow your cursor in real-time at 30fps. Powered by the same Rust cursor monitor — zero extra overhead.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Tauri 2.10 |
| Frontend | React 19 + TypeScript + Vite 7 |
| Rendering | PixiJS 6 + pixi-live2d-display |
| Backend | Rust (native platform APIs) |
| LLM | OpenAI-compatible API (7+ providers) |

**Under 1MB** clean codebase — no bloat, no mystery dependencies.

---

## Without Animo vs. With Animo

| Without Animo | With Animo |
|---------------|------------|
| 3–6 months building infrastructure | **Start customizing Day 1** |
| Hunt through Tauri GitHub issues for transparency hacks | **Battle-tested pipeline, already working** |
| Write platform-specific Rust for macOS AND Windows | **Single codebase, both platforms** |
| Build your own SSE parser + emotion engine | **Plug in any OpenAI-compatible API and go** |
| Debug WebGL alpha extraction edge cases | **5% resolution mask pipeline, optimized** |

**You're not paying for code. You're buying back months of your life.**

---

## Who This Is For

- **Indie Developers** — Ship an AI desktop companion without reinventing transparent window infrastructure
- **VTubers & Content Creators** — Build interactive desktop mascots for streams or fan engagement
- **AI Companion App Builders** — A polished, extensible shell for LLM-powered characters
- **Live2D Artists** — Bring your models to life beyond static showcases
- **Hobbyists & Tinkerers** — A solid starting point for desktop AI experiments

---

## What You Get

- Full source code (TypeScript frontend + Rust backend)
- Cross-platform click-through transparency pipeline
- Live2D rendering with eye tracking & expression system
- LLM chat integration with streaming + emotion detection
- Autonomous behavior engine (8 behavior types)
- OpenAI-compatible API client (7+ providers: Ollama, OpenAI, OpenRouter, Groq, Together AI, LM Studio, vLLM)
- Comprehensive documentation (installation, API guide, customization)
- Commercial license — build and sell your own apps

---

## Pricing

| Personal | Indie | Business |
|----------|-------|----------|
| **$49** | **$79** | **$149** |
| 1 developer | 1 developer | Up to 5 developers |
| 1 commercial app | 1 commercial app | Unlimited commercial apps |
| Lifetime updates | Lifetime updates | Lifetime updates + priority support |

<div align="center">

[**Get on Lemon Squeezy →**](https://roistore.lemonsqueezy.com/checkout/buy/bbd0dbc2-02c9-4442-a810-5e4bc6235d62) | [**Get on Gumroad →**](https://dakju.gumroad.com/l/animo-starter-kit)

</div>

---

## FAQ

**Q: Do I need to know Rust?**
No. The Rust backend is complete and battle-tested. You'll spend 95% of your time in TypeScript customizing the character, personality, and UI.

**Q: Is the Live2D SDK included?**
The Live2D Cubism SDK Core must be obtained separately from [live2d.com](https://www.live2d.com) (free for indie use). The kit includes everything else.

**Q: Can I use this commercially?**
Yes. The license allows you to build and sell apps derived from this code. You cannot redistribute the kit itself.

**Q: What LLM should I use?**
For development: [Ollama](https://ollama.ai) (free, local). For production: any OpenAI-compatible provider — zero code changes needed.

**Q: What platforms are supported?**
macOS and Windows. Both from a single codebase.

---

## License

This is a commercial product. Source code is provided upon purchase. See [LICENSE](LICENSE) for details.

---

<div align="center">

*Stop building plumbing. Start building characters.*

**[Get on Lemon Squeezy →](https://roistore.lemonsqueezy.com/checkout/buy/bbd0dbc2-02c9-4442-a810-5e4bc6235d62)** | **[Get on Gumroad →](https://dakju.gumroad.com/l/animo-starter-kit)**

Made by [OpenClo](mailto:animo.starter@gmail.com)

</div>
