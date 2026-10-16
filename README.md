[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://github.com/chris1111/PlistStar/blob/main/LICENSE)

<div align="center">

# ⭐ PlistStar

**A polished, dependency-free editor for macOS `.plist` files — packed into a single HTML file.**

OpenCore `config.plist` · Clover `config.plist` · LaunchAgents · `Info.plist` —
open, edit, validate and export from any browser. No install, no server, no telemetry — works fully offline.


</div>

---

## ✨ Highlights

- **Two synced views** — a collapsible **structure tree** on the left and the raw **XML Source** on the right. Every edit made in one view instantly appears in the other.
- **Click-to-jump** — select any key in the tree and the Source view scrolls to the exact line and flashes a blue marker (precise line mapping, not string search). Boolean switches jump straight to their `<true/>` / `<false/>` line.
- **BBEdit-style Preview** — line numbers and syntax highlighting for reviewing huge configs, rendered in chunks (600 + 900 lines) so the UI never freezes; soft-wrap switches off automatically on very large files.
- **Native-feeling editors for every type** — macOS-style toggles for booleans, UTC date pickers, validated number fields, and a live base64 size readout for data values.
- **Type conversion with undo** — click any type badge to convert between string, integer, real, boolean, date and data, with an undo toast if you click by accident.
- **Full right-click toolbox** — add a child or sibling, duplicate, move (or use **Alt + ↑ / ↓**), copy and delete any node.
- **One-click templates** — load the official OpenCore `Sample.plist` or Clover `config-sample.plist` right from the welcome card (dual mirror with offline cache).
- **Zero dependencies** — one HTML file. No build step, no frameworks, no runtime, no network calls. Your configs never leave your machine.

## 🚀 Getting started

1. Download **PlistStar.html**
2. Double-click it — it opens in your default browser
3. Edit your plist, then hit **⌘S / Ctrl+S** to export

> 💡 You can also simply **drag & drop** any `.plist` file onto the page to open it.

## 🧭 The three views

| View | Purpose |
|---|---|
| **Tree** | Collapsible dict/array structure with per-type editors, type badges and right-click actions |
| **Source** *(default)* | Raw XML textarea kept in live sync with the tree — hit **Apply** to re-parse hand edits |
| **Preview** | Read-only, BBEdit-style line-numbered, highlighted rendering for reviewing big configs |

## 🛠 Features at a glance

| Feature | Details |
|---|---|
| Serialization | Apple-standard tab indentation, DOCTYPE header, self-closing tags |
| Value types | string · integer · real · boolean · date · data (base64) · array · dict |
| Sync | Live two-way tree ⇄ source sync with exact line-map jump and flash |
| Big files | Chunked rendering, wrap auto-off — smooth even on huge `config.plist` files |
| Templates | OpenCore `Sample.plist` · Clover `config-sample.plist` (dual mirror + offline cache) |
| Files | Open via picker or drag & drop · export with ⌘S · copy XML to clipboard |
| Navigation | Breadcrumbs · live key filter · collapsible nodes |
| Safety | Number validation · BOM-tolerant parsing · type-conversion undo toast |

## ⌨️ Keyboard shortcuts

| Shortcut | Action |
|---|---|
| **⌘S / Ctrl+S** | Export the current plist |
| **⌘E / Ctrl+E** | Toggle the right panel |
| **⌘F / Ctrl+F** | Filter keys in the tree |
| **Alt + ↑ / ↓** | Move the selected node up / down |

## 📦 Notes & limitations

- PlistStar reads and writes **XML plists**. Binary `bplist` files are not supported — convert first with `plutil -convert xml1 file.plist`.
- Dates are edited and preserved in **UTC**, matching Apple's plist convention.
- Everything runs locally in your browser — no telemetry, no uploads, works fully offline.

## 📄 License

Copyright © 2026 **chris1111** · All Rights Reserved.


