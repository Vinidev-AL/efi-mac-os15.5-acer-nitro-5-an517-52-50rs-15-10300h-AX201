# EFI for Acer Nitro 5 - AN517-52-50RS (Compatible with macOS Sequoia)

> ⚠️ **Legal Disclaimer:** This project is intended strictly for educational and research purposes. macOS is a trademark of Apple Inc. This repository **does not contain or distribute any proprietary Apple software or resources**. We are not affiliated with, endorsed, or supported by Apple Inc. Installing macOS on non-Apple hardware may violate Apple's Terms of Service. Use at your own risk.

This repository contains a custom EFI configuration designed to enable macOS Sequoia to run on an Acer Nitro 5 laptop with the specifications listed below, using the OpenCore bootloader.

**Based on this project:**  
https://github.com/iwissemben/Hackintosh-Opencore-Acer-Nitro-5-AN515-55-51QY

---

## 🇬🇧 English

### Modifications
This EFI is based on version EFI-1.4 of the repository above and has been modified to support the Intel AX201 Wi-Fi card via HeliPort on macOS Sequoia 15.5.

### Tested Specifications
- **Model:** Acer Nitro 5 - AN517-52-50RS  
- **Processor:** Intel Core i5-10300H  
- **Wi-Fi:** Intel Wi-Fi 6 AX201  
- **RAM:** 16GB  
- **Storage:** Samsung 960 NVMe 512GB  
- **GPU:** NVIDIA GeForce GTX 1650 (Disabled)  
- **macOS Version:** Sequoia 15.5 

### Status

✅ Working:
- Wi-Fi (via HeliPort)
- Intel UHD integrated graphics
- Graphics acceleration
- Brightness control
- Keyboard and trackpad
- Power and thermal management
- Audio and USB ports

❌ Not working:
- Bluetooth
- Ethernet

☠️ Probably will never work:
- NVIDIA GTX 1650 (unsupported)
- HDMI output (wired to the NVIDIA GPU)

### BIOS Configuration
Before installation, make sure AHCI mode is enabled on your SSD:
1. Enter BIOS (press F2 at boot)
2. Go to the **Main** tab
3. Press `Ctrl + S` to reveal hidden options
4. Change **SATA Mode** or **VMD Controller** to **AHCI**
5. Save and reboot

### Installation

**Get the macOS Installer:**  
You can create your own installer using a real Mac or third-party tools available in the community. Trusted sources include Olarila, Dortania, or Hackintosh Elite.

**Install HeliPort:**  
HeliPort is a third-party utility that enables Intel Wi-Fi cards:
- https://github.com/OpenIntelWireless/HeliPort

**Grant Permission to Run HeliPort:**

```bash
sudo xattr -rd com.apple.quarantine /Applications/HeliPort.app
