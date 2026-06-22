# DIAVLO DROP

**One beat. Every platform.**

A desktop application for music producers. Drop a beat and get everything you need to publish on every platform.

![DIAVLO DROP](docs/screenshots/app.png)

## The Problem

You produce a beat. Then you need:
- A master WAV and MP3
- Tagged previews
- YouTube video with waveform visualizer
- Vertical and square videos for TikTok/Reels
- Cover artwork and thumbnails
- Metadata descriptions for every platform
- Everything packaged in one ZIP

That's hours of work per beat. DIAVLO DROP does it in one click.

## Features

- **Import** - Drag and drop WAV, FLAC, MP3, M4A
- **Analyse** - Real BPM and key detection via FFmpeg
- **Edit** - Waveform player with metadata editor
- **Producer Tag** - Mix audio tags with volume, fade, pan control
- **Artwork** - 6 procedural templates (Obsidian, Chrome, Inferno, Void, Signal, Canary Night)
- **Video** - 6 visualizer types with FFmpeg rendering
- **Export** - Full Drop, YouTube, TikTok, Beat Store presets
- **Metadata** - Auto-generated YouTube, Instagram, TikTok descriptions
- **Queue** - Batch export multiple beats
- **Local-first** - No accounts, no telemetry, no uploads

## Quick Install

```powershell
irm "https://github.com/Nikolai-coder/diavlodrop/releases/latest/download/install.ps1" | iex
```

Or download the installer from [Releases](https://github.com/Nikolai-coder/diavlodrop/releases).

## Usage Flow

1. Open DIAVLO DROP
2. Complete the onboarding (name, output folder)
3. Drop a beat file onto the Library
4. Edit metadata (BPM, key, title, genre)
5. Configure producer tag (optional)
6. Create artwork with built-in templates
7. Render videos with waveform visualizers
8. Select export preset and start
9. Get a complete package in your output folder

## Formats

| Input | WAV, FLAC, MP3, M4A |
|-------|---------------------|
| Master | WAV 44100Hz 16-bit |
| Audio | MP3 320kbps |
| Tagged | MP3 with producer tag |
| Previews | 60s / 30s MP3 |
| Video | MP4 H.264 AAC |
| Artwork | PNG 3000x3000 / 1280x720 / 1080x1920 / 1080x1080 |
| Package | ZIP with all assets |

## Privacy

DIAVLO DROP is local-first. Everything runs on your machine. No accounts, no telemetry, no data uploads. [Learn more](docs/privacy.md)

## Architecture

- **Frontend**: React 19 + TypeScript + Vite
- **Backend**: Rust + Tauri 2
- **Audio**: FFmpeg / FFprobe
- **Artwork**: Rust image crate (procedural)
- **Storage**: SQLite
- **Installer**: NSIS

[Architecture docs](docs/architecture.md)

## Development

```powershell
# Prerequisites
npm install

# Development
npm run tauri dev

# Build
npm run tauri build

# Tests
npm test
cargo test
```

## Roadmap

- v0.1.0 - Initial release with core features
- v0.2.0 - MIDI export, batch processing improvements
- v0.3.0 - Plugin system, custom visualizers
- v1.0.0 - Stable release with GPU acceleration

[Full roadmap](ROADMAP.md)

## License

MIT © 2026 Diavlo
