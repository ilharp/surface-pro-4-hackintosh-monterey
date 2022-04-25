# surface-pro-4-hackintosh-big-sur

Surface Pro 4 + Big Sur，无触摸屏/WiFi/蓝牙/摄像头，其他功能完整

## 硬件

组件|描述
-|-
型号|Surface Pro 4 8G 256G
CPU|Intel Core i5-6300U 2.5GHz
显卡|Intel HD Graphics 520 2GB
声卡|Realtek ALC3269（布局 3）
USB 无线网卡|COMFAST CF-811AC（自购）

## 目标对应机型

官方名称|MacBook Pro（13 英寸，2016 年，两个雷雳 3 端口）
-|-
标识符|MacBookPro13,1
部件号|MLL42xx/A、MLUQ2xx/A

## 来源 & 鸣谢

组件|来源于
-|-
[macOS](https://www.apple.com.cn/macos)|[Apple](https://www.apple.com.cn)
[OpenCore](https://github.com/acidanthera/OpenCorePkg)|[acidanthera](https://github.com/acidanthera)
ACPI|[bigsadan/surface-pro-4-hackintosh](https://github.com/bigsadan/surface-pro-4-hackintosh)
键盘 & 触摸板等|[VoodooI2C (基础)](https://github.com/VoodooI2C)，[Xiashangning/BigSurface](https://github.com/Xiashangning/BigSurface)
音频|[AppleALC](https://github.com/acidanthera/AppleALC) + 布局 3
无线网卡驱动|[chris1111/Wireless-USB-Big-Sur-Adapter](https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter)

## 修改的内容

- OpenCore 内核升级到了 [v0.8.0](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.0)

- 优化了 ACPI

- 内置 OpenCore Shell/Resources

- 开启 `SetupVirtualMap`（重要）

- 关闭 `XhciPortLimit`（重要）

- 修改了部分 OS 启动参数，修改 OS 启动 GUI 为中文

## 食用

1. 把 EFI 文件夹粘贴到 U 盘任何一个空分区的根目录里（注意 U 盘文件系统要能够被 Surface UEFI 识别）

1. Surface 进 UEFI，关掉 Boot Lock、Secure Boot 和 TPM 等，引导顺序将 U 盘置首

1. 插上 U 盘，安装 macOS

1. Reset NVRAM（如果某天突然发现有任何功能变得不正常了，在尝试修复之前记得先 Reset NVRAM）

1. 开始愉快的水果之旅

## 注意事项

- 在触摸板设置中关闭 `Force click and haptic feedback`，否则使用起来会有些奇怪（Voodoo 触摸板驱动会把触摸板按下当作 `Force Click`）

## 下载 & 更新记录

请参见 [Releases](https://github.com/ilharp/surface-pro-4-hackintosh-big-sur/releases)

## LICENSE

All files and codes in this repo are **only for archiving**, and their copyright **belongs to the original author**.
