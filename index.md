---
layout: splash
title: "Switch Homebrew Guide" #
header:
  overlay_color: "#5e616c" #
  overlay_image: assets/header.png
  overlay_filter: 0.5
  caption:

excerpt: "From zero to Hekate and Atmosphere!"
---

If you need assistance, visit us on [Discord](/discord.html){: target="_blank" }.
{: .notice--primary}

### Terminology used in this guide

- **Hekate**: A bootloader for the Nintendo Switch.
- **Atmosphère**: The CFW made by the Atmosphère-NX org.
- **CFW**: A Custom Firmware. Custom Firmware permits access to homebrew on the Nintendo Switch.
- **RCM**: A special mode of the Nintendo Switch's Tegra X1 chip that thanks to a bug allows us to push any payload to it. This exploit is known as ShofEL2 or fusee-gelee.
- **bootkit**: A folder on your computer that you will use to launch CFW from RCM. It contains a few scripts, TegraRCMSmash, fusee-gelee and the Hekate payload. You will set one up during this guide. You will need access to this folder each time you want to launch CFW, so keep it in a safe spot where you can find it later.
- **fusee-launcher**, **TegraRcmGui** and **web-fusee-launcher**: Programs that make use of the fusee-gelee exploit to push a payload to the Switch.
  - **intermezzo.bin** is a part of fusee-launcher.

### What are we doing to run homebrew on the Switch

This guide will boot you into Atmosphère using a combination of the RCM, the Hekate bootloader and Atmosphère CFW. In addition, this guide will enable an FTP server on your Switch to simplify transferring files while in Horizon. You will also be able to access the Homebrew menu by launching the album applet. This has only been tested from firmware 5.0.2 upwards, but theoretically should work on all firmware versions. Certain applications may not work on certain firmware versions so YMMV.

### What you will need

- A "first-generation" Switch. (All Switch consoles before July 2018 will work.)
  - If you are not sure about whether your Switch is a "first-generation" Switch, you can check [this thread](https://gbatemp.net/threads/switch-informations-by-serial-number.481215/). Match the first letters and numbers of your serial number to the list in the blue box. You can find your serial number using [these instructions by Nintendo](https://www.nintendo.com.au/how-to-find-the-serial-number-of-your-console).
    - If your serial number is listed as green, you have a "first-generation" Switch and will be able to boot CFW.
    - If your serial number is listed as orange, follow the guide, but you might not be able to boot CFW.
    - If your serial number is listed as red, your Switch is patched and you will not be able to boot CFW.
- A way to put your Switch into RCM. See [this guide](https://noirscape.github.io/RCM-Guide){: target="_blank" } for more information. Users on 1.0.0 can also enter RCM from a software side by using a program called reboot_to_rcm. See [here](1-0-0.html){: target="_blank" } for more details.
- A host PC running Windows, Linux, macOS or ChromeOS, or an Android device.
  - It's also possible to boot from a jailbroken iOS device using [NXBoot](https://mologie.github.io/nxboot/), but this is not officially supported.
- A USB Type-C to USB-A cable, or a USB Type-C to USB Type-C cable. (Depending on what your host PC supports.)
- If you are using an Android device, you need a way to connect the Switch to it, either a USB OTG cable, or USB-C to USB-C cable depending on what your device supports.
- A microSD card 2GB or larger, formatted to either FAT32, or exFAT (only if your switch has the exFAT support "update".)
  - The recommended SD card size is 128GB. This will allow you both store a NAND dump and make an emuNAND later on.
  - The recommended filesystem is FAT32. exFAT has issues with Homebrew due to filesystem corruption. exFAT SD cards can also not be used to run Lakka or other switch-linux implementations.

### What are the advantages to running homebrew

Running homebrew will allow you to run tools such as [Checkpoint](https://github.com/BernardoGiordano/Checkpoint){: target="_blank" }, a save manager or use [sys-ftpd](https://github.com/jakibaki/sys-ftpd) to run an FTP server to transfer files. You also can run emulators like [RetroArch](https://www.retroarch.com/?page=platforms){: target="_blank" } to play retro games on the Switch. In addition, you can run homebrew games such as [tetriswitch](https://gbatemp.net/threads/tetriswitch-a-tetris-clone-for-the-switch.498481){: target="_blank" } and [Pong](https://github.com/I-EAT-CHEEZE-YO/switch_sdl_pong){: target="_blank" } and [SudokuNX](https://github.com/ZetaDesigns/SudokuNX){: target="_blank" } or ports of other games, such as [Chocolate Doom](https://gbatemp.net/threads/chocolate-doom-ported-to-the-nintendo-switch.506909/){: target="_blank" }, [Doom 3](https://github.com/fgsfdsfgs/dhewm3){: target="_blank" } [Quake](https://github.com/fgsfdsfgs/nxquake){: target="_blank" }, [Wolfenstein 3D](https://gbatemp.net/threads/wolfenstein-3d-port.508755/){: target="_blank" } and [Duke Nukem 3D](https://gbatemp.net/threads/duke-nukem-3d.502386/){: target="_blank" }. It's also possible to [theme](https://github.com/suchmememanyskill/SwitchThemeGuide/wiki/NX-Theme-Injector) your Nintendo Switch.

### Are there any risks to running homebrew

Yes. Nintendo has increased the Telemetry on the Nintendo Switch compared to previous consoles and does ban if they detect you using homebrew. You can find more details on this and a comprehensive list [in the FAQ](faq.html#ban){: target="_blank" }. That said, Atmosphère, the CFW that will be installed if you use this guide includes the `creport` module. This module will store crash dumps to your SD card and does not report them to Nintendo. This means that you can safely use Homebrew.

---
Users on firmware 1.0.0 should follow the [1.0.0 guide](1-0-0.html) as it contains important instructions.
{: .notice--primary}

Go to [Setting up your SD card](sdcard.html) to get started.
{: .notice--primary}

---