# ✅ OpenCore EFI – macOS Sequoia 15.5 – AMD Ryzen 9 5900X + RX 6700 XT
![OpenCore 1.0.5](https://img.shields.io/badge/OpenCore-1.0.5-blue.svg)
![Status: Stable](https://img.shields.io/badge/Status-Stable-brightgreen.svg)
![macOS Sequoia](https://img.shields.io/badge/macOS-Sequoia%2015.5-red.svg)

This is a working and stable EFI for **macOS Sequoia 15.5**, fully optimized for AMD Ryzen and Radeon RX 6700 XT. Built for performance and reliability, with support for iServices, proper USB mapping, and full GPU acceleration using **NootRX** (no WhateverGreen).

Tested using **OpenCore 1.0.5**.

---

## 🖥️ System Specs

| Component      | Model / Details                                     |
|----------------|-----------------------------------------------------|
| **CPU**        | AMD Ryzen 9 5900X (12-core, 24-thread)              |
| **GPU**        | AMD Radeon RX 6700 XT                               |
| **Motherboard**| ASUS ROG Strix B550-F Gaming (non-WiFi)             |
| **Audio**      | Realtek ALC S1220A (working via `alcid=1`)          |
| **Ethernet**   | Intel I225-V 2.5Gb (patched using `IntelMausi.kext`)|
| **Storage**    | Internal SSD (Sequoia 15.5 installed)               |
| **Boot Mode**  | UEFI (Windows dual-boot compatible)                 |
| **SMBIOS**     | iMacPro1,1                                          |
| **USB Mapping**| USBToolBox + custom UTBMap.kext                     |

---

## ✅ Features

- Full GPU acceleration with **NootRX.kext**
- Native audio via AppleALC (`alcid=1`)
- Intel 2.5Gb Ethernet via IntelMausi.kext
- Proper USB mapping via USBToolBox and UTBMap.kext
- All Apple iServices working (iMessage, iCloud, FaceTime, App Store)
- Power management using `SSDT-EC-USBX` and `SSDT-SBUS-MCHC`
- Windows dual-boot compatible

---

## ⚙️ Boot Arguments

-v keepsyms=1 debug=0x100 amfi=0x80 agdpmod=pikera alcid=1 radpg=15

---

## 📁 Included Kexts

- `Lilu.kext`
- `NootRX.kext`
- `VirtualSMC.kext`
- `SMCProcessor.kext`
- `SMCSuperIO.kext`
- `AppleALC.kext`
- `IntelMausi.kext`
- `USBToolBox.kext`
- `UTBMap.kext`

---

## ⚠️ Notes

- Built for Sequoia 15.5 — also compatible with Sonoma and Ventura.
- Secure Boot and CFG Lock must be disabled in BIOS.
- Resize BAR should be **disabled**. Above 4G Decoding **enabled**.
- No wireless card required — built for the non-WiFi board version.

---

## 🧠 Recommended BIOS Settings

- Above 4G Decoding: **Enabled**  
- Resize BAR: **Disabled**  
- CSM: **Disabled**  
- Secure Boot: **Disabled**  
- SVM (Virtualization): **Enabled**  
- CFG Lock: **Disabled**

---

## 📝 Credits

- [OpenCore Team](https://github.com/acidanthera)
- [NootRX by xCuri0](https://github.com/xCuri0/NootRX)
- [USBToolBox](https://github.com/USBToolBox/tool)
- [Dortania Guide](https://dortania.github.io/)
- Hackintosh Discord & AppleLife Forums
