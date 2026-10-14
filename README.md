# evolution_ota

Over-the-air update information for denson9874's unofficial Evolution X builds for the
Pixel 11 series: kodiak (Pixel 11 Pro XL), grizzly (Pixel 11 Pro), cubs (Pixel 11) and
yogi (Pixel 11 Pro Fold).

The device trees ([kodiak](https://github.com/denson9874/device_google_kodiak) and its
siblings) ship a runtime overlay that points Evolution X's Updater here instead of
[Evolution-X/OTA](https://github.com/Evolution-X/OTA), which only lists official devices.
The overlay is deleted if a device becomes official.

- `builds/<device>.json`: the latest build, in the Updater's format. The download is the
  signed A/B OTA package on [SourceForge](https://sourceforge.net/projects/denson9874-s-user-builds/files/).
- `changelogs/<device>.txt`: what changed in that build.

The release routine updates both after the OTA package has been uploaded. The Updater only
installs packages signed with the builds' own release key.

First installs still need a computer: unlock the bootloader and flash the fastboot zip as
described in the XDA thread. After that, updates arrive over the air.
