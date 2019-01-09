---
layout: single
title: Setting up your SD card
---

### What you will need

- The latest release of [Atmosphère](https://github.com/Atmosphere-NX/Atmosphere/releases/latest). For this step, you will need the zip file and `fusee-primary.bin`.
- The latest release of [Hekate](https://github.com/ctcaer/hekate/releases/latest){: target="_blank"}
- The latest release of the [homebrew launcher](https://github.com/switchbrew/nx-hbmenu/releases/latest){: target="_blank"}.
- The latest release of [Checkpoint](https://github.com/FlagBrew/Checkpoint/releases/latest){: target="_blank"}. Download the `.nro` file.
- The latest release of [hb-appstore](https://github.com/vgmoose/hb-appstore/releases/latest){: target="_blank"}.
- [sys-ftpd.kip](https://noirscape.github.io/SwitchGuide/assets/sys-ftpd.kip) ([source](https://github.com/jakibaki/sys-ftpd){: target="_blank"})
- [hekate_ipl.ini](https://noirscape.github.io/SwitchGuide/assets/hekate_ipl.zip){: download=""}.
- The latest release of [nx-hbloader](https://github.com/switchbrew/nx-hbloader/releases/latest)

### Setting up your sd card

1. Turn off your Switch and put your microSD card in your computer.
2. Copy the `bootloader` folder from the Hekate zip to your SD card.
3. Copy the `atmosphere` folder from the Atmosphère zip to your SD card.
4. Copy `fusee-primary.bin` to the to the `atmosphere` folder.
5. Copy `hbmenu.nro`from the `nx-hbmenu` release  to the root of your SD card.
6. Make a folder called `switch` on the root of your SD card.
7. Copy `checkpoint.nro` from the `Checkpoint` release to the `switch` folder.
8. Extract the `hb-appstore` zip and copy `appstore.nro` to the `switch` folder.
9. Copy `hbl.nsp` from the `nx-hbloader` release to the `atmosphere` folder.
10. In the `atmosphere` folder, make a folder called `kips`.
11. If you are above firmware 3.0.0, copy `sys-ftpd.kip` to the `kips` folder. Otherwise, skip this step.
12. Copy `hekate_ipl.ini` to the `bootloader` folder on your SD card.
13. Safely remove your microSD card and plug it back in your Switch.

---

### Next step

The next step depends on the platform you want to boot CFW from.

- If you plan on booting CFW from a Windows system, go [here](os-specific-preparations/windows.html)
- If you plan on booting CFW from a macOS or Linux system, go [here](os-specific-preparations/linux.html)
- If you plan on booting CFW from an Android or chromeOS device, go [here](os-specific-preparations/android.html)
