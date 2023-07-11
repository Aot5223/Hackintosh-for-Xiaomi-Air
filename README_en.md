<h1> Xiaomi Air 13,3 Laptop Black Apple </h1>

<b> Hackintosh for 小米 Air 13,3



# 📄 Contents
- [Language Selection](#語言選擇/语言选择)
- [Project Notes](#Project-notes)
- [profile](#profile)
- [Download address](#Download-address)
- [configuration](#configuration)
- [System compatibility](#System-compatibility)
- [Update log](Update-log.md)
- [What works and doesn't work](#What-works-and-doesn't-work)
- [Installation Guide](#Installation-Guide)
- [thank you](#thank-you)
- [Contact information](#contact-information)
- [Copyright Notice](#Copyright-Notice)


## 🔎 語言選擇/语言选择
- [Traditional Chinese Version](README_繁體中文.md)
- [简体中文](README.md)



## 📢 project precautions
- This EFI file is only available for Mi Air 13,3 notebooks and does not guarantee compatibility on other devices.
- Please read the instructions carefully when using this item.
- This project only provides black Apple EFI files and does not contain macOS image files.
- During the installation process, ensure that all data is backed up to avoid accidental loss.
- This project is for study and research purposes only, not for commercial or other illegal purposes
- When installing and using the system, please comply with relevant laws and regulations and intellectual property protection provisions.
- The use of this project may pose a certain risk to your computer, if you encounter any problems, please refer to the discussion in the Hackintosh community or seek professional help. Or in the [Issues] (https://github.com/username/repo/issues) some questions we will contact you as soon as possible to solve.


## 📦 configuration file

The EFI profile provided with this project contains the following:

` ` `
EFI
├── BOOT
│   └── BOOTx64.efi
└── OC
├── ACPI
├── Kexts
├── Drivers
├── Resources
├── Tools
├── config.plist
└── Opencore.efi
` ` `

Among them, Bootx64.efi in Boot is the notebook EFI boot file; The ACPI in OC contains files such as DSDT, SSDT, UEFI variable and patch, Kexts contains Drivers, Drivers contains OpenCore bootloader, and Tools contains OpenCore related tools. Resources contains the Opencore boot interface theme (graphical interface), config.plist is the OpenCore configuration file, Opencore.efi is the Opencore boot file.




[! [Download from  https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/releases](https://img.shields.io/github/v/release/Aot5223/Hackintos H - for - Xiaomi - Air? Label = download)] (https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/releases)

## ⚙ configuration

| Configuration | Model |
|--------------|-----------------------------|
| Processor | i5-6200U |
| Core display | Intel HD 520 |
| only display | NVIDIA GeForce 940MX (masked) |
| memory | 8GB DDR4 |
| hard drive | Samsung 256 SSD |
| sound card | Realtek ALC298 |
| wireless card | |
| touch pad | |
| OpenCore version | [! [](https://img.shields.io/github/v/release/acidanthera/OpenCorePkg?include_prereleases&style=social&label=&logo=apple)]( https://github.com/acidanthera/OpenCorePkg/releases)     |

## ✅ System compatibility

- [x] Mojave and High Sierra
- [x] Catalina
- [x] Big Sur
- [x] Monterey
- [x] Ventura

## ❓ What works and doesn't work
- [x] USB port
- [x] Intel HD 520
- [x] Sound card
- [x] Microphone
- [x] WiFi
- [X] Bluetooth
- [x] Battery
- [x] Trackpad
- [x] Sleep and wake up
- [x] BootCamp
- [ ] NVIDIA GeForce 940MX


## 🛠 Installation Guide

### Change BIOS Settings


### Hard Drive (solid state) Settings
- Confirm that the disk is in GUID format
- Ensure that the EFI partition is larger than 400 MHZ
- Confirm that there are no built-in solid and mechanical disks not supported by other Black Apples

### Download and install Mac
1. [download] (https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/releases) the EFI files in the warehouse.
2. Use a USB startup disk creation tools [Etcher] (https://www.balena.io/etcher/) (recommended) production of U disk boot disk.
3. Copy the EFI folder to the EFI partition of the USB flash drive.
4. Enter the BIOS Settings and select a USB flash drive from Boot Options.
5. On the OpenCore boot screen, select Install macOS on the USB flash drive.
6. Follow the installation wizard to complete the installation.
7. After the installation is complete, copy the EFI folder on the USB flash drive to the EFI partition of the computer hard drive.
8. Restart the PC to access the macOS.


### Change SMBIOS (three codes)
- Use the model menu of OCAT or OpenCore Configurator to generate your unique 'SMBIOS (three codes)' information.
'SMBIOS (three codes)' must be unique and you cannot use one that exists in this' repository (EFI) '.
- Run the tool and select Generate SMBIOS.
- Use the table below to select the right model for your hardware.

| brand | Model number |
|--------------|-----------------------------|
| Apple | Apple MacBook Pro 13,3 |


- Go to the 'Apple Serial Number Query Website' via the tool's Verify serial number button and enter the verification code (the serial number is entered automatically).
- Requires an "invalid serial number" or "Purchase date not verified" message to work. If you get other prompts, you must generate a new 'SMBIOS (three codes)' and check again.

### Use BootCamp
[corpnewt] (https://github.com/corpnewt) - download [brigadier] (https://github.com/corpnewt/brigadier)
- Install py as prompted
- The program automatically downloads' Bootcamp program on Windows' after completion
- Follow the prompts to open the downloaded 'dmg' and copy the files inside to the Windows system disk
- Go to EFI's model Settings' Open using OCAT or OpenCore Configurator ', modify model 'UpdateSMBIOSMod to Create and enable SpoofVendor' to make Windows think you are a Mac model
- Restart Windows (How to enter Windows [BIOS](#BIOS))
- Install the Bootcamp program
- Follow the installer prompts to restart, then return to 'Mac'
- Go to EFI's model Settings' Open using OCAT or OpenCore Configurator ', modify the model's modification model 'UpdateSMBIOSMod to Custom and turn off SpoofVendor' so that Windows no longer considers you a Mac model
- Done! Enjoy the white Apple boot


## 🙏 Thank you


- [dortania/OpenCore-Install-Guide](https://github.com/dortania/OpenCore-Install-Guide)
- [Acidanthera](https://github.com/acidanthera)
- [Hackintosh](https://github.com/daliansky/Hackintosh)
- [brigadier](https://github.com/corpnewt/brigadier)



## 📧 Contact information

If you have any questions or suggestions, please contact the authors of this project.

- Email: 1551656605@qq.com
- GitHub:https://github.com/bilijp153
- can also be through a lot [Issues] (https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/issues) to contact us.


## 📄 Copyright Notice
This project follows the MIT open source protocol. You are free to use, modify, and distribute this project, provided that you cite the source and retain the original copyright notice. For details, see the License file.

© 2023 Aot5223.  All rights reserved.
