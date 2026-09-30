============================================================================================
FM ACTIONLINK - KITS 3D
============================================================================================

Shows Football Manager 26 kits in 3D, inside the game itself.

WHAT IT DOES
------------

- On the club screen, in the "About the Club" card, replaces the 3 2D shirts (home, away and
  third) with 3D shirts that gently sway (or turn all the way round, or only the button is
  added: see the settings below).
- A button in the corner of the card's title opens the full player in 3D: shirt, shorts,
  socks and boots, with tabs for outfield and goalkeeper kits. It turns by itself, turns by
  hand when you drag it, and closes with the X, Esc or a click outside the window.
- When the kit comes from the game's own official kits, a gold "Official" badge appears.
- Texts follow the game's language (all 18 FM26 languages).

Everything is drawn by FM itself, with the game's own player model. No extra program needed.

WHERE THE KITS COME FROM
------------------------

1. Your 3D kits folder (Documents\Sports Interactive\Football Manager 26\graphics\kits),
   following the config.xml files, like the game. How the folders are organised does not matter.
2. If the club has no kit in your folder, the official kits that ship with the game.

If the club has no 3D kit in either, its 2D shirt stays as it is.

Kits installed with the game open (by hand, by an app or by another plugin) show up by
themselves within a few seconds, without restarting the game.

PLAYER'S FACE (OPTIONAL)
------------------------

If you use the HeadHunter plugin (real heads in Documents\Sports Interactive\Football
Manager 26\heads), the full player gets the face, hair and eyes of one of the club's players,
and the arms and legs take his skin tone:

1. The first team's captain, if you have his head.
2. If not, the first player of the squad list whose head you have.
3. If nobody in the squad has one, the grey player stays.

No heads ship with this extension: it only uses the ones you already have installed.

INSTALL
-------

1. Have BepInEx 6 for IL2CPP (build be.755 or newer) in FM26. If you already use other plugins
   in the game, you have it.
2. Copy the FMActionLink.Kits folder (inside the zip's plugins folder) into your game's
   BepInEx\plugins:
   - Steam: ...\steamapps\common\Football Manager 26\BepInEx\plugins
   - Epic: ...\Epic Games\<FM26 folder>\BepInEx\plugins
   - Xbox / Game Pass: ...\XboxGames\Football Manager 26\Content\BepInEx\plugins
3. Start the game. About 5 seconds after the menu, the extension is ready.
4. Open any club's screen.

It does not need the base FM ActionLink plugin, nor the game's ID option.

HOW TO CHANGE THE SETTINGS (.CFG FILE)
--------------------------------------

The settings live in FMActionLink.Kits.look.cfg, inside the extension's folder:

    BepInEx\plugins\FMActionLink.Kits\FMActionLink.Kits.look.cfg

It is created by itself the first time the game starts with the extension.

Step by step:

1. Open the file with Notepad (right click > Open with > Notepad).
2. Each line is one setting written as  name = number . Change only the number after the "=".
   Whatever comes after "#" is just an explanation and can stay as it is.
3. Save the file (Ctrl+S). If the game is open, the change shows in about a second, with no
   need to restart anything.

Watch out:
- Use a DOT for decimals: 0.9 (not 0,9). With a comma the line is ignored and the default
  value is used.
- If the file gets messed up, just delete it: the next time the game starts it is created
  again with the default values.

The settings:

  Shirts in the "About the Club" card
  cardKits3D          1      1 = 3D shirts in the card. 0 = the game's 2D shirts stay, and
                             only the button that opens the full player in 3D is added.
  cardSpin            0      0 = gentle sway. 1 = full 360 degree turn.
  cardSpinSeconds     10     Seconds each full turn takes (with cardSpin = 1).

  Light
  lightIntensity      1.1    Strength of the light.
  lightHeight         25     Height of the light, in degrees above the horizon.
  lightDirection      160    Side the light comes from, in degrees around the player
                             (180 = from the viewer's side).
  fillIntensity       0      Second light, from the other side (0 = off).
  fillDirection       340    Side the second light comes from, in degrees.
  fillHeight          10     Height of the second light, in degrees.

  Colours
  kitBrightness       0.9    Colour brightness of the game's official kits (below 1 =
                             darker, above 1 = lighter).
  userKitBrightness   0.75   The same for kits from your folder, which tend to come out
                             lighter than the official ones.
  kitShine            0.05   Fabric shine: 0 = matt, 1 = glossy.
  mannequinBrightness 1      Tone of the grey player.

The middle number is the default value.

CURRENT LIMITS
--------------

- The game's own official goalkeeper kits do not show yet (those in your folder do).
- Women's teams have not been tested yet.
- Clicking a shirt does not open the full player yet: use the button in the title.

TROUBLESHOOTING
---------------

Everything the extension does is written to BepInEx\LogOutput.log, on lines starting with
[Kits]. If something does not show up, send that part to whoever maintains the extension.

LICENCES
--------

The Inter font (fonts folder) is distributed under the SIL Open Font License
(fonts\OFL-Inter.txt). The player model, the official kits and the FM emblem are read from
each person's own game installation: none of them is inside this package.
