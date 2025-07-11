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
- ✅ Radeon GPU support powered by **NooTRX** kext instead of WhateverGreen  

---

## ⚙️ Requirements (Windows)

- Windows PC with admin rights  
- USB flash drive (at least 16 GB) formatted as FAT32 or exFAT  
- macOS Installer: You can use either **Litemint09’s RDRS** or the official **macOS Sequoia 15.5 installer**  
- [GibMacOS](https://github.com/corpnewt/gibMacOS) or similar tools for downloading macOS installers on Windows  
- [MountEFI](https://github.com/crypticmind/MountEFI) or [EFI Mounter](https://github.com/SoniEx2/EFI-Mounter) for mounting EFI partitions in Windows  
- [ProperTree](https://github.com/corpnewt/ProperTree) for editing plist files  
- [smibosgen.bat](https://github.com/dortania/OC-Gen-X) or similar SMBIOS generator for creating serials  
- 7-Zip or similar tool for extracting archives  

---

## 🚀 Installation Instructions (Windows)

1. **Download macOS Installer**  
   Use [GibMacOS](https://github.com/corpnewt/gibMacOS) on Windows to download macOS Sequoia 15.5 installer app.

2. **Create macOS USB Installer**  
   Use [TransMac](https://www.acutesystems.com/scrtm.htm) or [balenaEtcher](https://www.balena.io/etcher/) (with a DMG) to flash macOS installer onto USB drive. Alternatively, use Terminal on macOS if available.

3. **Copy EFI Folder**  
   Use [MountEFI](https://github.com/crypticmind/MountEFI) to mount the EFI partition of the USB installer, then replace the EFI folder with this repository’s EFI folder.

4. **Configure BIOS Settings**  
   - Disable Secure Boot  
   - Set SATA Mode to AHCI  
   - Disable Fast Boot  
   - Disable CFG Lock (if available)  
   - Enable USB Legacy Support (if applicable)  

5. **Boot Installer**  
   Boot from the USB installer on your Ryzen system and install macOS Sequoia 15.5.

6. **Post-install EFI Setup**  
   After installation, use [MountEFI](https://github.com/crypticmind/MountEFI) on Windows to mount your macOS system drive EFI partition and replace its EFI folder with this configured EFI.

7. **Generate SMBIOS Serials**  
   Run `smibosgen.bat` or use [OC-Gen-X](https://github.com/dortania/OC-Gen-X) on Windows to generate fresh SMBIOS serials and update your config.plist accordingly with ProperTree.

---

## 🔧 Troubleshooting

- **Black screen on boot:**  
  Make sure boot args include `agdpmod=pikera` and that **NooTRX** kext is properly installed.

- **WiFi not working:**  
  Use a supported USB WiFi dongle with Chris1111’s patch; onboard WiFi not supported.

- **Freezing or kernel panics:**  
  Verify BIOS settings and USB port mapping via USBToolBox.

- **Audio issues:**  
  Confirm `alcid=1` boot arg; try alternate layout IDs if needed.

- **Apple services issues:**  
  Re-generate SMBIOS serials and system identifiers with `smibosgen.bat`.

---

## 🙌 Credits

- OpenCore Team — [https://github.com/acidanthera/OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)  
- Chris1111 — Wireless USB Adapter patch [https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)  
- AMD OSX Community  
- **NooTRX** (Radeon GPU support)  
- USBToolBox  

---

## 📬 Contact

For support or questions:  
**Email:** [waynegrizzley@gmail.com](mailto:waynegrizzley@gmail.com)  
**Website:** [www.waynegrizzley.com](https://www.waynegrizzley.com)  

---

## ⚠️ Disclaimer

Use at your own risk. No warranty or guarantee.

---

Enjoy your Hackintosh Ryzen build with Radeon GPU acceleration powered by **NooTRX** and USB WiFi support! 🎉
