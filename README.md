[![OpenCore Version](https://img.shields.io/badge/OpenCore-0.8.3-green.svg)]


# Lenovo-Thinkpad-Helix-2-Hackintosh
[W.I.P} This repo contains EFI files required to get Monterey working on Second Genration of Lenovo Helix laptops


Model | Lenovo Helix 20CG001RTX
------------- | ---------------
CPU | Intel Core M-5Y71
GPU | Intel HD Graphics 5300
RAM | 8GB LPDDR3 1600Mhz
WiFi | Intel Dual Band Wireless-AC 7265
Software | macOS 12.4 Monterey

## What works?

-Graphic acceleration (But it performs worse than Windows) IDW Why

-Audio (only on Realtek USB)

-WiFi (doesn't obtain IP on some networks)

-Bluetooth

-USB 3

-Function keys (Sound, Brightness)

-Cameras

-Trackpad

## What doesn't?

-Sleep via the Power key or Close the lid

-Intel SST meaning the headphone jack also doesn't work

-Fingerprint

-Battery Level (Due it has dual battery)





## Graphical glitches in macOS

The workaround that work for me is using [one-key-hidpi](https://github.com/xzhih/one-key-hidpi). Download and run the code and select 'Enable HIDPI (with EDID)'. Then restart your computer and the glitches should be resolved.


## Touchscreen

For touchscreen models, I also added VoodooI2C to take advantage of the touchscreen display. However, it is disabled. If you want to use it, you have to activate all VoodooI2C-related kexts in the config! Since v3.0 there is a new touchpad kext that also uses VoodooInput. So you need to disable VoodooInput that comes with VoodooPS2 and enable VoodooInput that comes with VoodooI2C, otherwise the system will not boot.

