# Lily58L

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/firstcontributions/first-contributions)
[![Discord](https://img.shields.io/discord/548530462419582996?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/frjFXZB "Redirect to Keycapsss Discord")
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg?style=flat-square)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

Lily58L is 6×4+4keys column-staggered split keyboard.

It is a modified version of the Lily58 Pro pcb from [kata0510](https://github.com/kata0510)
and has the the following additional features.
- one rotary encoder support on each side
- underglow with SK6812 Mini RGB led's (6 per side)
- per key RGB led with SK6812 Mini-E led (with legs, easy to solder)

**[Build-Guide](buildguide_en.md)**

**Hardware available at [keycapsss.com](https://keycapsss.com)**

![](img/Lily58L-pcb-1.png)
![](img/Lily58L-pcb-2.png)


# Parts

Part name | Quantity | Remarks | Photo |
| ------- | -------- | ------- | ----- |
| Lily58L PCB | 2 pcs ||
| Lily58L case | 1 set | 2 solid panels, 2 with holes for switches |
| [Pro Micro](https://keycapsss.com/keyboard-parts/parts/79/arduino-pro-micro-atmega32u4-controller), [Puchi-C](https://keycapsss.com/keyboard-parts/mcu-controller/141/puchi-c-pro-micro-replacement-with-usb-c-and-atmega32u4) or Elite-C | 2 pcs (a mix is possible) | Optionally, use [Mill-Max Single Row Socket Headers](https://keycapsss.com/keyboard-parts/parts/100/single-row-socket-headers-pins-mill-max-series-315), to make it hot-swappable. ||
| Key switch (MX) | 58 pcs |  ||
| [Kailh switch socket](https://keycapsss.com/keyboard-parts/parts/49/kailh-hot-swap-pcb-sockets-10-pcs) | 58 pcs |  ||
| Diodes 1N4148W (SMD) | 58 pcs |||
| TRRS jack | 2 pcs ||
| Tactile switch | 2 pcs | Reset switch ||
| TRRS cable | 1 cable | Must be a 4-pole cable ||
| Key caps | 58 pcs | 1.5U caps, can also be 1U ||
| Micro USB or USB-C cable | 1 pcs | Dependent what you use on the master half. ||


## Optionally:

Part name | Quantity | Remarks | Photo |
| ------- | -------- | ------- | ----- |
| [OLED module](https://keycapsss.com/keyboard-parts/parts/80/ssd1306-oled-lcd-display-0.91-inch-128x32-i2c-white) | 2 pcs | It is possible to use only one display ||
| SK6812 Mini | 12 pcs | RGB led's for underglow ||
| SK6812 Mini-E | 58 pcs |RGB led's for keycap backlight **(underglow led's must be soldered, because they are connected in series)** ||

## Firmware:
Clone/download the QMK firmware and execute the following in the [qmk_firmware](https://github.com/qmk/qmk_firmware) directory to write the default Lily58L keymap

    make lily58/light:lily58l:avrdude


When **`Detecting USB port, reset your controller now...`** is displayed, press the reset button on the keyboard to start writing.
Each half of the keyboard must be programmed separately using this approach.

If you're using DFU bootloader (in case of the elite c), replace the 'avrdude' with 'dfu'

## Schematic:

[![Lily58L schematic](img/Lily58L-schematic.png)](img/Lily58L-schematic.png?raw=true)