# HP PRODESK 400G2 DM黑苹果 EFI

## 我的配置

|         硬件       |                   型号                  | 
|-------------------:|:----------------------------------------|
|               主板 | HP PRODESK 400G2 DM                       |
|                CPU | Intel Core i5-6400                      |
|               显卡 | ntel HD Graphics 530 1536 MB   |
|              硬盘1 | 三星 PM961 256G M2 NVMe                 |
|              硬盘2 | 日立 5400转 500G SATA                |
|               内存1 | 玖合 DDR4 2666Mhz 16G  |
|               内存2 | 枭鲸 DDR4 2666Mhz 16G  |
|        无线 + 蓝牙 | BCM94360HMB 双频 BT4.0 无线网卡 PCI-E   |
|               键盘 | 海盗船 K70 LUX                               |
|               鼠标 | 罗技 G304无线                               |
|            显示器 | 27寸 4K 宏基显示器 H277HK          |


## 更新注意事项

更新 EFI 之后，第一次进系统最好是带 -v 参数启动，否则可能会出现禁止符号，无法启动。如果出现这种情况下，再次启动时，加上 -v 参数就可以了。进入系统之后，最好使用 Hackintool 重建一下驱动缓存。


## EFI 简介

感谢黑苹果星球会员交流群@ycvip521在我安装无果即将自闭之时提供了可安装版本的EFI，此EFI根据原EFI修改而来。


这个 EFI 的特点是使用的是 `Mac mini8,1` 机型，双硬解正常，因已做了 USB 定制，所有 USB 接口都可用。

缺点：

1、使用VoodooHDA-2.9.2.kext音量小；使用AppleALC.kext自带小喇叭无声。按需食用

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

如果你的配置跟我上面配置相同或兼容，那么你可以直接使用该 EFI 进行安装。安装前请注意，一定要用 Clover Configurator 重新生成并替换 SMBIOS 部分的内容，否则会因为机器有同一个硬件 ID 而被苹果封锁。生成时，请选择 `Mac mini8,1` 机型。


## 系统截图

![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/%E5%85%B3%E4%BA%8E%E6%9C%AC%E6%9C%BA@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/HWMonitorSMC@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/USB@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/USB%E5%AE%9A%E5%88%B6@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/WIFI@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/%E4%BB%A5%E5%A4%AA%E7%BD%91%E5%8D%A1@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/%E5%8F%98%E9%A2%91@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/%E7%A1%AC%E8%A7%A3@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/%E8%8A%82%E8%83%BD@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/%E8%93%9D%E7%89%99@2x.png)
![avatar](https://gitee.com/xiaojiangshan/hp-prodisk-400g2-dm-efi-for-clover/blob/master/系统截图/音频@2x.png)
