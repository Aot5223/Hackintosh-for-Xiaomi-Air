<h1>小米 Air 13,3 笔记本的黑苹果</h1>  

 <b> Hackintosh for Xiaomi-Air 13,3
   

 
 # 📄 目录
- [语言选择（語言選擇/Language Selection）](#-语言选择)
- [项目注意事项](#-项目注意事项)
- [配置文件](#-配置文件)
- [下载地址](#-下载地址)
- [配置](#-配置)
- [系统兼容性](#-系统兼容性)
- [更新日志](更新日志.md)
- [什么工作和不工作](#-什么工作和不工作)
- [安装指南](#-安装指南)
- [感谢](#-感谢)
- [联系方式](#-联系方式)
- [版权声明](#-版权声明)


## 🔎 语言选择   
- [繁體中文版本](README_繁體中文.md) 
- [English Version](README_en.md)

 

## 📢 项目注意事项
- 该 EFI 文件仅适用于 小米Air  13,3笔记本，不保证在其他设备上的兼容性。
- 使用本项目时请仔细阅读使用方法。
- 本项目仅提供黑苹果 EFI 文件，不包含 macOS 操作系统镜像文件。
- 在安装过程中，请确保所有数据已备份，以免意外丢失。
- 本项目仅供学习和研究使用，请勿用于商业用途或其他非法用途 
- 在安装和使用该系统时，请遵守相关法律法规和知识产权保护规定。
- 使用本项目可能会对电脑造成一定风险，如果您遇到任何问题，请参考 Hackintosh 社区的相关讨论或寻求专业人士的帮助，或在 [Issues](https://github.com/username/repo/issues) 中提出问题我们将尽快与您联系解决。

 
## 📦 配置文件

该项目提供的 EFI 配置文件包含以下内容：

``` 
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
```
 
其中，Boot 里的 Bootx64.efi 是笔记本 EFI 引导文件；OC 里的 ACPI 包含了 DSDT、SSDT、UEFI 变量和补丁等文件，Kexts 包含了驱动程序，Drivers 包含了 OpenCore 引导程序，Tools 包含了 OpenCore 的相关工具，Resources 包含了 Opencore 的引导界面主题（图形界面），config.plist 是 OpenCore 配置文件，Opencore.efi 是 Opencore 引导文件。




[![Download from https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/releases](https://img.shields.io/github/v/release/Aot5223/Hackintosh-for-Xiaomi-Air?label=下载)](https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/releases)

## ⚙ 配置

|    配置       |        型号                 |
|--------------|-----------------------------|
|    处理器     |          i5-6200U          |
|     核显      |    Intel HD 520    |
|     独显      |      NVIDIA GeForce 940MX（已屏蔽）    |
|     内存      |     8GB DDR4         |
|     硬盘      |       Samsung 256 SSD        |
|     声卡      |       Realtek ALC298        |
|   无线网卡     |               |
|   触摸板     |              |
|  OpenCore版本     |          [![](https://img.shields.io/github/v/release/acidanthera/OpenCorePkg?include_prereleases&style=social&label=&logo=apple)](https://github.com/acidanthera/OpenCorePkg/releases)     |

## ✅ 系统兼容性

  - [x] Mojave和High Sierra
  - [x] Catalina 
  - [x] Big Sur 
  - [x] Monterey 
  - [x] Ventura 

注:Catalina从10.15.4版本起支持

## ❓ 什么工作和不工作
- [x] USB接口
- [x] Intel HD 520
- [x] 声卡
- [x] 耳机接口
- [x] 麦克风
- [x] WiFi
- [X] 蓝牙
- [x] 电池
- [x] 触控板
- [x] 睡眠和唤醒
- [x] BootCamp
- [ ] NVIDIA GeForce 940MX


## 🛠 安装指南

### 更改BIOS设置


### 硬盘（固态）设置
- 确认硬盘为GUID格式
- 确认硬盘EFI分区大于400M
- 确认没有内置其他黑苹果不支持的固态和机械盘

### 下载和安装Mac
1. [下载](https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/releases)本仓库中的 EFI 文件。
2. 使用 USB 启动盘创建工具（推荐[Etcher](https://www.balena.io/etcher/)）制作 U 盘启动盘。
3. 将 EFI 文件夹复制到 U 盘的 EFI 分区中。
4. 进入 BIOS 设置，在 Boot Options 中选择 U 盘启动。
5. 进入 OpenCore 引导界面，选择u盘中的“Install macOS”（安装 macOS）。
6. 根据安装向导完成安装。
7. 安装完成后，将 U 盘中的 EFI 文件夹复制到电脑硬盘的 EFI 分区中。
8. 重新启动电脑，即可进入 macOS 操作系统。


### 更改SMBIOS（三码）
- 使用OCAT或OpenCore Configurator（下称该工具）的机型菜单生成您唯一的`SMBIOS（三码）`信息。
`SMBIOS（三码）` 必须是唯一的，您不能使用此`存储库(EFI)`中存在的一个。
- 运行该工具并选择生成 SMBIOS。
- 使用下表为您的硬件选择合适的型号。

|    品牌       |        型号                 |
|--------------|-----------------------------|
|    Apple     |          Apple MacBook Pro 13,3          |


- 通过该工具的验证序列号按钮转到`苹果序列号查询网站`并输入验证码（序列号已自动输入）。
- 需要“无效序列号”或“未验证购买日期”消息才算能用。如果你得到是其他提示，必须生成 新的`SMBIOS（三码）`并再次检查。

### 使用BootCamp
- 下载[corpnewt](https://github.com/corpnewt)的[brigadier](https://github.com/corpnewt/brigadier)
- 按照提示安装py
- 完成后程序会自动下载`Windows上的Bootcamp程序`
- 按照提示把下载来的`dmg`打开，把里面的文件复制到Windows系统盘
- 进入EFI的机型设置`使用OCAT或OpenCore Configurator`打开，修改机型`UpdateSMBIOSMod为Create和开启SpoofVendor`让`Windows`认为你是Mac机型
- 重启进Windows（怎么进Windows看[BIOS](#BIOS)）
- 安装Bootcamp程序
- 按照安装程序提示重启，然后回`Mac`
- 进入EFI的机型设置`使用OCAT或OpenCore Configurator`打开，修改机型的修改机型`UpdateSMBIOSMod为Custom和关闭SpoofVendor`让`Windows`不再认为你是Mac机型
- 完成！享受白苹果方式的启动吧
   
   
## 🙏 感谢
 

  - [dortania/OpenCore-Install-Guide](https://github.com/dortania/OpenCore-Install-Guide)
  - [Acidanthera](https://github.com/acidanthera)
  - [Hackintosh](https://github.com/daliansky/Hackintosh)
  - [brigadier](https://github.com/corpnewt/brigadier)


   
## 📧 联系方式

如有问题或建议，欢迎联系本项目的作者。

- 邮箱：1551656605@qq.com
- GitHub：https://github.com/bilijp153
- 还可以通过 GitHub 的 [Issues](https://github.com/Aot5223/Hackintosh-for-Xiaomi-Air/issues)功能与我们联系。


## 📄 版权声明
本项目遵循 MIT 开源协议。您可以自由地使用、修改和分发本项目，但请注明出处并保留原始版权声明。详情请参见 [许可证](License) 文件。
 
© 2023 Aot5223.  All rights reserved.
   

