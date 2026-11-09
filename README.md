# Source Engine Standalone Launcher for Linux

A pre-compiled standalone Source Engine launcher for Linux (x86_64), based on the nillerusr branch. This build allows you to play Half-Life 2 and other Source games independently without Steam, with native OpenGL rendering via Valve's ToGL translation layer.

## Features
- **Launcher:** Runs without the Steam client or internet dependency.
- **Stable OpenGL Performance:** Utilizes the integrated ToGL translation layer for optimal graphics compatibility on modern desktop Linux systems.
- **Compatibility:** Native 64-bit build fixed for modern distributions including Arch Linux and Debian/Ubuntu.

## Supported Games
- Half-Life 2 (Base, Episode One, Episode Two)
- Portal
- Counter-Strike: Source 
- Other
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

1. Download the latest release from the Releases section: `source-engine-64bit-launcher.tar.gz`.
2. Extract the archive:
   ```bash
   tar -xzvf source-engine-64bit-launcher.tar.gz
   cd hl2
   ```
3. Copy your original retail game folders (e.g., `hl2`, `portal`, `cstrike`, `platform`) and paste them directly into this extracted `hl2` folder (beside `hl2_launcher` and the `bin` folder).
4. Set execution permissions for the binary:
   ```bash
   chmod +x hl2_launcher
   ```
5. Launch your game using the Terminal:
   - **Half-Life 2:** `SDL_VIDEODRIVER=x11 ./hl2_launcher -windowed -noborder`
   - **Portal:** `SDL_VIDEODRIVER=x11 ./hl2_launcher -game portal -windowed -noborder`
   - **Counter-Strike: Source:** `SDL_VIDEODRIVER=x11 ./hl2_launcher -game cstrike -windowed -noborder`
5. Launch your game using the quick script:
   ```bash
   ./source-engine.sh
   ```

## 🛠️ Troubleshooting (Wayland Issues)

If you are running a modern Linux desktop environment using **Wayland** (like GNOME or KDE Plasma on Arch Linux) and the game freezes or fails to open a window after showing the graphics target, you must force the engine to run via **XWayland** by appending the X11 video driver variable.

Always execute the launcher using the full combined parameters:
```bash
SDL_VIDEODRIVER=x11 ./hl2_launcher -windowed -noborder
```

---

## 📷 Screenshots & Package Layout

### 1. Basic Game Directory Structure
Ensure your legally owned retail game folders (`hl2`, `platform`, etc.) are placed directly beside the compiled launcher as shown below:

<p align="center">
  <img src="https://github.com/user-attachments/assets/5f89c801-e288-4d8b-a8f1-094b3cea49df" alt="Basic Structure" width="90%">
</p>

### 2. Multi-Episode Directory Layout (Optional)
The launcher is fully capable of handling separate data footprints for Episode One (`episodic`), Episode Two (`ep2`), and `lostcoast` within the same workspace:

<p align="center">
  <img src="https://github.com/user-attachments/assets/6a5d2b0d-7546-41fd-b68a-6e9be8946dd3" alt="Multi-Episode Structure" width="90%">
</p>

### 3. Standalone Engine Execution
Proof of performance running natively with stable OpenGL rendering and XWayland environment overrides:

<p align="center">
  <img src="https://github.com/user-attachments/assets/a6d8d6bf-1d50-4949-98c5-d7f6bf4be7c2" alt="Gameplay Execution" width="90%">
</p>

---
*Non-commercial use only. All game assets belong to Valve Corporation.*
