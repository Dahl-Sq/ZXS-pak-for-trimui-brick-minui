# ZXS.pak for TrimUI Brick console with MinUI firmware

## Playing ZX Spectrum games on you Brick

> ⚠️ This package was created and tested on MinUI-20250126-0 version and goes without any warranties.

Turn the console off, extract its TF card (with working **MinUI** installation) and insert it into you computer's cardreader. Please keep in mind that upper or lower case characters matter! All your files and folders names must be exactly the same as shown in this manual.

Unpack the archive and place folder `ZXS.pak` into `/Emus/tg5040` on the card. There must be three files: `default.cfg`, `fuse_libretro.so` and `launch.sh`.

Create folder `/Roms/ZX Spectrum (ZXS)`. You can use your own name instead of `ZX Spectrum`, but keep `(ZXS)` part in the end.

If you are using (undocumented) feature of **MinUI** to show covers and icons from `.res` hidden folders, then you can place the file `ZX Spectrum (ZXS).png` into `/Roms/.res`. (Rename it properly if you have chosen another name for ZX platform!) Oh, and if you can't understand this paragraph, then just ignore it.

Place some games into folder `/Roms/ZX Spectrum (ZXS)` and maybe their covers into `/Roms/ZX Spectrum (ZXS)/.res`. The emulator can work with `TAP`, `TZX`, `Z80` files and can pretend to be **ZX Spectrum 48K** or **ZX Spectrum 128K**. (Russian Spectrum models **Pentagon** and **Scorpion** are also available, but to use them you should place their ROM files on the card.)

Now safely extract the card from computer, place it back into you console and turn the console on. You'll see "ZX Spectrum" section in the main menu. Enter it and start one of your games.

First you should create some *common* settings for the whole **ZX Spectrum** platform. Press "Menu" button, go to "Options" and set everything in "Frontend" and "Emulator" submenus. My personal recommendations are:

- **Frontend**:
	- `Screen Scaling = Fullscreen`
	- `Screen Effect = none` (or set it to `Lines` if you like CRT picture)
	- `Screen Sharpness = Crisp`
- **Emulator**:
	- `Model = Spectrum 128K` (some old games do require 48K model to work, but it's easy to set "per game")
	- `Size Video Border = none`
	
Next, choose how console's controls should be mapped to Spectrum keyboard. My recommendation is to configure it as "Cursor Joystick" (the same as "Protek", the same as "AGF"). That is, configure `Joypad … mapping` options as follows:

- D-pad:
	- "Left" as 5
	- "Right" as 8
	- "Up" as 7
	- "Down" as 6
- Buttons:
	- "A" (East) as 0 (fire)
	- "B" (South) as 7 (useful for jumping)

Remember, you can always change those settings individually for any specific game anytime you want. Also remember, buttons "L" and "R" are already mapped to "Enter" and "Space" by default, and you can always access the virtual screeen keyboard by pressing "Select" button (then navigate it with D-pad and "A").

Now go to the "Save Changes" submenu and select "Save for console".

That's it! Use the screen keyboard to activate "Cursor" or "Protek" or "AGF" control in the running game, then use it to set additional game options (like difficulty level), then use it to start the game itself and play!

> If you don't like Cursor control, you can map Brick's D-pad and buttons as Sinclair Joystick (a.k.a. Sinclair Interface 2): 6/7 for Left/Right, 8/9 for Down/Up, 0 for Fire.

> You can also map "Start" button to the key that starts the playing for any specific game!

> If you for any reason want to totally reset *all* console settings to their factory defaults, just remove the file `/.userdata/ZXS-fuse/minarch.cfg`.

Some games can't be run on Spectrum 128K and require 48K model; some games can't be controlled by Cursor Joystick; some games require additional control keys and so on. In that case, open such game, press "Menu" button, go to "Options", set everything specific to the situation, then go to "Save Changes" but select "Save for game", not "Save for console". Then quit the game, start it again, and it will run with its personal settings.

> If you for any reason want to remove game-specific settings, just find the corresponding file in `/.userdata/ZXS-fuse` folder and remove it.

Have fun!
