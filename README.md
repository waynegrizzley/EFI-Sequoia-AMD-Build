# ✅ OpenCore 1.0.5 EFI for Ryzen 9 5900X + Radeon RX 6700 XT

**macOS Version:** Sequoia 15.5 (Build 23G90)  
**OpenCore Version:** 1.0.5  
**Motherboard:** ASUS ROG Strix B550-F Gaming (Non-WiFi)  
**CPU:** AMD Ryzen 9 5900X  
**GPU:** Radeon RX 6700 XT  

---

## ✔️ Features

- ✅ Full Ryzen 9 5900X CPU support with kernel patches  
- ✅ Radeon RX 6700 XT GPU acceleration with `agdpmod=pikera`  
- ✅ USB WiFi dongle hack enabled via [Chris1111 Wireless USB Adapter patch](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)  
- ✅ Native Intel 2.5Gb Ethernet support configured  
- ✅ Realtek ALC1200 audio configured with `alcid=1`  
- ✅ Custom USB port mapping with USBToolBox `UTBMap`  
- ✅ SMBIOS generated for Ryzen platform — supports iMessage & App Store  
- ✅ Boot Arguments: `-v keepsyms=1 debug=0x100 amfi=0x80 agdpmod=pikera alcid=1 radpg=15`  
- ✅ BIOS tweaks: Secure Boot off, SATA AHCI mode, Fast Boot disabled  

---

## ⚙️ Requirements

- ASUS ROG Strix B550-F Gaming (non-WiFi) motherboard  
- AMD Ryzen 9 5900X CPU  
- Radeon RX 6700 XT GPU  
- Compatible USB WiFi dongle (per Chris1111 patch)  
- USB flash drive (FAT32 formatted) for macOS installer  
- macOS Sequoia 15.5 Installer  

---

## 🚀 Installation Instructions

1. **Prepare macOS USB Installer**  
   Use GibMacOS or Terminal to create a bootable macOS Sequoia 15.5 USB installer.

2. **Copy EFI Folder**  
   Mount the EFI partition on the USB installer and replace the EFI folder with this repository’s EFI.

3. **BIOS Setup**  
   - Disable Secure Boot  
   - Set SATA Mode to AHCI  
   - Disable Fast Boot  
   - Disable CFG Lock if present  
   - Enable USB Legacy Support (if applicable)  

4. **Boot Installer**  
   Boot your system from the USB installer and proceed with macOS installation.

5. **Post-Install**  
   After installation, mount your system drive’s EFI and copy this EFI folder there.

---

## 🔧 Troubleshooting

- **Black screen on boot**  
  Ensure `agdpmod=pikera` is in boot args and WhateverGreen kext is up to date.

- **WiFi not working**  
  Use a supported USB WiFi dongle with Chris1111’s patch; onboard WiFi not supported.

- **System freezes or kernel panics**  
  Double-check BIOS settings and USB port mapping to avoid overcurrent or conflicts.

- **No sound / Audio issues**  
  Confirm `alcid=1` boot arg and verify Realtek codec compatibility.

- **Apple services not working (iMessage, FaceTime)**  
  Run `smibosgen.bat` to generate new SMBIOS serials and system identifiers.

---

## 🙌 Credits

- OpenCore Team — [https://github.com/acidanthera/OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)  
- Chris1111 — Wireless USB Adapter patch [https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)  
- AMD OSX Community for Ryzen patches  
- WhateverGreen for AMD GPU support  
- USBToolBox for USB port mapping  

---

## 📬 Contact

If you have questions or issues, contact:  
**Email:** [waynegrizzley@gmail.com](mailto:waynegrizzley@gmail.com)  
**Website:** [www.waynegrizzley.com](https://www.waynegrizzley.com)  

---

## ⚠️ Disclaimer

Use this EFI at your own risk. No warranty or guarantees are provided.  

---

Enjoy your smooth Hackintosh Ryzen build with Radeon GPU acceleration and USB WiFi support! 🎉
