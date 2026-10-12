# Insanity Engine VR

A 6DOF VR mod for **Outlast (2013)** with motion controls.

Play Outlast in virtual reality with full head tracking, room-scale 6DOF movement, and **motion controls**. Hold the camcorder in your hand and aim it where you want, independent of where you're looking. The thing that makes Outlast terrifying becomes something you do with your own hands.

## Features

- **True 6DOF head tracking:** lean, duck, and peek around corners with your body
- **Hand-held camcorder:** hold grip to hold and aim the camcorder with your hand instead of your head
- **Sharp UI:** menus and HUD render on their own full-resolution floating panel, so text is crisp and readable
- **Snap and smooth turning:** switchable in-game
- **In-game settings menu:** tune FOV, scale, render resolution, UI distance and size, and more, live, without restarting
- **Clean spectator view:** a normal single image on your monitor for anyone watching or recording

## Requirements

- **Outlast (2013), Steam version.** The mod only works with the Steam build. GOG, Epic, and the 32-bit version aren't supported.
- **A PC VR headset** with an OpenXR runtime set as the active runtime. Any of these work:
  - **SteamVR:** SteamVR Settings → OpenXR → "Set SteamVR as OpenXR runtime"
  - **Meta Quest Link:** Meta Quest PC app → Settings → General → set as active OpenXR runtime
  - **Virtual Desktop:** uses its own runtime (VDXR), no extra setup needed
- **Microsoft Visual C++ 2015–2022 x64 Redistributable.** Most gaming PCs already have it. If the game runs flat with no VR, install this first.

> **Note:** This mod uses `d3d9.dll`, so it can't be installed alongside other mods that use the same file (ReShade, DXVK, dgVoodoo).

## Installation

1. **Download** the latest Insanity Engine VR zip and unzip it.
2. **Open your Outlast folder.** In Steam: right-click Outlast → Manage → Browse local files.
3. **Go into `Binaries\Win64`**, the folder that contains `OLGame.exe`. *Not* the main Outlast folder.
4. **Copy all the unzipped files** into `Binaries\Win64`.
5. **Run `Outlast-VR.bat` once.** It sets up your game settings for VR (field of view, motion blur off, frame cap removed, mouse-look disabled) and backs up your original settings first.
6. **Start your headset and VR runtime first**, then launch Outlast from Steam normally. The mod loads automatically.

> If the headset or VR runtime isn't running when the game starts, the game runs flat. Close it, start your VR runtime, and launch again.

### Updating

If Windows asks to replace files:
- `d3d9.dll`: **Yes**
- `openxr_loader.dll`: **Yes**
- `outlastvr.ini`: **No**, so you keep your settings

### Uninstalling

Delete the mod files from `Binaries\Win64`, or use Steam's **Verify integrity of game files** to restore the original game.

## Settings

Press **F10** in-game, or click the arrow in the corner, to open the Insanity Engine VR menu on your monitor. Every change saves automatically. Use **Reset to Defaults** if anything gets weird.

## Status

Actively in development. Working: head tracking, the hand-held camcorder, turning, the sharp UI, and motion-tracked hands and arms.

Coming next: grabbable doors, night vision through the camcorder screen, and physical holsters.

## Credits & Licenses

This mod is a fork of jrush64's outlast-vr-mod and is licensed under **GPL-3.0**.

Bundled components:

- **DXVK** — D3D9-to-Vulkan translation. https://github.com/doitsujin/dxvk
- **jrush64's outlast-vr-mod** — original mod this is forked from (GPL-3.0). https://github.com/jrush64/outlast-vr-mod
- **MinHook** — API hooking library (BSD-2-Clause).
- **Dear ImGui** — UI library (MIT).

Each component's full license is included in the `licenses/` folder.

Also uses:
- [MinHook](https://github.com/TsudaKageyu/minhook) (BSD-2-Clause)
- [Dear ImGui](https://github.com/ocornut/imgui) (MIT)
- [OpenXR Loader](https://github.com/KhronosGroup/OpenXR-SDK) by Khronos (Apache-2.0)

See `THIRD-PARTY-NOTICES.txt` for full license notices.


