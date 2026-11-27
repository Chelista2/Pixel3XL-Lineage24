<div align="center">

# 📱 LineageOS 24.0 for Google Pixel 3 XL (`crosshatch`)

[![LineageOS](https://img.shields.io/badge/LineageOS-24.0-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](https://lineageos.org/)
[![Android](https://img.shields.io/badge/Android-17-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![Device](https://img.shields.io/badge/Device-Google%20Pixel%203%20XL-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://wiki.lineageos.org/devices/crosshatch/)
[![Status](https://img.shields.io/badge/Status-Still%20in%20Work%20%7C%20Not%20for%20Download-red?style=for-the-badge)](https://img.shields.io/badge/Why_did_you_click_that%3F-Don't_be_so_impatient_--_it_literally_says_not_for_download!-blueviolet?style=for-the-badge "Why did you click that? Don't be so impatient!")  
[![Copium](https://img.shields.io/badge/Compile_Success_Chance-0.02%25_&_Prayers-ff1493?style=for-the-badge)](#building-from-source)  [![Notch](https://img.shields.io/badge/Notch_Size-Absolute_Unit-111111?style=for-the-badge)](#device-specifications)

**Unofficial LineageOS 24.0 builds & device resources for the Google Pixel 3 XL (`crosshatch`).**

[📥 Downloads](../../releases) • [🐛 Report a Bug](../../issues) • [💬 Discussions](../../discussions)

</div>

---

## 📋 Device Specifications

<table>
  <tr>
    <td valign="top">

| Feature | Specification |
| :--- | :--- |
| **Codename** | `crosshatch` |
| **SoC** | Qualcomm SDM845 Snapdragon 845 (10 nm) — runs hot enough to toast bread |
| **CPU** | Octa-core (4x2.5 GHz Kryo 385 Gold & 4x1.6 GHz Kryo 385 Silver) |
| **GPU** | Adreno 630 |
| **Memory** | 4 GB LPDDR4X RAM (Ram Altman would be happy) |
| **Storage** | 64 GB / 128 GB UFS 2.1 |
| **Display** | 6.3" P-OLED, 1440 x 2960 pixels (~523 ppi) + two speaker cutouts that look like a surprised face |
| **Battery** | 3430 mAh Li-Po (now includes complimentary 18% spicy pillow energy) |

</td>
    <td align="center" valign="middle" width="260">
      <img src="https://wiki.lineageos.org/images/devices/crosshatch.png" alt="Google Pixel 3 XL" width="210" />
    </td>
  </tr>
</table>

---

## ⚙️ Current Status

| Component | Status | Notes |
| :--- | :---: | :--- |
| **Boot / System** | ⚠️ | untested / still in Work — either boots into Android 17 or summons a demon |
| **Display & Touch** | ⚠️ | untested / still in Work — touch may respond to telepathy only |
| **Wi-Fi & Bluetooth** | ⚠️ | untested / still in Work — pairs exclusively with haunted smart fridges |
| **RIL (Calls / SMS / Data)** | ⚠️ | untested / still in Work — emergency calls only (including 911 for your sanity) |
| **Camera (Front / Back)** | ⚠️ | untested / still in Work — front cam captures existential dread in 4K |
| **Audio & Speakers** | ⚠️ | untested / still in Work — plays Enigma at max volume on boot |
| **Fingerprint Sensor** | ⚠️ | untested / still in Work — unlocks if you whisper "please" |
| **NFC / Google Pay** | ⚠️ | untested / still in Work — pays with hopes, dreams, and lint |
| **SELinux** | ⚠️ | untested / still in Work — currently negotiating a ceasefire |

---

## 🚀 Installation Guide

> **⚠️ Disclaimer:** Flashing custom ROMs carries inherent risks. Back up all your important data before proceeding. We are not responsible for bricked devices, lost data, your death, your house burning down, atomic wars, sudden spontaneous combustion of your toaster, or the heat death of the universe.

### Prerequisites
- Unlocked Bootloader (if it's carrier-locked, go cry in a corner)
- Latest `adb` and `fastboot` tools installed on your PC (not a version from 2014 found on a sketchy forum)
- ROM `.zip` (and `boot.img` / `twrp.img`) from the [Releases](../../releases) page (spoiler: they aren't there yet)
- The phone itself
- Usb cable (ideally one that doesn't disconnect if a cat sneezes nearby)
- A brain (obviously)
- Emotional resilience for bootloops

---

### Method 1: LineageOS Recovery (ADB Sideload)



**Reboot into Bootloader:**
```bash

adb reboot bootloader

```

2. **Flash LineageOS Recovery:**

```bash

fastboot flash boot boot.img

```

3. **Boot into Recovery:**

Use the volume buttons to select **Recovery Mode** and confirm with the Power button.

4. **Factory Reset (Required for clean install):**

In LineageOS Recovery, navigate to **Factory Reset** ➔ **Format data / factory reset**.

5. **Sideload the ROM:**

Go back to the main menu, select **Apply Update** ➔ **Apply from ADB**, and run:

```bash

adb sideload lineage-24.0-XXXXXXXX-UNOFFICIAL-crosshatch.zip

```

6. *(Optional)* Flash **GApps** or **Magisk** via `adb sideload` right after (reboot to recovery if prompted).

7. Select **Reboot system now** and enjoy!



---



### Method 2: TWRP Recovery (ZIP Flash)



**Reboot into Bootloader:**
```bash

adb reboot bootloader

```

2. **Boot into TWRP:**

Temporarily boot TWRP (or flash it permanently depending on your setup):

```bash

fastboot boot twrp-x.x.x-crosshatch.img

```

3. **Wipe Data:**

In TWRP, go to **Wipe** ➔ **Format Data**, type `yes` to confirm, and reboot back into TWRP.

4. **Transfer the ROM ZIP:**

Copy `lineage-24.0-XXXXXXXX-UNOFFICIAL-crosshatch.zip` onto your device's internal storage via MTP or `adb push`:

```bash

adb push lineage-24.0-XXXXXXXX-UNOFFICIAL-crosshatch.zip /sdcard/

```

5. **Install the ROM:**

Go to **Install**, select the `lineage-24.0-XXXXXXXX-UNOFFICIAL-crosshatch.zip` file, and **Swipe to confirm Flash**.

6. *(Optional)* Reboot to TWRP if you want to flash **GApps** or **Magisk** afterwards.

7. Tap **Reboot System** and enjoy!



---



## 🙏 Credits & Acknowledgements

**[LineageOS Team](https://lineageos.org/)** for the incredible ROM base.
**Google** for kernel sources and device blobs.
Everyone contributing to `sdm845` and `crosshatch` development.
