# RUDE: Romero's Ultimate Doom Engine

 RUDE is a fork of Chocolate Doom 3.1.0 with some stuff from Crispy Doom.
 The name is some kind of play on words and stands for Romero's Ultimate Doom Engine and
it's another tribute to John Romero. Easy to understand if you know my Romero's Heresy II
project for Heretic. :)

 It's a strong limit removing port aiming to fix game breaking bugs and prevent crashes while
remaining faithful to the original executables. There are a few new gameplay features too.
 It's somewhere in the middle between Chocolate Doom and Crispy.

 Please refer to the Chocolate Doom documentation.
 Also contains code from MBF and PrBoom+.
 Of course DOOM © 1996 id Software.
 Chocolate Doom © 2024 Simon Howard and Crispy Doom © 2024 Fabian Greffrath.

# New features:

 * Widescreen support both zoomed view and real wide (bits from Russian Doom and Crispy).
 * UI centering for widescreen (mostly taken from Crispy).
 * Support for Unity IWADs with widescreen assets (SmileTheory).
 * Enable loading 16 bit RIFF wavs in .wads (SmileTheory).
 * Doom 1.0 and 1.1 emulation (SmileTheory).
 * Draw the player mugshot with max view.
 * Supports SIGIL and SIGIL II (even multiplayer), E1M4b and E1M8b (Crispy).
 * Extended setup to support SIGIL, SIGIL II and new features. Can warp to title.
 * There's a new 'Unholy massacre' skill level (-skill 6). :D Double monsters, lesser health pickups,
 zombiemen got a point blank attack, pistol with increased accuracy and damage, bumped minimum damage
 dealt for punch and you can eat gore when very low on health.
 * Replaced the Unholy Massacre title graphic. Thanks Julia Nechaevskaya!
 * Remove SPECHIT limit (Crispy).
 * Entirely remove INTERCEPTS limit (fixes all-ghosts bug).
 * Heretic: entirely remove INTERCEPTS and SPECHIT limits (Crispy).
 * Got rid of supersized PNGs (Crispy).
 * Fixed backpacks from Marshmallow (idea and bits of code):
 * Players now can exchange supplies (default backpack key is 'x', default stimpack key is 'c').
 * Players drop backpacks with their inventory upon death, you can't drop another one until the
 previous one has been picked up tough. They work even in SP.
 * Players can only pick up their own backpacks in coop.
 * Single player respawn.
 * Keep keys and no DM items in Coop options (Marshmallow).
 * Spawn double the monsters and take double damage options.
 * Classic mode with only Doom 1 monsters for slaughterfest maps and lame players, regular shotgun
 takes precedence. Now Wolf SS is not replaced.
 * Slow ISA VGA simulation (Trident 9000i).
 * New command line parameters for the above: backpack, nodmweapons, keepkeys, sprespawn, 2xmonsters,
 xpain, nod2monsters, isa, halfammo.
 * Extended demo format while keeping vanilla compatibility.
 * Doom 1.2 demo support (SmileTheory).
 * Alternative fix for the demo desync accessing menus bug: disable some menus while recording demos
 instead of pausing the game at record and playback time.
 * Drag and Drop support (Crispy).
 * Resurrect cheat with IDDQD (Crispy, works differently here).
 * Support for extended nodes (Crispy).
 * Autorun key (Crispy).
 * The startup console is back and with colored title, works from the Windows command line
 (thanks Julia Nechaevskaya for hint on colors).
 * Fake splitscreen.
 * Added LCD gamma fix from Russian Doom using a custom darker palette by Julia Nechaevskaya.
 * New 'One thousand deaths await thee' skill level for Heretic. You take double damage, monsters
 got half hit points and half ammo for a more dynamic gameplay.
 * Removed limits for Heretic (Crispy).
 * Fixed boss level ending not triggered if every player is dead in multiplayer.
 * Fixed Doom II monster exclusion bug.
 * Fixed configuration not being saved for Heretic.
 * Support for Ogg, FLAC and MP3 music lumps (Crispy).
 * Don't load Boom maps by default, only with the -boom parameter.
 * Fixed crash with invalid blockmap (DWHEEL.WAD).
 * Add FPS counter (AlexMax).
 * Display tally screen after ExM8 (Crispy).
 * Allow skipping the Doom finales.
 * Add the -noumskill parameter to prevent showing UM in the menu.
 * Many bugfixes from Crispy.

 Have fun!

# Compiling on Windows

 Dowload codeblocks-17.12mingw-setup.exe (to compile the 32 bit version), CMake 3.29, TortoiseGit and
Git 64 bit versions.
 In System advanced configuration add the MinGW binaries folder to the Path environment variable
(here C:\DEV\CodeBlocks\MinGW\bin).
 Select CodeBlocks - MinGW Makefiles in Cmake-GUI.
 Download libraries to setup CMake-GUI: SDL2-devel-2.30.12-mingw.zip, SDL2_mixer-devel-2.8.1-mingw.zip,
SDL2_net-devel-2.2.0-mingw.zip, libsamplerate-0.2.2-win32.zip, lpng1647.zip and
fluidsynth-2.3.7-winXP-x86.zip.
 Compile yourself libsamplerate, lpng and zlib.
 Get the missing dlls from: SDL2-2.30.12-win32-x86.zip, SDL2_mixer-2.8.1-win32-x86.zip,
SDL2_net-2.2.0-win32-x86.zip and crispy-doom-5.12.0-win32.zip.

# Chocolate Doom

Chocolate Doom aims to accurately reproduce the original DOS version of
Doom and other games based on the Doom engine in a form that can be
run on modern computers.

Originally, Chocolate Doom was only a Doom source port. The project
now includes ports of Heretic and Hexen, and Strife.

Chocolate Doom’s aims are:

 * To always be 100% Free and Open Source software.
 * Portability to as many different operating systems as possible.
 * Accurate reproduction of the original DOS versions of the games,
   including bugs.
 * Compatibility with the DOS demo, configuration and savegame files.
 * To provide an accurate retro “feel” (display and input should
   behave the same).

More information about the philosophy and design behind Chocolate Doom
can be found in the PHILOSOPHY file distributed with the source code.

## Setting up gameplay

For instructions on how to set up Chocolate Doom for play, see the
INSTALL file.

## Configuration File

Chocolate Doom is compatible with the DOS Doom configuration file
(normally named `default.cfg`). Existing configuration files for DOS
Doom should therefore simply work out of the box. However, Chocolate
Doom also provides some extra settings. These are stored in a
separate file named `chocolate-doom.cfg`.

The configuration can be edited using the chocolate-setup tool.

## Command line options

Chocolate Doom supports a number of command line parameters, including
some extras that were not originally suported by the DOS versions. For
binary distributions, see the CMDLINE file included with your
download; more information is also available on the Chocolate Doom
website.

## Playing TCs

With Vanilla Doom there is no way to include sprites in PWAD files.
Chocolate Doom’s ‘-file’ command line option behaves exactly the same
as Vanilla Doom, and trying to play TCs by adding the WAD files using
‘-file’ will not work.

Many Total Conversions (TCs) are distributed as a PWAD file which must
be merged into the main IWAD. Typically a copy of DEUSF.EXE is
included which performs this merge. Chocolate Doom includes a new
option, ‘-merge’, which will simulate this merge. Essentially, the
WAD directory is merged in memory, removing the need to modify the
IWAD on disk.

To play TCs using Chocolate Doom, run like this:

```
chocolate-doom -merge thetc.wad
```

Here are some examples:

```
chocolate-doom -merge batman.wad -deh batman.deh vbatman.deh  (Batman Doom)
chocolate-doom -merge aoddoom1.wad -deh aoddoom1.deh  (Army of Darkness Doom)
```

## Other information

 * Chocolate Doom includes a number of different options for music
   playback. See the README.Music file for more details.

 * More information, including information about how to play various
   classic TCs, is available on the Chocolate Doom website:

     https://www.chocolate-doom.org/

   You are encouraged to sign up and contribute any useful information
   you may have regarding the port!

 * Chocolate Doom is not perfect. Although it aims to accurately
   emulate and reproduce the DOS executables, some behavior can be very
   difficult to reproduce. Because of the nature of the project, you
   may also encounter Vanilla Doom bugs; these are intentionally
   present; see the NOT-BUGS file for more information.

   New bug reports can be submitted to the issue tracker on Github:

     https://github.com/chocolate-doom/chocolate-doom/issues

 * Source code patches are welcome, but please follow the style
   guidelines - see the file named HACKING included with the source
   distribution.

 * Chocolate Doom is distributed under the GNU GPL. See the COPYING
   file for more information.

 * Please send any feedback, questions or suggestions to
   chocolate-doom-dev-list@chocolate-doom.org. Thanks!
