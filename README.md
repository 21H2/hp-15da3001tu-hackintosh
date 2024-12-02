# HP 15 DA3001TU Hackintosh EFI 🌙  
_A minimalist EFI setup for the HP 15 DA3001TU with Intel Core i3 1005G1._

---

## ✨ Overview  
This repository contains the EFI folder for macOS on the HP 15 DA3001TU, tailored for Hackintosh enthusiasts who value simplicity and efficiency. Please note: **Graphics acceleration is not working**, and Wi-Fi is unsupported due to the Realtek wireless card.

**Specs:**  
- **Model:** HP 15 DA3001TU  
- **Processor:** Intel Core i3 1005G1  
- **Graphics:** Integrated Intel UHD Graphics (no acceleration)  
- **Wi-Fi:** Not supported (Realtek card)  
- **Bootloader:** OpenCore  

---

## ⚙️ Features  
- Basic macOS functionality with Intel i3 processor.  
- Configured for stability with minimal issues.  
- Designed for future updates and easy customization.  

---

## 🚧 What's Missing?  
- **Graphics Acceleration**: Integrated Intel UHD Graphics are not fully accelerated, resulting in reduced performance for graphic-heavy tasks.  
- **Wi-Fi Support**: No driver available for the Realtek wireless card. You might need a USB Wi-Fi dongle or compatible PCIe card for wireless connectivity.  
- **SMBIOS Configuration**: You'll need to customize your SMBIOS for iCloud and App Store functionality.  

> Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate and customize a valid SMBIOS.  

---

## 📂 EFI Details  
- **OpenCore Version**: [Insert OpenCore version used]  
- **Kexts Included**:  
  - Lilu.kext  
  - WhateverGreen.kext (for basic graphics support, though acceleration is not functional)  
  - VirtualSMC.kext  
  - IntelMAK kext (for Intel CPUs)  
  - USBInjectAll.kext (for USB mapping)  

---

## 🔧 Installation  

1. **Prepare USB:**  
   - Format your USB drive as `MacOS Extended (Journaled)` with a GUID partition table.  
   - Create a bootable macOS installer using Terminal (refer to [this guide](https://dortania.github.io/OpenCore-Install-Guide/)).

2. **Copy EFI Folder:**  
   - Replace the default EFI folder on your USB with the one provided in this repository.  

3. **Customize SMBIOS:**  
   - Open `config.plist` with [ProperTree](https://github.com/corpnewt/ProperTree) and generate a new SMBIOS.  
   - Choose a suitable model (e.g., MacBook Air 2020) for best compatibility with macOS services like iCloud and App Store.

4. **BIOS Settings:**  
   - **Disable Secure Boot** in BIOS.  
   - Set SATA mode to **AHCI** for storage devices.  
   - Set Boot Mode to **UEFI**.  
   - Disable **Fast Boot** if necessary.  

---

## 🌸 Recommendations  

- **Graphics Acceleration**: Since graphics acceleration is not functional, avoid heavy graphic tasks. Keep an eye out for future updates to OpenCore and kexts for possible support.  
- **Wi-Fi Support**: Replace the Realtek Wi-Fi card with a compatible one like the **Broadcom BCM94360NG** or use a USB Wi-Fi dongle.  
- **Audio**: Ensure you install necessary kexts for audio functionality if sound is not working. Look into **AppleALC** or **VoodooHDA** kexts based on your needs.  
- **USB Devices**: If USB ports are not working, ensure USB mapping is correctly set up in `config.plist` and try the **USBInjectAll.kext**.

---

## 🖤 Disclaimer  
This EFI is provided "as-is." I am not responsible for any damage to your system. Ensure you have backups before making changes.  

---

### ✨ Aesthetics Matter  
_“In chaos, I find structure. In the unknown, I build systems.”_  

Enjoy the blend of beauty and functionality. 🌌  
