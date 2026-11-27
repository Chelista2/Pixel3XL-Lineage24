<div align="center">

# 📱 LineageOS 24.0 for Google Pixel 3 XL (`crosshatch`)

[![LineageOS](https://img.shields.io/badge/LineageOS-24.0-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](https://lineageos.org/)
[![Android](https://img.shields.io/badge/Android-17-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![Device](https://img.shields.io/badge/Device-Google%20Pixel%203%20XL-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://wiki.lineageos.org/devices/crosshatch/)
[![Status](https://img.shields.io/badge/Status-Still%20in%20Work%20%7C%20Not%20for%20Download-red?style=for-the-badge)](https://img.shields.io/badge/Why_did_you_click_that%3F-Don't_be_so_impatient_--_it_literally_says_not_for_download!-blueviolet?style=for-the-badge "Why did you click that? Don't be so impatient!")
**Unofficial LineageOS 24.0 builds & device resources for the Google Pixel 3 XL (`crosshatch`).**

[📥 Downloads](../../releases) • [🐛 Report a Bug](../../issues) • [💬 Discussions](../../discussions)

</div>

---

## 📋 Device Specifications

| Feature | Specification |
| :--- | :--- |
| **Codename** | `crosshatch` |
| **SoC** | Qualcomm SDM845 Snapdragon 845 (10 nm) |
| **CPU** | Octa-core (4x2.5 GHz Kryo 385 Gold & 4x1.6 GHz Kryo 385 Silver) |
| **GPU** | Adreno 630 |
| **Memory** | 4 GB LPDDR4X RAM |
| **Storage** | 64 GB / 128 GB UFS 2.1 |
| **Display** | 6.3" P-OLED, 1440 x 2960 pixels (~523 ppi) |
| **Battery** | 3430 mAh Li-Po |

---

## ⚙️ Current Status

| Component | Status | Notes |
| :--- | :---: | :--- |
| **Boot / System** | ⚠️ | untested / still in Work |
| **Display & Touch** | ⚠️ | untested / still in Work |
| **Wi-Fi & Bluetooth** | ⚠️ | untested / still in Work |
| **RIL (Calls / SMS / Data)** | ⚠️ | untested / still in Work |
| **Camera (Front / Back)** | ⚠️ | untested / still in Work |
| **Audio & Speakers** | ⚠️ | untested / still in Work |
| **Fingerprint Sensor** | ⚠️ | untested / still in Work |
| **NFC / Google Pay** | ⚠️ | untested / still in Work |
| **SELinux** | ⚠️ | untested / still in Work |

---

## 🚀 Installation Guide

> **⚠️ Disclaimer:** Flashing custom ROMs carries inherent risks. Back up all your important data before proceeding. We are not responsible for bricked devices, lost data, dead cats, atomic wars. If you brick your device Ill laught at you.

### Prerequisites
* Unlocked Bootloader
* Latest `adb` and `fastboot` tools installed on your PC
* LineageOS Recovery (`boot.img` / `vendor_boot.img`) & ROM `.zip` from the [Releases](../../releases) page (not aviable yet / building still in progress)

### Flashing Steps
1. **Reboot into Bootloader:**
   ```bash
   adb reboot bootloader
