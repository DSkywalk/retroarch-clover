=== Caprice32 core for RetroArch ===
 
 This module will add support for Amstrad CPC games to RetroArch
 
 Available executables and arguments:
 - /bin/cpc <rom> <clover_args>
 -  runs "cap32" core

 Caprice 32 usage (written by D_Skywalk): 
    launch an TAPE (cdt) or DSK, and game should autostart. Check Instructions Below!

 Core options:
  Autorun - disabled/enabled. If enabled, the core will run the first bas/bin found in DSK
  Resolution - Internal resolution; 384x272|800x600. 800x600 have a better KeyboardOnScreen.
  Pad X CFG - Configure pad; cursors|joystick|qaop|sxkl. See below.

 Controls:
	- JoyConfig "cursors": [STR] K, [A] ENTER, [B] F1,   [X] N, [Y] Y, DIR CURSORS.
	- JoyConfig "joystick":[STR] J, [A] FIRE1, [B] FIRE2,[X] N, [Y] Y, DIR JOYDIR.
	- JoyConfig "qaop":    [STR] R, [A] SPACE, [B] 1,    [X] 3, [Y] 2, DIR QAOP.
	- JoyConfig "sxkl":    [STR] QR,[A] UP,    [B] Z,    [X] N, [Y] SPACE, DIR SXKL.

	- JoyConfig common: [L2] CTRL, [R2] COPY, [L] ENTER, [R] SHIFT, [SEL] ** ALT MODE - KEEP PRESSED **.
    - Alternative mode: [STR] ** KeyboardOnScreen **, [UP] # RUN"DISC, [DW] # RUN"DISK,[LF] # CAT, [RG] # |CPM
	
 To start a game without autorun:
	Caprice32 emulates a real CPC, which means that to run a game you have to do the same thing as you would with a real CPC.

	To play a game, you must insert a disk image and type two basic commands:

		- You have to know what files the disc image has. It's easy, just press [SELECT] and [DPAD-LEFT]. This will then type CAT on screen.
		- You'll see a list of files. The important filetypes are BIN, BAS or ones without the extension, ex: ABADIA.BAS, GRYZOR.BIN, TETRIS.
		- With JoyConfig-cursors, use [R] and [R2] to copy the game's filename.
		- To run the game, place the cursor at the beginning of the name, press [L2]+[DPAD-LEFT] buttons and press [L] while holding them. This will put RUN" in front of the file name and launch the game.
		- For some games, you don't have to type the  RUN" command, they load with the |CPM command. Those are easily detectable. If you get an error when you executing the CAT command (Ignore, Cancel), these games are protected. Don't worry about it, they are even easier to execute, just press [SELECT] and [DPAD-RIGHT].

 Credits:
 Core by libretro
 Module rewriten and built by D_Skywalk, tested by 1lokolo1/nesito
 Hakchi module system by madmonkey
 NES Mini shell integration by Cluster
 (c) 2016-2017

