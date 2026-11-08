# Source Engine Standalone Launcher for Linux
This repository provides a pre-compiled, standalone Source Engine launcher optimized for modern 64-bit Linux distributions (Arch Linux, Debian, Ubuntu). 

### Why this is important for Linux users:
While Valve officially provides a native Linux version of Half-Life 2 on Steam, it is an outdated 32-bit build that frequently suffers from library conflicts, audio issues, and font rendering glitches on modern rolling-release distributions. This 64-bit standalone build addresses those compatibility issues, removes the Steam client overhead, and introduces native Vulkan support for maximum performance.

A pre-compiled standalone Source Engine launcher for Linux (x86_64), based on the nillerusr branch. This build allows you to play Half-Life 2 and other Source games independently without Steam, with native Vulkan support.

## Features
- **Standalone:** Runs without the Steam client or internet dependency.
- **Vulkan Support:** Better performance and stability on Linux using the `-vulkan` flag.
- **Compatibility:** Fixed for modern distributions including Arch Linux and Debian/Ubuntu.

## Supported Games
- Half-Life 2 (Base, Episode One, Episode Two)
- Portal
- Counter-Strike: Source

## Package Structure

```text
hl2/
├── hl2_launcher         (Main engine binary)
└── bin/                 (Folder containing essential compiled .so libraries)
    ├── engine.so
    ├── launcher.so
    ├── vstdlib.so
    └── ...
```

## ⚠️ Important Requirement (Game Version)

This engine **does not support the latest 20th Anniversary Edition** update of Half-Life 2. You must use the classic/older build. If you are using Steam game files, revert to the legacy build by following these steps:

1. Open **Steam**.
2. Right-click on **Half-Life 2** and select **Properties**.
3. Click on the **Betas** tab on the left.
4. Under "Beta Participation", select **`steam_legacy - pre-20th anniversary build`** from the dropdown menu.
5. Close the window and let Steam re-download the older compatible game files.

## How to Install and Play

1. Download the latest release from the Releases section: `source-engine-64bit-vulkan-standalone.tar.gz`.
2. Extract the archive:
   ```bash
   tar -xzvf source-engine-64bit-vulkan-standalone.tar.gz
   cd hl2
   ```
3. Copy your original retail game folders (e.g., `hl2`, `portal`, `cstrike`, `platform`) and paste them directly into this extracted `hl2` folder (beside `hl2_launcher` and the `bin` folder).
4. Set execution permissions for the binary:
   ```bash
   chmod +x hl2_launcher
   ```
5. Launch your game using the Terminal:
   - **Half-Life 2:** `./hl2_launcher -vulkan`
   - **Portal:** `./hl2_launcher -game portal -vulkan`
   - **Counter-Strike: Source:** `./hl2_launcher -game cstrike -vulkan`

---

### 📷 Gameplay Screenshot


---
*Non-commercial use only. All game assets belong to Valve Corporation.*
