# I-Hate-This-Place-VR-Mod
VR Mod for I Hate This Place

I HATE THIS PLACE VR  -  VR mod for "I Hate This Place" (Unity 6000.0, IL2CPP, URP)
=================================================================================

Version 0.1.20 (test build on Quest 3 VDXR).

WHAT IT DOES
------------
* Stereo VR through OpenXR (SteamVR, Meta/Oculus, Virtual Desktop, WMR...).
* Two views - the right stick click (R3) switches between them:
    FIRST PERSON  you are the character: the view sits at its head, the left stick walks where you look,
                  the right stick turns (snap turn), your right hand aims.
    NORMAL        you stand where the game's own camera is and look down on the scene, like the flat game.
                  The right stick is a normal gamepad right stick here (aim / throw distance).
* The character aims where your right controller points (while a trigger is held).
* The VR controllers act as a gamepad for the game's own controls and menus.
* The HUD (time, HP / ST / FD bars, held weapon, quick items) floats by your left controller;
  menus are on a screen floating in front of you.

INSTALL
-------
1. BepInEx 6 (be.788) is already in the game folder.
2. Copy the BepInEx folder from this zip into the game folder (merge / overwrite).
3. Start SteamVR (or your OpenXR runtime), then start the game.

CONTROLS
--------
Left stick ......... walk                     Right stick left/right .. turn (first person)

Right stick up ..... d-pad right              Right stick down ........ d-pad left   (first person)

Normal view: the right stick is the gamepad's right stick (no turning / d-pad from it).

Right stick click .. switch first person / normal view

Right trigger ...... RT (shoot - the character aims where your right hand points)

Left trigger ....... RB (throw) - while held: aim with your right hand, right stick up / down = further / closer

Right grip ......... ready / aim the gun where your right hand points + red laser (while held)

Left stick click ... run (until you stop walking or click again)

Left grip .......... LB                       Hold LB + left stick click .. flashlight on / off

A .................. A                        Hold Y .................. Y

B .................. B (sneak)               Tap Y ................... d-pad up

X (tap) ............ X                        Hold X .................. Back / View

X + Y together ..... Start (pause)

Both stick clicks .. re-centre

In the inventory / map / crafting the sticks and buttons work like on a gamepad (left stick = move the selection).
On the title and pause screens you can also point the right hand at the screen and pull the trigger to click.

First person: the weapon goes into your right hand (fine-tune with [Aiming] WeaponPositionOffset /
WeaponRotationOffset) and the flashlight shines from your left hand.

MELEE (bat...): swing your right controller so the bat actually hits the enemy - the attack happens on contact and
the character turns to what you hit (the right trigger still attacks too).

[Aiming] MeleeSwingMode = Collision (default)
or Swing (any fast swing attacks); MeleeHitSpeed = how fast the swing must be for a touch to count (default 1.0).

Everything is in BepInEx\config\ihatethisplace.vr.cfg ([Controls] = gamepad buttons).

WEAPON ADJUST (each weapon its own place in your hand): first person, weapon in hand - hold B + click the right stick
for 1.5 s (or "Adjust weapon in hand" in the settings menu). Hold the LEFT GRIP to grab the weapon with your left hand,
move / turn it, let go. B = undo, A = save for this weapon (saved in [Weapon - <name>] in the config).
CHEATS: settings menu "Unlimited ammo", "Unlimited HP", "Unlimited stamina", "Unlimited food" (or [Cheats] in the config).
The weapon / ammo panel floats to the right of your right hand ([UI] AmmoOnRightHand / AmmoOnRightHandOffset).

IN-GAME SETTINGS MENU:  hold Y + left stick click for 1.7 s (view, zoom of the normal view, aiming, screen).
HAND ADJUST:            hold Y + right stick click for 1.5 s.

IF THE TWO EYES LOOK DIFFERENT: open the in-game settings menu, "Render effects" - switch the game's effects off
one at a time to find the one that causes it (saved in [Camera] DisabledRenderFeatures). Please tell me which one.

USEFUL SETTINGS ([View])
------------------------
ViewMode = FirstPerson / Normal (start view).

NormalViewZoom = 1 (the game's camera spot); smaller, e.g. 0.6, brings the normal view closer to the player.

NormalViewHeightOffset = metres up / down for the normal view.


Uses Astien's OpenXR bridge (see BepInEx\plugins\IHVR\LICENSES). Free, non-commercial.
