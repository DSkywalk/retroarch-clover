# RetroArch module for hakchi

This is a hakchi/hakchi2 module which adds libretro cores and RetroArch front-end to your NES Mini.

It will automatically detect unsupported NES games and run them instead of the default emulator. Save states will work as usual.

It can also run games for other consoles. This pack already contains my following cores:
- caprice32 (Amstrad CPC) - changes at: https://github.com/DSkywalk/libretro-cap32
- fuse (ZX Spectrum)
- mame2003_mini (various arcades machines)
- pcsx_rearmed (Sony PlayStation)

## How to use this

1. Go to "releases" tab and download the newest release.zip 
2. Unpack release.zip anywhere you want
3. Copy retroarch.hmod and the cores you want (.hmod files from cores and extra_cores folders) to user_mods directory of Hakchi2.
4. Install the modules (all modules can be installed in one go) via Hakchi2's Modules menu.
5. Add the games as usual

Please note:
- To add RetroArch shortcut to NES Mini's shell, drag-and-drop CloverApp.zip to Hakchi2
- To make your own RetroArch modules, use the structure from libretro_core_template.zip. Use exisiting modules as a reference.
- To add your own BIOS images for custom cores, use bios_template.zip (please read the readme.txt inside).
- If the file extension of your game is not supported by Hakchi2, you may need to change the path in command line arguments (in Hakchi2's game options) to make it point to the corresponding core.
- To load arcade games that come in the form of ZIP archives, you'll need to change /bin/zip in game's command line arguments to /bin/fba, /bin/mame2000, /bin/mame2003 or /bin/cps2 depending on the core needed for the game to run (look at "Additional Information" section for all avaiable /bin/<> commands). For some cores like Final Burn Alpha, BIOS image (e.g. neogeo.zip for Neo-Geo) must be in the game directory.
- You can re-enable bilinear filtering in RetroArch's settings (Settings —> Video —> Bilinear Filtering)
- If you want to use RetroArch's XMB UI instead of RGUI, install xmb_assets.hmod and change Menu Driver in Settings —> Driver —> Menu Driver to "xmb"

## Additional information

Executables and arguments for all available cores:
        - /bin/cpc <rom> <clover_args>
          runs "caprice32" core
        - /bin/zx <rom> <clover_args>
          runs "fuse" core
        - /bin/mame2003_mini <rom> <clover_args>
          runs "mame2003 minimized" core
        - /bin/pcsx <rom> <clover_args>
          runs "pcsx_rearmed" core

## Known issues

- Default CRT filter is not working, scanlines shader added instead but it's not working with all systems.
- It's recommended to turn your NES Mini off from shell, not during the game

## Credits
Repo Cores by D_Skywalk

NES Mini port by madmonkey

NES Mini shell integration by Cluster

Various additions, tweaks and fixes by pcm720

RetroArch/libretro project: https://www.libretro.com
