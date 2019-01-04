---
layout: single
title: NAND dumping (Android/chromeOS)
---

{%include nand-dump-infobox.md %}

### Dump your NAND.

1. Boot your Switch into RCM and connect it to your device, see [this guide](https://noirscape.github.io/RCM-Guide){: target="_blank" } for more information on RCM.
2. Go to [this website](https://atlas44.s3-us-west-2.amazonaws.com/web-fusee-launcher/index.html){: target="_blank"}.
3. Under the Payload section, select upload payload and upload the .bin file you previously downloaded.
4. Click `do the thing`, select `APX` and click connect.</li>
5. Use the volume and power buttons to select `Tools`, then select `Backup`.
6. Use the volume and power buttons to select `Backup eMMC BOOT0/1`.
7. Wait for the backup to complete. This should not take too long.
8. Press any key to return to the Hekate menu.
9. Use the volume and power buttons to select `Backup eMMC RAW GPP`.
10. For the next step, it depends on wether you have an SD card that has at least 30GB of storage free.
  - If you have an SD card that at least 30GB of storage available, you can just wait for the backup to complete. This can easily take several hours.
  - If you don't have an SD card that has at least 30GB of storage available, Hekate will make partial NAND dumps and you will need to move them to your computer during the backup. Hekate will prompt you when to do this. When it does, plug your SD card into your computer and move the `backup/(number)/rawnand.bin` files (they'll be named as `rawnand.bin.00`, `rawnand.bin.01` and so on) to a folder on your computer. After that, unplug your SD card and put it in your Switch, press any button and then select `Backup eMMC RAW GPP` again. Rinse and repeat until it says it finished.
11. Unplug your SD card and put it in your phone.
12. Move the contents of the `backup` folder to a safe folder on your phone.
13. Put your SD card back in your Switch.
14. If your SD card has had less than 30GB of space available during the backup process or your SD card was not formatted as exFAT, you will need to combine the "rawnand.bin" files. See [NAND dumping (combining partial dumps)](rawnand-combine.html) for instructions on how to do this. You will need a macOS/Linux or Windows device to combine your NAND dumps.

[Continue to Launching CFW (Android)]({{ '/launching-cfw/android.html' | relative_url }})
{: .notice--primary}