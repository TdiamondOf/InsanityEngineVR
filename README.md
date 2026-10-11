# InsanityEngineVR
A 6DOF VR mod for Outlast (2013) with motion controls and interactability.
# Insanity Engine VR

A 6DOF VR mod for **Outlast (2013)** with real motion controls.

Play Outlast in virtual reality with full head tracking, room-scale 6DOF movement, and — the part that makes this different — **motion-controlled hands.** Grab the camcorder off your hip, raise it to your face, and actually *hold* it up like it's real. The thing that makes Outlast terrifying becomes something you do with your own hands.

Insanity Engine VR

A 6DOF VR mod for Outlast (2013) with motion controls.

Play Outlast in virtual reality with full head tracking, room-scale 6DOF movement, and motion controls. Hold the camcorder in your hand and aim it where you want, independent of where you’re looking. The thing that makes Outlast terrifying becomes something you do with your own hands.

Features
True 6DOF head tracking: lean, duck, and peek around corners with your body
Hand-held camcorder: hold grip to hold and aim the camcorder with your hand instead of your head
Sharp UI: menus and HUD render on their own full-resolution floating panel, so text is crisp and readable
Snap and smooth turning: switchable in-game
In-game settings menu: tune FOV, scale, render resolution, UI distance and size, and more, live, without restarting
Clean spectator view: a normal single image on your monitor for anyone watching or recording
Requirements
Outlast (2013), Steam version. The mod only works with the Steam build. GOG, Epic, and the 32-bit version aren’t supported.
A PC VR headset with an OpenXR runtime set as the active runtime. Any of these work:
SteamVR: SteamVR Settings → OpenXR → “Set SteamVR as OpenXR runtime”
Meta Quest Link: Meta Quest PC app → Settings → General → set as active OpenXR runtime
Virtual Desktop: uses its own runtime (VDXR), no extra setup needed
Microsoft Visual C++ 2015–2022 x64 Redistributable. Most gaming PCs already have it. If the game runs flat with no VR, install this first.

Note: This mod uses d3d9.dll, so it can’t be installed alongside other mods that use the same file (ReShade, DXVK, dgVoodoo).

Installation
Download the latest Insanity Engine VR zip and unzip it.
Open your Outlast folder. In Steam: right-click Outlast → Manage → Browse local files.
Go into Binaries\Win64, the folder that contains OLGame.exe. Not the main Outlast folder.
Copy all the unzipped files into Binaries\Win64.
Run Outlast-VR.bat once. It sets up your game settings for VR (field of view, motion blur off, frame cap removed, mouse-look disabled) and backs up your original settings first.
Start your headset and VR runtime first, then launch Outlast from Steam normally. The mod loads automatically.

If the headset or VR runtime isn’t running when the game starts, the game runs flat. Close it, start your VR runtime, and launch again.

Updating

If Windows asks to replace files:

d3d9.dll: Yes
openxr_loader.dll: Yes
outlastvr.ini: No, so you keep your settings
Uninstalling

Delete the mod files from Binaries\Win64, or use Steam’s Verify integrity of game files to restore the original game.

Settings

Press F10 in-game, or click the arrow in the corner, to open the Insanity Engine VR menu on your monitor. Every change saves automatically. Use Reset to Defaults if anything gets weird.

Status

Actively in development. Head tracking, the hand-held camcorder, turning, and the sharp UI are working.

Coming next:

Motion-tracked hands and arms
Physical holsters: reach to your hip, grab the camcorder, raise it to your face
Night vision visible only through the camcorder’s screen
Grabbable doors
Credits

This mod is built on the excellent Outlast VR mod by jrush64. Insanity Engine VR extends that foundation with motion controls and other features. Huge thanks to jrush64. None of this exists without their work.

Also uses:

MinHook (BSD-2-Clause)
Dear ImGui (MIT)
OpenXR Loader by Khronos (Apache-2.0)

See THIRD-PARTY-NOTICES.txt for full license notices.

License

Released under GPL-3.0, the same license as the base mod. The full source code for every release is available in this repository. You’re free to use, modify, and redistribute it, but any version you release must also be open source under GPL-3.0 and keep this license and credit intact.
