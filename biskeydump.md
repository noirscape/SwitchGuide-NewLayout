---
layout: default
title: Dumping your BIS keys.
---

You cannot currently get your BIS keys on any device running 6.2 or higher.
{: .info-box}

BIS keys are console-specific. It is not possible to use another consoles BIS keys. Do not share your BIS keys!
{: .info-box}

In this step we will dump your BIS keys. Your BIS keys are needed in case you accidentally update your NAND and wish to downgrade it later or if you want to extract files from your NAND dumps.

## What you will need.

- The latest version of [biskeydump](https://switchtools.sshnuke.net/).

## Dumping your BIS keys

1. Turn off your switch and put it in your computer.
2. From the biskeydump zip, extract `biskeydump.bin`.
3. Copy `biskeydump.bin` to the `payloads` folder in the `bootloader` folder on your SD card.
4. Launch Hekate using the steps at [Launching CFW](/launching-cfw/). Stop at the step where it tells you to launch Atmosphere.
5. Go to `Launch` -> `Payloads` -> `biskeydump.bin`.
6. Wait a few seconds and your BIS keys should appear on top of the screen, as well as a QR code.
7. Scan the QR code using your phone.
8. You now have your BIS keys on your phone's clipboard.
9. Store these BIS keys in a safe place.

You should read the [Final Notes]({{ '/finalizing.html' | relative_url }}){: .a-table}.
{: .info-box}