---
description: The title says it all!
---

# 📲 Flashing Your Freshly Baked ROM to your device!

So once, you've completed the build successfully first of all pat yourself on your back no, just do it right now! That is incredible! Now lets know how to flash your build to your device.

## 1. Prerequisites

### A. Fastboot and ADB Drivers

If you haven't built them yet fire-up terminal in the eternal directory and :

```
make fastboot adb
```

### B. Unlocked Bootloader

An Unlocked Bootloader is a must for all of this, if your device already has an unlocked bootloader I'm pretty sure you what it is. You may make a search online :

```
How to Unlock Bootloader on [Full Device Name]?
```

{% hint style="info" %}
**Warning! Unlocking Bootloader of your device might void your warranty be sure while doing this step, we are not responsible for anything happening prior or after unlocking the bootloader!**
{% endhint %}

Once, Your Bootloader is Unlocked Follow here.

### C. Enable USB Debugging

On your device, go to "Settings" > "Developer options" (if available) or "About phone" > tap on the "Build number" multiple times until it says you're a developer. Then go back to the main settings and find "Developer options." Enable "USB debugging."

### D. Locate the ROM file

The Location of the ROM file in general is :

```
eternal/out/target/product/<device_codename>/rom_file.zip
```

## 2. Flashing

The command may vary sometimes due to frequent changes. A typical Fastboot command to flash a ROM is:

```perl
fastboot flash system rom_file_name.zip
```

Replace "rom\_file\_name.zip" with the actual name of your ROM file.

### 3. Wait for the flashing process to complete

The Fastboot command will start flashing the ROM onto your device. It may take a few minutes to complete. Do not disconnect your device during this process.

### 4. Wipe all data

Do `fastboot -w` and all your data would be wiped!

### 5. Reboot

Do `fastboot reboot` and your device shall boot into the Eternal OS ROM Enjoy and be sure to publish it on forum.xda-developers.com!

### 6. Bonus (for who have completed)

When Publishing on XDA use this template!

##

_Portions of this page are reproduced from work created and_ [_shared by the Android Open Source Project_](https://code.google.com/p/android/) _and used according to terms described in the_ [_Creative Commons 3.0 Attribution License_](https://creativecommons.org/licenses/by/4.0/)_._
