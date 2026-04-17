SELA (Superelliptical Lissajous Aim)
---------------------------------------------
OVERVIEW
---------------------------------------------

This is a Send Input demo of a controller aiming system that combines:

- Gyro input → gross aim
- Displacement-based thumbstick → fine aim

These two systems are designed to be used together.

This is NOT velocity-based stick aim.
This behaves closer to MNK.


---------------------------------------------
CORE MECHANIC: GYRO RATCHETING
---------------------------------------------

This system uses "ratcheting", which replicates lifting a mouse.

- Hold SQUARE → Gyro OFF
- Release SQUARE → Gyro ON


---------------------------------------------
CONTROLS / BINDS
---------------------------------------------

--- MOUSE ---
R1              → Left Click (Mouse1)
L1              → Right Click (Mouse2)

--- TRIGGERS ---
R2              → F
L2              → Space

--- FACE BUTTONS ---
Triangle        → Q
Circle          → X
Cross           → Z
Square          → Disable Gyro (Hold)

--- MOVEMENT (LEFT STICK) ---
Left Stick Up   → W
Left Stick Down → S
Left Stick Left → A
Left Stick Right→ D

--- DPAD ---
Dpad Up         → Left Shift
Dpad Down       → V
Dpad Left       → E
Dpad Right      → R

--- STICKS ---
L3              → Left Ctrl
R3              → C

--- SYSTEM ---
Options         → Escape
Share           → Tab

--- TOUCHPAD ---
Left Tap        → [
Right Tap       → ]

--- AIMING ---
Gyro            → Gross aim
Right Stick     → Fine aim (displacement-based)


---------------------------------------------
SUPPORTED CONTROLLERS
---------------------------------------------

Confirmed:
- DualSense (DS5 via USB)

Likely:
- DualShock 4 (DS4)

Untested:
- Switch Pro Controller
- Alpakka / custom devices
- Other controllers


---------------------------------------------
READ THIS
---------------------------------------------

This demo uses Windows SendInput for mouse and keyboard output.

DO NOT USE THIS IN GAMES WITH ANTI-CHEAT.

- This may be flagged or blocked
- Not intended for multiplayer anti-cheat environments

Use this in:
- offline
- single-player
- unrestricted environments

---------------------------------------------
MULTIPLAYER / FULL VERSION
---------------------------------------------

For safe multiplayer usage:

- A hardware-based solution (Teensy USB) is required
- This runs as a native input device instead of using SendInput
- The full version is designed to run with a Teensy setup

The full version also feels more stable and smooth overall due to a more consistent input pipeline.

This demo is intended to get a feel for the aiming method.


---------------------------------------------
SETUP
---------------------------------------------

Required files:

- GyroThumbUI.exe
- JoyShockLibrary.dll

Steps:

1. Plug in controller via USB
2. Place both files in the same folder
3. Run GyroThumbUI.exe
4. Click Start

Do NOT touch the controller during calibration. Doing so will cause cursor drift.
If this happens, press Alt + F4 to close the app and reopen it.



---------------------------------------------
TROUBLESHOOTING
---------------------------------------------

JoyShockLibrary.dll missing:
→ Place it in the same folder as the exe

MSVCP140.dll (or similar) missing:
→ Install Microsoft Visual C++ Redistributable (x64)

App does not launch:
→ Missing runtime or DLL

Controller not detected:
→ Plug in controller via USB
→ Close DS4Windows / Steam Input / reWASD

Gyro not moving:
→ Square is being held (gyro disabled)

Input feels off:
→ This system has a learning curve

For old FPS ports, disable joystick input completely before testing.
If aim feels wrong, assume the game is mixing joystick and mouse.
Checklist:
1. Disable Steam Input for that game.
2. Turn off in-game joystick/controller support.
3. Hide the controller from the game with HidHide if needed.
4. Close remappers that expose a virtual gamepad unless required.
5. Re-launch the game and confirm it no longer detects a joystick/controller.



---------------------------------------------
MODDING / DESIGN POTENTIAL
---------------------------------------------

This control scheme is not limited to standard FPS aiming.

Because the right stick is displacement-based and can act as an independent reticle,
it can be used for:

- Mexican standoff style dual wielding (ex: pistol 1 = main camera, pistol 2 = independent reticle)
- Manual reloading, similar to Pavlov VR
- Independent aiming for grenades and melee attacks
- Utility selection (ex: lower quad nods)
- Weapon manipulation (ex: adding/removing scopes, muzzles, etc.)

This opens up design space similar to VR-style interaction in a flatscreen environment.

The documents in the "Mod Ideas" folder go over these concepts in more detail.

---------------------------------------------
SUMMARY / NOTES
---------------------------------------------

Gyro = gross aim  
Right stick = fine aim  
Square = ratchet (lift/reset)

- Displacement-based thumbstick aim
- No aim assist
- Not flick stick
- Not velocity-based

Early demo focused on the core aiming method.
