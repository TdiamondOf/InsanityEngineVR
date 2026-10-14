## ⚠️ IMPORTANT — MUST READ

This is a VERY early build. Expect bugs.

Hand tracking: You may need to adjust settings in the Insanity menu (F10) to get your hands tracking correctly.
Camcorder: Currently broken. A fix is in progress.

Found a bug? Report it on the Issues page.


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

- [ ] **Outlast (2013) on PC.** Tested on the Steam version. GOG/Epic not tested yet.
- [ ] **A PC VR headset with motion controllers.** Tested on Meta Quest via Quest Link and Virtual Desktop. SteamVR headsets should work but haven't been tested.
- [ ] **An active OpenXR runtime.** If you have more than one installed (SteamVR, Meta app, Virtual Desktop), make sure the one you're using is set as the active OpenXR runtime.
- [ ] **A Vulkan-capable GPU.** Anything from the last ~8 years is fine.

## Installation

- [ ] **Run Outlast once normally, then quit.** This creates the game's settings files the setup script needs.
- [ ] **Open the game folder.** In Steam, right-click Outlast → Manage → Browse local files, then open `Binaries\Win64` (the folder with `OLGame.exe`).
- [ ] **Copy everything from the zip into that folder**, next to `OLGame.exe`:
- [ ] `d3d9.dll` — the mod
- [ ] `openxr_loader.dll` — talks to your headset
- [ ] `dxvk_d3d9.dll` — makes the game run smoothly (DXVK)
- [ ] `outlastvr.ini` — mod settings
- [ ] `OutlastVR_DoorHandles.ini` — door-grab calibration
- [ ] `Outlast-VR.bat` — setup / uninstall script
- [ ] **Run `Outlast-VR.bat`**, choose Install, and enter your headset's refresh rate (72 / 80 / 90 / 120). It backs up your game settings, sets the FOV and frame cap, and turns off mouse look and motion blur.
- ⚠️ **Do not turn off Depth of Field in the game's settings.** Night vision needs it. The mod already removes the blur.
- [ ] **Start your VR runtime first** (Quest Link, Virtual Desktop, or SteamVR) with your headset connected.
- [ ] **Launch Outlast from Steam.** The mod loads automatically.

**On your monitor:** **F10** opens the mod menu. **G** recenters your view.

## Uninstall

Run `Outlast-VR.bat` again and choose Uninstall. This restores your original game settings and deletes all the mod files from `Binaries\Win64`: `d3d9.dll`, `openxr_loader.dll`, `dxvk_d3d9.dll`, `outlastvr.ini`, `OutlastVR_DoorHandles.ini`, and finally `Outlast-VR.bat` itself.

### Updating

If Windows asks to replace files:
- `d3d9.dll`, `openxr_loader.dll`, `dxvk_d3d9.dll`, `Outlast-VR.bat`: **Yes**
- `outlastvr.ini`, `OutlastVR_DoorHandles.ini`: **No**, so you keep your settings

## Settings

Press **F10** in-game, or click the arrow in the corner, to open the Insanity Engine VR menu on your monitor. Every change saves automatically. Use **Reset to Defaults** if anything gets weird.

## Status

Actively in development. Working: head tracking, the hand-held camcorder, turning, the sharp UI, and motion-tracked hands and arms.

Coming next: grabbable doors, night vision through the camcorder screen, and physical holsters.

## Picking things up & interacting

**Batteries and story items:** There is no pickup prompt. Just walk up to the item and press **X** — if you're close enough, it's picked up automatically.

**Some story interactions:** For certain scripted actions, the prompt only appears while you're **crouched**. If you walk up to something and no prompt shows, **crouch down** — the prompt will appear partway through the crouch. Press the button while you can see it to trigger the action.

## Known Issues

- **Night vision:** the night-vision light can still show partly in your own view. It's aimed through the camcorder screen, but each eye looks through the screen at a slightly different angle.
- **HUD dot:** the centre dot isn't centred in the headset.
- **No pickup prompt:** prompts don't appear in VR. **X** picks up the nearest item within 1.5 m, with the game's own pickup animation.
- **Aiming left/right** still comes from your body, not your head.
- **Tested setups:** Steam version with Meta Quest (Quest Link and Virtual Desktop) only. GOG/Epic copies and SteamVR headsets are untested.

## Credits & Licenses

Insanity Engine VR is by T-Diamond (TdiamondOf). It is a fork of jrush64's outlast-vr-mod and is licensed under **GPL-3.0** (see `LICENSE`). The source code for each release is attached to it on the Releases page.

- [jrush64's outlast-vr-mod](https://github.com/jrush64/outlast-vr-mod) — the original mod this is forked from (GPL-3.0)
- [DXVK](https://github.com/doitsujin/dxvk) — Direct3D 9 to Vulkan, bundled as `dxvk_d3d9.dll` (zlib/libpng)
- [OpenXR Loader](https://github.com/KhronosGroup/OpenXR-SDK) by Khronos — bundled as `openxr_loader.dll` (Apache-2.0)
- [MinHook](https://github.com/TsudaKageyu/minhook) — API hooking, built into `d3d9.dll` (BSD-2-Clause)
- [Dear ImGui](https://github.com/ocornut/imgui) — the settings menu, built into `d3d9.dll` (MIT)

Full license notices for every bundled component are in `THIRD-PARTY-NOTICES.txt`.


