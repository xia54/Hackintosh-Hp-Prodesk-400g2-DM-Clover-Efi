# HP PRODESK 400G2 DM黑苹果 EFI

## 我的配置

|         硬件       |                   型号                  | 
|-------------------:|:----------------------------------------|
|               主板 | HP PRODESK 400G2 DM                       |
|                CPU | Intel Core i5-6400                      |
|               显卡 | Intel HD Graphics 530 1536 MB   |
|              硬盘1 | 三星 PM961 256G M2 NVMe                 |
|              硬盘2 | 日立 5400转 500G SATA                |
|               内存1 | 玖合 DDR4 2666Mhz 16G  |
|               内存2 | 枭鲸 DDR4 2666Mhz 16G  |
|        无线 + 蓝牙 | BCM94360HMB 双频 BT4.0 无线网卡 PCI-E   |
|               键盘 | 海盗船 K70 LUX                               |
|               鼠标 | 罗技 G304无线                               |
|            显示器 | 27寸 4K 宏基显示器 H277HK          |


## 折腾日志

2020年6月10日：经网友测试， `Mac mini8,1` 机型可能会在启动输入密码界面掉帧，更换` iMac17,1` 即正常， 如遇到此问题可尝试更改。

2020年5月30日：测试更新15.5，无痛升级。更新关于本机截图。

## 更新注意事项

更新 EFI 之后，第一次进系统最好是带 `-v` 参数启动，否则可能会出现禁止符号，无法启动。如果出现这种情况下，再次启动时，加上 `-v` 参数就可以了。进入系统之后，最好使用 `Hackintool` 重建一下驱动缓存。


## EFI 简介

感谢黑苹果星球会员交流群`@ycvip521`在我安装无果即将自闭之时提供了可安装版本的EFI，此EFI根据原EFI修改而来。


这个 EFI 的特点是使用的是 `Mac mini8,1` 机型，双硬解正常，因已做了 USB 定制，所有 USB 接口都可用。

缺点：

1、使用`VoodooHDA-2.9.2.kext`音量小；使用`AppleALC.kext`自带小喇叭无声。按需食用

2、关于睡眠：其表现为可手动/自动睡眠，但唤醒后黑屏。建议禁用睡眠



Clover 版本为：5107。

Clover 驱动包含：

* ApfsDriverLoader.efi
* CsmVideoDxe.efi
* DataHubDxe.efi
* EmuVariableUefi.efi
* FSInject.efi
* HFSPlus.efi
* SMCHelper.efi

系统驱动包含：

* ACPIBatteryManager.kext
* AirportBrcmFixup.kext
* AppleALC.kext
* BrcmBluetoothInjector.kext
* HibernationFixup.kext
* Lilu.kext
* RealtekRTL8111.kext
* RTCMemoryFixup.kext
* USBPorts.kext
* WhateverGreen.kext
* FakeSMC.kext
* FakeSMC_SMMSensors.kext
* FakeSMC_LPCSensors.kext
* FakeSMC_GPUSensors.kext
* FakeSMC_CPUSensors.kext
* FakeSMC_ACPISensors.kext
## EFI 使用

如果你的配置跟我上面配置相同或兼容，那么你可以直接使用该 EFI 进行安装。安装前请注意，一定要用 `Clover Configurator` 重新生成并替换 `SMBIOS` 部分的内容，否则会因为机器有同一个硬件 ID 而被苹果封锁。生成时，请选择 `Mac mini8,1` 机型。


## 系统截图
![avatar](https://github.com/ylen0l/Hackintosh-Hp-Prodesk-400g2-DM-Clover-Efi/blob/master/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E6%88%AA%E5%9B%BE/%E5%85%B3%E4%BA%8E%E6%9C%AC%E6%9C%BA20200530%E5%AE%9E%E6%B5%8B15.5%402x.png)关于本机

加图片打开太慢了，就留了关于本机，其他截图去`系统状态截图`里面打开看吧
