## ⚠️ IMPORTANT — MUST READ

This is an early beta. Expect bugs.

Found a bug? Report it on the Issues page, and attach `%LOCALAPPDATA%\OutlastVR\OutlastVR_Log.txt` if you can.


# Insanity Engine VR

A 6DOF VR mod for **Outlast (2013)** with motion controls.

Play Outlast in virtual reality with full head tracking, room-scale 6DOF movement, and **motion controls**. Hold the camcorder in your hand with night vision on its own little screen, or switch to the game's full-screen camcorder view. The thing that makes Outlast terrifying becomes something you do with your own hands.

## What's new in v0.2.0-beta

- **Your body follows your head.** Turn your real body and Miles turns with you; the view never swings away from where you are looking, including when you turn 180°, sprint, or vault.
- **Story interactions just work.** Keyboards, levers, valves, pumps and buttons fire on **X** when you are within reach, without aiming at them exactly.
- **Realistic camcorder.** Held in your hand, raised with the grip, night vision rendered on the camcorder's screen with its light shining through it. A switch in the menu gives you the game's original full-screen camcorder instead.
- **Walk where you look.** Pushing the left stick forward walks where your head faces.
- **Vault, mantle and climb** keep the view on your head instead of snapping to the animation.
- **Menus in the room.** The pause menu and main menu hang in front of you instead of being glued to your face.
- **New defaults:** snap turning, motion-tracked arms on, hand markers off, bloom halved.

## Features

- **True 6DOF head tracking:** lean, duck, and peek around corners with your body. The head stays attached to the body: lean up to 20 cm, further than that and the body holds you.
- **Body turns with your head:** turn in your chair or on your feet and Miles follows, with a 35° slack so small glances don't move him.
- **Hand-held camcorder:** hold the right grip to raise it; the picture and night vision are on its screen. Or pick the full-screen mode in the menu, where a tap of the grip raises it.
- **Motion-tracked arms:** Miles's arms follow your controllers (on by default).
- **Forgiving interactions:** X picks up the nearest item and works levers, valves, keyboards and pumps within 1.5 m. Doors open with a tap of Use, or grab the handle with the grip and move your hand.
- **Sharp UI:** menus and HUD render on their own full-resolution floating panel.
- **Snap and smooth turning:** switchable in-game. Snap is the default.
- **In-game settings menu:** tune everything live, without restarting.
- **Clean spectator view:** a normal single image on your monitor for anyone watching or recording.

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

## Controls

| Control | What it does |
|---|---|
| Left stick | Walk. Forward is where your head faces. |
| Right stick | Turn (snap by default, smooth in the menu). |
| Right stick up / down | Zoom the camcorder while it is up. |
| Right stick click (R3) | Night vision on / off while the camcorder is up. |
| Right grip | Camcorder. Hold to raise in Realistic mode; tap to raise and tap to lower in full-screen mode. |
| Left grip | Hold to sprint. |
| Both grips at a wardrobe or bed | Push it. |
| A | Jump / vault / climb. |
| B | Crouch. |
| X | Use: pick up the nearest item, work levers, valves, keyboards and pumps, open doors. |
| Y | New camcorder battery. |
| Menu button | Pause. |
| Keyboard G | Recenter the view. |
| Keyboard F10 | Open the mod menu on your monitor. |

## Uninstall

Run `Outlast-VR.bat` again and choose Uninstall. This restores your original game settings and deletes all the mod files from `Binaries\Win64`: `d3d9.dll`, `openxr_loader.dll`, `dxvk_d3d9.dll`, `outlastvr.ini`, `OutlastVR_DoorHandles.ini`, and finally `Outlast-VR.bat` itself.

### Updating

If Windows asks to replace files:
- `d3d9.dll`, `openxr_loader.dll`, `dxvk_d3d9.dll`, `Outlast-VR.bat`: **Yes**
- `outlastvr.ini`, `OutlastVR_DoorHandles.ini`: **No**, so you keep your settings. New settings in this version simply take their defaults.

## Settings

Press **F10** in-game, or click the arrow in the corner, to open the Insanity Engine VR menu on your monitor. Every change saves automatically. Use **Reset to Defaults** if anything gets weird.

| Group | What's in it |
|---|---|
| Turning | Snap or smooth, snap angle, turn speed. **Body turns with your head** and its threshold (35°). |
| Head tracking | Look around with your head, lean and duck, lean amount, **lean radius** (how far your head may leave the body, 20 cm), neck-to-eye distance, steadying, game camera motion. |
| Motion controls | **Miles's arms follow the controllers** (on), how much they follow, **walk where you look** (on), per-hand tilt/turn/twist offsets, hand markers (off). |
| Camcorder | **Realistic camcorder (held in hand)** (on) or the game's full screen. Night vision light through the screen and its aim, night vision screen tuning, how the camcorder sits in your hand. |
| Input | Pick up the nearest item with Use (on), **levers, valves and keyboards: no aim needed** (on), aim up/down follows your head. |
| Doors | Grip calibration for door handles. |
| HUD & menus | Sharp UI panel, size, distance, position. |
| Image quality | Reduce bloom (on), film grain, depth of field, motion blur, vignette, sharpening. |
| Stereo & scale | Depth, field of view, focus distance, swap eyes. |
| Monitor view | What the monitor shows, which eye, zoom. |
| Overlay | Mouse controls the overlay. |

## Picking things up & interacting

**Batteries, documents, keys:** there is no pickup prompt. Walk up to the item and press **X**; if you're within 1.5 m it's picked up with the game's own animation.

**Levers, valves, pumps, keyboards, buttons:** stand within reach and press **X**. You don't need to aim at them exactly. Things that need an item (a key card, a fuse) still need it, as in the flat game. If something still refuses, crouch and try again.

**Doors:** tap **X** for a quick open. Or grab the handle with the grip and move your hand to open it slowly.

## Status

Actively in development. Working: head tracking with the body following, the held camcorder with night vision on its screen, the full-screen camcorder mode, turning, walk where you look, motion-tracked arms, pickups, doors, story interactions, vaulting and climbing, menus in the room.

## Known Issues

- **Controller recenter is unreliable.** The L1 double-tap often doesn't register. Use **G** on the keyboard for now.
- **Night vision:** the night-vision light can still show partly in your own view. It's aimed through the camcorder screen, but each eye looks through the screen at a slightly different angle.
- **HUD dot:** the centre dot isn't centred in the headset.
- **Sprint:** the camera follows the running animation's forward motion one-to-one, so you feel the stride while sprinting.
- **Minor head-movement stutter** even standing still; inherited from the base injection layer, low priority.
- **Tested setups:** Steam version with Meta Quest (Quest Link and Virtual Desktop) only. GOG/Epic copies and SteamVR headsets are untested.

## Credits & Licenses

Insanity Engine VR is by T-Diamond (TdiamondOf). It is a fork of jrush64's outlast-vr-mod and is licensed under **GPL-3.0** (see `LICENSE`). The source code for each release is attached to it on the Releases page.

- [jrush64's outlast-vr-mod](https://github.com/jrush64/outlast-vr-mod) — the original mod this is forked from (GPL-3.0)
- [DXVK](https://github.com/doitsujin/dxvk) — Direct3D 9 to Vulkan, bundled as `dxvk_d3d9.dll` (zlib/libpng)
- [OpenXR Loader](https://github.com/KhronosGroup/OpenXR-SDK) by Khronos — bundled as `openxr_loader.dll` (Apache-2.0)
- [MinHook](https://github.com/TsudaKageyu/minhook) — API hooking, built into `d3d9.dll` (BSD-2-Clause)
- [Dear ImGui](https://github.com/ocornut/imgui) — the settings menu, built into `d3d9.dll` (MIT)

Full license notices for every bundled component are in `THIRD-PARTY-NOTICES.txt`.
