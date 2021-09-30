# surface-pro-4-hackintosh-big-sur

## 硬件

- 型号：Surface Pro 4 8G 256G

- 买了 USB 无线网卡：COMFAST CF-811AC

## 配置

主要使用的项目：[bigsadan/surface-pro-4-hackintosh](https://github.com/bigsadan/surface-pro-4-hackintosh) 和 [chris1111/Wireless-USB-Big-Sur-Adapter](https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter)

## 修改的内容

- OpenCore 内核升级到了 [v0.7.3](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.7.3)，更新了全部内置包，更新了配置文件结构

- 开启了 `AppleXcpmCfgLock`，不过这个开不开都没关系

- 开启了 `SetupVirtualMap`（重要）

- 修改了部分 OS 启动参数，修改 OS 启动 GUI 为中文

## 食用

1. 把 EFI 文件夹粘贴到 U 盘任何一个空分区的根目录里（注意 U 盘文件系统要能够被 Surface UEFI 识别）

1. Surface 进 UEFI，关掉 Boot Lock、Secure Boot 和 TPM 等，引导顺序将 U 盘置首

1. 插上 U 盘，安装 macOS

1. 开始愉快的水果之旅

## 鸣谢

- Apple 的 macOS

- [acidanthera/OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)

- kext 和 aml 作者

- [bigsadan/surface-pro-4-hackintosh](https://github.com/bigsadan/surface-pro-4-hackintosh)

- [chris1111/Wireless-USB-Big-Sur-Adapter](https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter)

## LICENSE

All files and codes in this repo are **only for archiving**, and their copyright **belongs to the original author**.
