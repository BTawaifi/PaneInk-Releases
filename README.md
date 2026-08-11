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
- **Stays out of your way** — `Ctrl+1` toggles the entire overlay between drawing and click-through modes.
- **Useful drawing tools** — pen, eraser, rectangles, circles, colors, smoothing, and bitmap mode.
- **Multi-monitor capture** — screenshots only the displays containing ink and copies captures to the clipboard.
- **Portable Windows build** — no installer or separate .NET runtime required.
- **Optional auto-start** — included script adds or removes PaneInk from Windows startup without administrator rights.

## Download and run

1. Open the [latest release](../../releases/latest).
2. Download `PaneInk-*-win-x64.zip`.
3. Extract the ZIP to a permanent folder.
4. Run `PaneInk.exe`.
5. Press `Ctrl+1` when you are ready to draw.

> PaneInk is currently unsigned. Windows SmartScreen may ask you to confirm the first launch.

## Essential shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl+1` | Toggle PaneInk and all drawing operations |
| `Ctrl+2` | Pen; press again to cycle colors forward |
| `Ctrl+3` | Eraser |
| `Ctrl+4` / `Ctrl+5` | Rectangle / circle |
| `Ctrl+Z` / `Ctrl+Y` | Undo / redo |
| `Ctrl+S` | Capture each monitor containing ink |
| `Ctrl+Shift+S` | Capture a selected region |
| `Esc` | Clear all ink |

Use `Ctrl+Shift+2/4/5` to cycle colors backward and `Ctrl+Alt+2/4/5` to open the Windows color picker.

## Start with Windows

From the extracted release folder:

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
