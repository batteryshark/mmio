# MMIO - Mario Multiverse IO

This is a plugin for optimized gamepad support on Mario Multiverse.

## Changelog
20220124_0:
	-> Fixed issue with XInput Analog Flipping Out
	
	-> Fixed bug where Analog deadzone settings were not respected by DInput.

20220123_0:
	-> Added option to allow/ignore background input.
	
	-> Added auto generation of mmio_config.json if it doesn't exist.
	

20220122_1:
	-> Massive refactor of input loops (should be even more responsive)
	
	-> Added configuration file (mmio_config.json)
	
	-> Added customizable analog deadzone setting.
	
	-> Added setting to choose XInput (1) or DirectInput (2) or Auto (0)
	
	
v4:
	-> Initial Test 

## To Use:
1. Backup your fmodex.dll (copy it)
2. Copy mmio.dll and fmodex.dll to your Mario Multiverse folder from the release.
3. In MarioConfig.exe, set "Use Joypad if connected" to "false", if set to true, mmio will operate in bypass mode and the game will use the original DirectInput handler.

## To Remove:
1. Delete mmio.dll and the fmodex.dll.
2. Rename your original backed up fmodex.dll back to "fmodex.dll"


## ** Notes **

- An included mmio_config.json file allows you to force DInput even when XInput is supported. It also lets you set your own analog deadzone.


- When the game updates, the hash of fmodex.dll will no longer match, so Neo's updater will replace it. Copy the fmodex.dll from the release again to continue use.

- Neo's updated input will eventually replace this.

- If your controller supports XInput, mmio will operate in XInput Mode:
	-> More efficient input processing.
	
	-> Support for additional shortcuts item+Left item+Right PageDown/PageUp, Item+Y (Screen toggle), Item+A (Skip)
	
	-> Supports Analog/Digital at the same time
	
	
- If your controller does not support XInput, mmio will operate in its own DirectInput Mode:
	-> More efficient input processing.
	-> Reads button mapping from MarioConfig
	-> Supports Analog/Digital at the same time

Please let me know your feedback - any improvements on mmio I will also foward to Neo when the new input system is built.
