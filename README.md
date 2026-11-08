# source-engine-linux-launcher
Pre-compiled standalone Source Engine launcher supporting Vulkan for Linux x86_64.
# Source Engine Standalone Launcher for Linux

A pre-compiled standalone Source Engine launcher for Linux (x86_64), based on the nillerusr branch. This build allows you to play Half-Life 2 and other Source games independently without Steam, with native Vulkan support.

## Features
- **Standalone:** Runs without the Steam client or internet dependency.
- **Vulkan Support:** Better performance and stability on Linux using the `-vulkan` flag.
- **Compatibility:** Fixed for modern distributions including Arch Linux and Debian/Ubuntu.

## Supported Games
- Half-Life 2 (Base, Episode One, Episode Two)
- Portal
- Counter-Strike: Source

## How to Install and Play

1. Download the latest release from the Releases section: `source-engine-64bit-vulkan-standalone.tar.gz`.
2. Extract the archive:
   ```bash
   tar -xzvf source-engine-64bit-vulkan-standalone.tar.gz
   cd hl2
   ```
3. Copy your original retail game folders (e.g., `hl2`, `portal`, `cstrike`, `platform`) and paste them directly into this extracted `hl2` folder.
4. Set execution permissions for the binary:
   ```bash
   chmod +x hl2_launcher
   ```
5. Launch your game using the Terminal:
   - **Half-Life 2:** `./hl2_launcher -vulkan`
   - **Portal:** `./hl2_launcher -game portal -vulkan`
   - **Counter-Strike: Source:** `./hl2_launcher -game cstrike -vulkan`

---
*Non-commercial use only. All game assets belong to Valve Corporation.*
