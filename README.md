<p align="center">
  <img src="assets/PaneInk.png" alt="PaneInk icon" width="144">
</p>

<h1 align="center">PaneInk</h1>

<p align="center"><strong>Draw naturally over anything on your Windows desktop.</strong></p>

<p align="center">
  <a href="../../releases/latest"><img alt="Download latest release" src="https://img.shields.io/badge/Download-Latest_release-22c55e?style=for-the-badge"></a>
  <img alt="Windows 10 and 11" src="https://img.shields.io/badge/Windows-10_%7C_11-0078d4?style=for-the-badge&logo=windows11">
  <img alt="MIT License" src="https://img.shields.io/badge/License-MIT-64748b?style=for-the-badge">
</p>

PaneInk is a lightweight, pressure-sensitive drawing overlay built for quick explanations, presentations, lessons, reviews, and visual thinking. Toggle it on, draw over any app, then toggle it off without losing your ink.

## Why PaneInk?

- **Natural pen input** — smooth pressure-sensitive strokes without artificial circular ends.
- **Stays out of your way** — `Ctrl+Alt+1` is the only global hotkey PaneInk ever holds. Toggle the overlay off and every click goes straight back to the desktop; your ink comes back exactly as you left it when you toggle on again.
- **A full toolset** — pen, highlighter, eraser, line, arrow, rectangle, circle, text labels, numbered step badges, and opaque redaction blocks, plus a bitmap drawing mode.
- **Multi-monitor, DPI aware** — screenshots capture only the displays containing ink and copy straight to the clipboard; ink, pointer and captures stay aligned even across monitors with different scaling.
- **Install your way** — a per-user installer (no administrator prompt) or a portable, self-contained ZIP. No separate .NET runtime to install either way.
- **Optional auto-start** — the installer's checkbox, or the bundled script for the portable build, adds or removes PaneInk from Windows startup without administrator rights.

## Download and run

Grab the latest release from the [Releases page](../../releases/latest).

- **Installer** — run `PaneInk-<version>-win-x64-setup.exe`. It installs per user into `%LOCALAPPDATA%\Programs\PaneInk`, adds a Start Menu entry, offers to start PaneInk at sign-in, and registers an uninstaller in **Apps & features**.
- **Portable ZIP** — extract `PaneInk-<version>-win-x64.zip` to a permanent folder and run `PaneInk.exe`.

> PaneInk is currently unsigned. Windows SmartScreen may ask you to confirm the first launch.

Press `Ctrl+Alt+1` when you are ready to draw.

## Essential shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl+Alt+1` | Toggle PaneInk (the only global hotkey — everything else below only works while it's on) |
| `P` | Pen; press again to cycle colors forward |
| `E` | Eraser |
| `R` / `C` | Rectangle / circle |
| `K` | Redact — an opaque block over anything that must not appear in a screenshot |
| `B` | Toggle bitmap drawing mode |
| `Ctrl+Z` / `Ctrl+Y` | Undo / redo |
| `Ctrl+S` | Capture each monitor containing ink |
| `Ctrl+Shift+S` | Capture a selected region |
| `Ctrl+Del` | Clear all ink |
| `Esc` | Cancel the current action, or toggle the overlay off — this never deletes your ink |

`Shift+<key>` cycles a tool's color backward, and `Ctrl+P` opens the Windows color picker for the current tool. The floating toolbar (drag its grip to move it, or collapse it with the chevron) covers the rest — highlighter, line, arrow, text labels and numbered badges included.

## Start with Windows

The installer offers this with its **Start PaneInk when I sign in** checkbox. For the portable ZIP, run the bundled script from the extracted folder:

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\set-autostart.ps1 -Add
```

Remove it at any time with:

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\set-autostart.ps1 -Remove
```

## Verify your download

Each release includes a `.sha256` checksum file. In PowerShell:

```powershell
Get-FileHash .\PaneInk-*-win-x64.zip -Algorithm SHA256
```

Compare the result with the hash inside the downloaded `.sha256` file.

## Requirements

- Windows 10 or Windows 11
- x64 processor

PaneInk is licensed under the MIT License. The license is included in every release package; the application source is maintained in a private repository.
