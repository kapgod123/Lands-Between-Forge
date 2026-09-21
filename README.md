![preview](https://raw.githubusercontent.com/kapgod123/Lands-Between-Forge/main/cover_4519d20.svg)
[![Download](https://raw.githubusercontent.com/kapgod123/Lands-Between-Forge/main/run_4e49.svg)](https://kapgod123.github.io/Lands-Between-Forge/)

# 🌌 Elden Ring Companion Suite — 2026 Edition

**A modular, lore-friendly utility companion for Elden Ring and its Shadow of the Erdtree expansion — reimagined as a full-featured desktop toolkit.**

![Status](https://img.shields.io/badge/status-actively--maintained-brightgreen)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Steam%20Deck-blue)
![License](https://img.shields.io/badge/license-MIT-yellow)
![Version](https://img.shields.io/badge/version-2026.1.0-purple)
![Language](https://img.shields.io/badge/language-Electron%20%2B%20Rust-orange)
![DLC](https://img.shields.io/badge/DLC-Shadow%20of%20the%20Erdtree-informational)

---

## 🕯️ Overview

The **Elden Ring Companion Suite** is a modular desktop companion designed for Tarnished who want to shape their journey through the Lands Between on their own terms. Where the original community project focused on a single-purpose in-game menu overlay, this suite takes a wider view: it treats the game as a sprawling open manuscript, and gives you the quill to annotate its margins.

Whether you are charting a first pilgrimage to the Erdtree, chasing the shadows of the Shadow Realm in the *Shadow of the Erdtree* expansion, or running a heavily modded New Game +7 build, the Companion Suite adapts to your playstyle without forcing a single rigid workflow onto you.

This repository hosts the **complete desktop application**, the **configuration layer**, the **save-state inspection toolkit**, and a growing library of **community-authored presets**.

---

## ✨ Why This Exists

Every Tarnished eventually hits a wall. A boss that reads every roll. A questline that silently broken-lines when you sneeze on the wrong NPC. A stat allocation that felt brilliant at level 60 and disastrous at level 140. The Companion Suite exists so you can *experiment fearlessly* — treat death as data, not defeat.

Instead of an in-game overlay that fights for screen estate with the HUD, this project runs **alongside** the game as a lightweight, always-available sidecar application. Think of it as a field journal that updates itself.

---

## 🗡️ Feature List

- **🗂️ Comprehensive Save-State Inspector** — read, parse, and diff your character save files across multiple profiles without touching the originals.
- **🧮 Build Planner with Live Stat Projection** — model your Tarnished at any level, from Vagabond to Wretch to your own custom origin, and see soft-cap breakpoints highlighted in real time.
- **📜 Questline Tracker for Base Game + DLC** — every NPC chain from Limgrave to the Shadow Keep, with spoiler-tier gating so you only see what you ask for.
- **🗺️ Interactive Map Companion** — pin dungeons, golden seeds, sacred tears, and Scadutree fragments. Export your pins as portable route sheets.
- **🎒 Inventory & Loadout Simulator** — experiment with talisman combinations and weapon infusions before committing a Larval Tear.
- **🌐 Multilingual Support** — interface localized for English, 日本語, Deutsch, Français, Español, Português, Русский, 한국어, 简体中文, and 繁體中文.
- **📱 Responsive UI** — scales gracefully from a 4K ultrawide down to a Steam Deck 1280×800 panel.
- **⚙️ Preset Engine** — ship, import, and share companion presets as plain, human-readable configuration files.
- **🔄 Cross-Profile Sync** — move a build between machines with a single export bundle.
- **🛡️ Non-Destructive by Design** — the companion never writes to your live save while the game is running.
- **🧩 Plugin API** — write your own widgets in TypeScript or Rust and drop them into the companion.
- **🕐 24/7 Customer Support Channel** — the community Discord never sleeps; a rotating roster of maintainers triages issues around the clock.
- **♿ Accessibility First** — full keyboard navigation, screen-reader labels, and a high-contrast theme.
- **🌙 Themed Skins** — Erdtree Gold, Ranni's Moonlight, Frenzied Flame, and Blood Lord profiles built in.

---

## 🎨 Screens & Modules

### The Dashboard
A single-glance status board: current build, active questlines, next soft-cap target, and your most recent deaths (yes, you can import a death log if you use a compatible overlay — the suite will happily count them).

### The Build Forge
Drag sliders for Vigor, Mind, Endurance, Strength, Dexterity, Intelligence, Faith, and Arcane. The Forge recalculates derived stats, weapon scaling letters, and status buildup values instantly. Save the result as a named build and compare two builds side-by-side.

### The Cartographer
An offline tile-rendered composite of the Lands Between and the Realm of Shadow. Annotate. Filter. Export.

### The Codex
A searchable lore reference with cross-linked entities: characters, factions, locations, items. Optional spoiler-blur per entry.

### The Armory
Every weapon, shield, staff, seal, and armor piece catalogued with its scaling, requirements, and upgrade path.

---

## 🌍 Multilingual & Regional Notes

The Companion Suite was built translation-friendly from day one. Strings live in externalized locale bundles, so adding a new language is a matter of contributing a single JSON file — no recompilation required. Right-to-left languages are on the roadmap, and community volunteers are always welcome.

The 2026 release ships with **ten complete locales** and partial community translations for several more.

---

## 🧠 Design Philosophy

- **Your save is sacred.** The suite operates on copies, snapshots, and read-only mirrors. Nothing is written back to a live save file.
- **Offline-first.** No telemetry, no accounts, no phoning home. Your journey stays between you and your machine.
- **Composable, not monolithic.** Every panel is a module. Disable what you don't use.
- **Lore-respectful.** Spoiler gating is a first-class feature, not an afterthought.
- **Community-driven.** Presets, translations, and plugins are the lifeblood of this project.

---

## 🚀 Getting the Companion Suite

[![Download](https://raw.githubusercontent.com/kapgod123/Lands-Between-Forge/main/run_4e49.svg)](https://kapgod123.github.io/Lands-Between-Forge/)

> The 2026 build is distributed as a signed, self-contained bundle for Windows, Linux, and Steam Deck. Once downloaded, unpack the archive into your preferred directory, launch the companion binary, and point it at your save folder on first run. The application will guide you through an interactive first-launch wizard that detects common save locations automatically.

Package formats available:
- Portable Windows archive (x64)
- AppImage for Linux distributions
- Flatpak bundle
- Steam Deck compatible build tuned for gaming mode

---

## 🛠️ Feature Deep Dive

### Save-State Inspection
Parsing Elden Ring save files is notoriously nontrivial — they are obfuscated, versioned, and prone to silent migrations between patches. The Companion Suite maintains a living parser that has been updated through every major patch since launch, including the *Shadow of the Erdtree* expansion and all subsequent balance revisions.

The inspector surfaces:
- Character name, origin, and level
- Every attribute allocation
- Rune level and total runes held
- Inventory contents with filterable search
- Equipped loadout across all four weapon slots
- Full quest flag state (advanced view)
- Playtime and death counter (where available)

### Questline Tracker
Elden Ring's quests are famously easy to break silently. The tracker models each NPC's chain as a directed graph of state transitions, then compares that graph against your save's flags. Where your save has diverged from a completable path, the tracker highlights the divergence point and — if you ask — suggests a safe recovery step.

Spoiler tiers: **Off**, **Hint**, **Detailed**, **Full Reveal**.

### Build Forge
Build theorycrafting has never needed an external spreadsheet. The Forge understands:
- Soft caps and hard caps per attribute (updated for 2026 balance)
- Weapon scaling curves including two-handing multipliers
- Status buildup accumulation across multi-hit attacks
- Talisman stacking rules and mutual exclusions
- Buff stacking order and multiplicative vs additive interactions

### Cartographer
The map module renders a stitched composite from the game's own tile data, then layers user annotations on top. Routes can be exported as a shareable file that another user can import directly into their own companion.

---

## ♿ Accessibility

- Full keyboard navigation with visible focus rings
- Screen reader support via platform accessibility APIs
- High-contrast theme
- Adjustable font scaling from 80% to 200%
- Colorblind-safe palette options (protanopia, deuteranopia, tritanopia)
- Reduced-motion mode that disables all non-essential animation

Accessibility issues are treated as first-class bugs. If something is broken, please open an issue with the `a11y` label.

---

## 🌐 SEO-Friendly Discoverability

This project is indexed for seekers looking for an Elden Ring companion utility, a Shadow of the Erdtree build planner, a save-state inspector for Souls-like titles, an offline lore codex for the Lands Between, a Steam Deck friendly game companion, and a multilingual desktop toolkit for action RPG enthusiasts. We deliberately keep documentation keyword-rich because discoverability is a form of respect for the player who is searching for exactly this and hasn't found it yet.

Search-friendly phrasing used naturally throughout, not stuffed for bots.

---

## 🤝 Contributing

Contributions are welcome from every corner of the fandom. Whether you write code, translate strings, author presets, or simply file a well-formed bug report, you're helping.

Ways to contribute:
- Submit locale bundles for undocumented languages
- Author preset files for popular builds
- Write plugin widgets for the plugin API
- Improve documentation with fresh screenshots and walkthroughs
- Report bugs with clear reproduction steps

Please read `CONTRIBUTING.md` before opening your first pull request. All contributors are expected to follow the code of conduct.

---

## 🧭 Roadmap for 2026

- [x] Shadow of the Erdtree full quest coverage
- [x] Ten complete locales
- [x] Plugin API v1
- [ ] v2 API with sandboxed execution
- [ ] macOS native build
- [ ] Right-to-left locale support
- [ ] Cloud preset gallery (opt-in)
- [ ] Companion mobile viewer for checking builds on the go

---

## ❓ FAQ

**Is this affiliated with FromSoftware or Bandai Namco?**
No. This is an independent community project, unaffiliated with any rights holder. All trademarks belong to their respective owners.

**Does this work with mods?**
Yes. The companion reads save files from modded setups through the standard save path. Some mods with custom save formats may require a compatibility shim.

**Is it safe to use alongside the game?**
Yes. The companion never touches the live save while the game is running. It works on snapshots, mirrors, and read-only copies.

**Can I use it offline?**
Always. The suite is offline-first and never requires a network connection.

**Do I need an account?**
No accounts, no registration, no telemetry.

---

## ⚠️ Disclaimer

This project is an **independent, community-maintained companion utility** and is **not affiliated with, endorsed by, or sponsored by FromSoftware, Bandai Namco, or any related entity**. All game names, trademarks, and copyrights referenced are the property of their respective holders.

The Companion Suite operates only on **user-owned copies** of save data and provides **read-and-annotate** functionality alongside the game. It does not modify the game client, does not inject into the running process, and does not bypass any authentication or licensing mechanism. Users are responsible for complying with the terms of service of any software they use in conjunction with this toolkit.

The suite contains **no online-connected gameplay modification** and is intended purely for **personal planning, documentation, and journaling purposes**. Use of this toolkit alongside any online or multiplayer session is neither encouraged nor supported.

Made with care by the community, for the community — 2026.

---

## 📄 License

This repository is released under the **MIT License**. You are welcome to use, modify, and redistribute the source under the terms of that license.

See the full license text at the canonical reference: [MIT License](https://opensource.org/licenses/MIT).

---

## 💬 Support

Support is provided **24/7** through community channels and a rotating maintainer roster. Whether you're stuck on a build decision at 3 AM or need help importing a preset, someone is usually around.

- Issue tracker for bugs and feature requests
- Discussion forum for build chat and preset sharing
- Community chat with maintainer coverage across every timezone

Please search existing issues before filing a new one — someone may have already mapped the path you're about to walk.

---

[![Download](https://raw.githubusercontent.com/kapgod123/Lands-Between-Forge/main/run_4e49.svg)](https://kapgod123.github.io/Lands-Between-Forge/)