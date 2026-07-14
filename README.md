# Atomic Data Manager

An intelligent data-block manager for Blender — rapidly clean unused data, inspect where data-blocks are used, view rich statistics, and catch missing files before they break a render.

> **Unofficial fork, maintained by [Purple Hato](https://github.com/PurpleHato), updated for modern Blender (4.3 – 5.1.2+).**
> This project is **not affiliated with, endorsed by, or associated with Remington Creative.** The original add-on (© 2019 Remington Creative, GPL-3.0) is no longer maintained and its product website is offline, so this fork keeps the tool working on current Blender releases. Full credit for the original work belongs to Remington Creative.

## Features

- **Rapid cleaning** — *Nuke* (remove a whole category) or *Clean* (remove only unused data-blocks), per category: collections, images, lights, materials, node groups, particles, textures, worlds.
- **Inspection tools** — see exactly where and how a data-block is used, with rename / replace / duplicate / delete and a fake-user toggle.
- **Rich statistics** — per-category total / unused / unnamed / missing counts, plus blend-file size.
- **Missing-file detection** — warned about missing image and library paths on load; reload or remove them in bulk.
- **Pie menu** — drive common actions from a configurable hotkey (default `D`).
- **Data security** — confirmation dialogs preview exactly what will be removed; undo supported.

## Requirements

Blender **4.3 or newer** (developed and tested on 5.1.2). Earlier versions are not supported — the code uses Grease Pencil v3 identifiers introduced in 4.3.

## Installation

Atomic Data Manager ships as a Blender **Extension**.

1. Download `atomic_data_manager-2.0.0.zip` from the [releases page](https://github.com/PurpleHato/atomic-data-manager/releases).
2. Blender → **Edit → Preferences → Extensions** → drop-down (∨) → **Install from Disk** → select the zip.
3. Enable **Atomic Data Manager (2026 - Hato)**.
4. Find it under **Properties → Scene**.

> The zip has `blender_manifest.toml` at its root (no wrapper folder) — that is correct for an extension; Blender creates the install folder from the manifest `id`.

## What changed in 2.0.0

- Repackaged as a Blender 4.2+ **Extension** (`blender_manifest.toml`); minimum Blender raised to **4.3**.
- Removed the bundled legacy auto-updater (incompatible with the Extension system — Blender's Extensions platform handles updates now).
- Converted all internal imports to relative and re-keyed preferences off the live package name (required for the `bl_ext` extension namespace).
- Fixed the Blender 5.0 compositor API change (`scene.node_tree` → `scene.compositing_node_tree`).
- Fixed Grease Pencil v3 object-type detection and several long-standing bugs.
- Version bumped to **2.0.0**.

## License

GPL-3.0-or-later. See [`LICENSE.txt`](LICENSE.txt). Based on the original Atomic Data Manager © 2019 Remington Creative.
