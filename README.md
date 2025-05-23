## Hackintosh 黑苹果长期维护机型 EFI 及安装教程整理

[![img](https://img.shields.io/github/stars/daliansky/Hackintosh.svg?color=ff69b4&label=%E7%82%B9%E8%B5%9E&logoColor=ff69b4&style=social)](https://github.com/daliansky/Hackintosh) [![img](https://img.shields.io/github/followers/daliansky.svg?label=%E7%B2%89%E4%B8%9D&logoColor=success&style=social)](https://github.com/daliansky/Hackintosh) ![img](https://img.shields.io/github/contributors/daliansky/Hackintosh.svg?color=red&label=%E8%B4%A1%E7%8C%AE%E4%BA%BA%E6%95%B0) [![img](https://img.shields.io/github/last-commit/daliansky/Hackintosh.svg?color=orange&label=%E6%9C%80%E8%BF%91%E6%8F%90%E4%BA%A4)](https://github.com/daliansky/Hackintosh)

## English Version: [Hackintosh long-term maintenance model EFI and installation tutorial](README_en.md)

    今天采用关键词OPENCORE搜索的方式，采用最近更新排序，搜索了前10页的维护信息，再筛出未进入清单，但维护得不错得REPO,更新时间只是最近2天得，肯定又很多漏的，一一核对很费精力，readme文档内内容太多，整理了一下思路,列出列出了以下几个点，希望大家一起看看如何整理比较方便。
    
      (1)拆分文档：拆分成笔记本和台式机两份文件,readme文档内将厂商链接过去，这样再更新文件的时候会轻松一些。
    
      (2)自动化脚本：目前更新的方式还是靠人去对，筛出新增的然后再增加进去，比较费时间。从我自己找的方式看，是可以通过脚本实现的，这个可以节省很多时间和精力。
               范围：github.com，
               更新时间：最近3个月，
               限制条件：commit的提交次数大于20次的。（另外的一点将已经在清单里面的去掉,不去也行，直接更换清单）
               其他：排序和合并，排序后需要人工将命名不规范的补齐。
               
      (3)搜索引擎：当然，能够做到一个搜索引擎，专门针对黑苹果优化的，这或许就是这份清单的终点，也就失去了一些意义，变为纯粹的白嫖工具了。
大家有更好的思路也可以提出来，一起完成，虽然我不确定现在继续做这些的意义还有多少。
------
- 黑苹果论坛：

  - **国内** [远景论坛](http://bbs.pcbeta.com)、[威锋论坛](http://bbs.feng.com)
  - **国外** [insanelymac 论坛](https://www.insanelymac.com/forum/)、[tonymacx86 论坛](https://www.tonymacx86.com/)、[德国黑苹果论坛](https://www.hackintosh-forum.de/)、[俄罗斯黑苹果论坛](https://www.applelife.ru)、[法国黑苹果论坛](https://www.hackintosh-montreal.com)、 [osxlatitude 论坛](https://osxlatitude.com/forums/)

- 一些黑苹果常用的软件或者驱动开发者的主页，希望大家能及时更新驱动和软件，驱动需要自己去对应驱动开发者的主页去更新。

- _[RehabMan](https://bitbucket.org/RehabMan/)_ 维护了很多黑苹果驱动和相关补丁
- _[Vit9696](https://github.com/acidanthera)_ lilu 和相关插件、applealc 的主要开发或维护者
- _[Clover 更新地址](https://sourceforge.net/projects/cloverefiboot/)_ Clover 团队更新 clover 的主要发布渠道
- _[常用软件和驱动清单](./LinkList.md)_ 整理了常用软件和驱动的主要发布地址，持续修改……
- **OPENCORE参考文档**[中文版](https://sumingyd.github.io/OpenCore-Post-Install/)、[英文版](https://dortania.github.io/Getting-Started-With-ACPI/)
- [英特尔无线网卡驱动文档](https://openintelwireless.github.io/itlwm/)、[英特尔蓝牙驱动文档](https://openintelwireless.github.io/IntelBluetoothFirmware/)

## 同步更新：[黑果小兵的部落阁](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)


## 机型讨论：[远景 pcbeta.com](http://bbs.pcbeta.com/viewthread-1795904-1-1.html)

<details>
<summary>更新日志</summary>

更新日期：

- 2024年3月4日
  - 新增机型：
    - FEVM FN60G
    - minisforum UM480XT
    - minisforum UM560XT
    - minisforum UM580D/UM590
    - minisforum NAG6

完整的更新日志：[更新日志](./Changelog.md)

</details>

## 目录
笔记本
- [Acer 宏碁](#acer-宏碁)
- [Asus 华硕](#asus-华硕)
- [DELL 戴尔](#dell-戴尔)
- [Gigabyte 技嘉](#gigabyte-技嘉)
- [Hasee 神舟](#hasee-神舟)
- [HP 惠普](#hp-惠普)
- [Huawei 华为](#huawei-华为)
- [Lenovo 联想](#lenovo-联想)
- [LG](#lg)
- [Mechrevo 机械革命](#mechrevo-机械革命)
- [MSI 微星](#msi-微星)
- [Razer Blade 雷蛇](#razer-blade-雷蛇)
- [Samsung 三星](#samsung-三星)
- [Shinelon 炫龙](#shinelon-炫龙)
- [Toshiba 东芝](#toshiba-东芝)
- [XiaoMi 小米](#xiaomi-小米)
- [Intel 英特尔](#intel-英特尔)
- [Other 其它](#other-其它)
- [笔记本更多的机型](#笔记本更多的机型)
- [笔记本相关资源](#笔记本相关资源)

台式机
- [AMD Ryzen](#amd-ryzen)
- [ASRock 华擎](#asrock-华擎)
- [ASUS 华硕](#asus-华硕-1)
- [Dell 戴尔](#dell-戴尔-1)
- [Gigabyte 技嘉](#gigabyte-技嘉-1)
- [HP 惠普](#hp-惠普-1)
- [Intel 英特尔](#intel-英特尔-1)
- [Lenovo 联想](#lenovo-联想-1)
- [minisforum 铭凡](#minisforum-铭凡)
- [MSI 微星](#msi-微星-1)
- [Mini 迷你系列](#mini-迷你系列)
- [台式机其它机型](#台式机其它机型)
- [硬件兼容列表](#硬件兼容列表)

## 笔记本部分机型

### Acer 宏碁

| 机型名称                    | 发布地址                                                     | 教程地址                                                     | 备注                                             |
| --------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ |
| Acer A315-53G               | [链接](https://github.com/hanngoc1406/ACER-A315-53G-Hackintosh-Opencore) |                                                              |                                                  |
| Acer Aspire 5741G | [链接](https://github.com/AlexHackintosh/Acer-Aspire-5741G-High-Sierra) | | |
| Acer Aspire 3 A315-51       | [链接](https://github.com/ZeroInfinityXDA/Acer-A315-51-Hackintosh) |                                                              |                                                  |
| Acer Aspire 3 A315-54K-34P6 | [链接](https://github.com/velickovicdj/A315-54K-34P6_OpenCore_Big_Sur) |                                                              |                                                  |
| Acer Aspire 3 A315-56 | [链接](https://github.com/NaseelNiyas/Acer-a315-56-Opencore) | | |
| Acer Aspire A514-51G        | [链接](https://github.com/yosisetiawan/EFI-Hackintosh-Acer-A514-51G) |                                                              |                                                  |
| Acer Aspire A514-52-37H1    | [链接](https://github.com/samleong123/Acer-Aspire-A514-52-37H1-macOS-Catalina-Clover-EFI) |                                                              |                                                  |
| Acer Aspire A515-51G        | [链接](https://github.com/h-okon/Acer-Aspire-A515-Hackintosh) [链接](https://github.com/AnshulRaghav/Acer-Big-Sur-Hackintosh) |                                                              |                                                  |
| Acer Aspire A515-51G        | [链接](https://github.com/Siddhesh1197/Acer-A515-51G-Hackintosh) | [链接](https://github.com/Siddhesh1197/Acer-A515-51G-Hackintosh/blob/master/README.md) |                                                  |
| Acer Aspire A515-53G-5269 | [链接](https://github.com/TristanListanco/Acer-A515-53G-5269-Opencore-EFI)  |  | |
| Acer Aspire A515-55 | [链接](https://github.com/hanlywijaya/Acer-Aspire-A515-55-Opencore) |  | |
| Acer A515-51G-58VH          |                                                              |                                                              |                                                  |
| Acer A515-52G-58LZ | [链接](https://github.com/tucano3000/ACER-A515-52G-58LZ-HACKINTOSH-OPENCORE) | | |
| Acer A715                   | [链接](https://github.com/WangGang-a1/Acer-A715-EFI)         |                                                              |                                                  |
| Acer Aspire 7 Gaming | [链接](https://github.com/long5436/Ryzentosh-Acer-aspire-7-A715-42G-Opencore-EFI) | | AMD Ryzen 5 5500U |
| Acer Aspire 7 A715-75G-50SA | [链接](https://github.com/AbhaySingh15/Acer-aspire-7-A715-75G-Opencore-EFI) | | |
| Acer Aspire 7 A715-75G-50TA | [链接](https://github.com/ambujs89/acer-aspire-7-A715-75G-50TA-Opencore-EFI)                                                                                                                                     |                                                                                      |                                            |
| Acer Aspire E1-471G         | [链接](https://github.com/matthew728960/Clover-ACER-E1-471G) | [链接](https://github.com/matthew728960/Clover-ACER-E1-471G/blob/master/README.md) | ACER Aspire E1-471g                              |
| Acer Aspire E5-471G         | [链接](https://github.com/THLIVSQAZ/ACER-E5-471G-OpenCore) [链接](https://github.com/THLIVSQAZ/ACER-E5-471G-Clover) |                                                              |                                                  |
| Acer Aspire E5 475G         | [链接](https://github.com/hilmanshini/Acer-Aspire-E5-475G-Clover-Hackintosh) |                                                              |                                                  |
| Acer Aspire E5-476G         | [链接](https://github.com/budhilaw/Acer-E5-476G-Hackintosh) [链接](https://github.com/rockavoldy/Acer-E5-476G-Hackintosh)<br />[链接](https://github.com/temamumtaza/Hackintosh-Catalina-Acer-e5-476g) |                                                              | 链接 1 = i5-8250U; 链接 2 = i3-6006U（OpenCore） |
| Acer Aspire E5-571-5552     | [链接](https://github.com/GaryDoooo/acer_e51_osx)            |                                                              |                                                  |
| Acer Aspire E5-571G         | [链接](https://github.com/daviiid99/Acer-Aspire-E5-571G)     |                                                              |                                                  |
| Acer Aspire E1-571G         | [链接](https://github.com/DiogoSilva48/Acer-E1-571G-Hackintosh) |                                                              |                                                  |
| Acer Aspire E1-572G         | [链接](https://github.com/TonyStark10006/Acer_E1-572G_Hackintosh_EFI) |                                                              |                                                  |
| Acer Aspire E5-575G         | [链接](https://github.com/Davone98/Hackintosh-Acer-Aspire-E5-575G) |                                                              |                                                  |
| Acer Aspire E5-575G-53vg    | [链接](https://github.com/RabinPhaiju/acer-aspire-e5-575g-53vg-EFI)                                                                                                                                              |                                                                                      |                                            |
| Acer Aspire P3-171 | [链接](https://github.com/youheng7185/aspire-p3-171-opencore-efi) | | |
| Acer Aspire V 15 V5-591G    | [链接](https://github.com/kushwavez/acer-aspire-v5-591g-clover-efi) |                                                              |                                                  |
| Acer Aspire V3-371 | [链接](https://github.com/WhosPix3l/Aspire-V3-EFI) | | |
| Acer Aspire VN7-591G        | [链接](https://github.com/zhangyan56/acer-vn7-591G-i5-4210H-macos-10.15.5-EFI) |                                                              |                                                  |
| Acer ES1-572-37pz           | [链接](https://github.com/joodrew/hackintosh-acer-es1-572-37pz) |                                                              |                                                  |
| Acer F5-573G                |                                                              |                                                              |                                                  |
| Acer F5-573G-55PJ           |                                                              |                                                              |                                                  |
| Acer F5-573g-75A3           | [链接](https://github.com/vinicioslc/HACKINTOSH-ACER-F5-573G-75A3) |                                                              |                                                  |
| Acer Nitro 5 AN515-44-R99Q | [链接](https://github.com/myusernameisvista/Acer-Nitro-5-AN515-44-Ryzentosh-EFI) | | AMD Ryzen 5 4600H |
| Acer Nitro 5 AN515-50U2     | [链接](https://github.com/Lojhan/EFI-ASPIRE-5-NITRO-AN515-50U2) |                                                              |                                                  |
| Acer Nitro 5 AN515-52       | [链接](https://github.com/tien191web/Acer-Nitro5-AN515-52-EFIhackintosh) |                                                              |                                                  |
| Acer Nitro 5 AN515-52-593F | [链接](https://github.com/ezyway/EFI-AN515-52-593F) | | |
| Acer Nitro 5 AN515-54       | [链接](https://github.com/jigarpatel7600/Acer-Nitro5)        |                                                              |                                                  |
| Acer Nitro 5 AN515-54-51NJ | [链接](https://github.com/MKC-MKC/Acer_Nitro_5_AN515-54-51NJ-EFI-OpenCore) | | |
| Acer Nitro 5-an515-54-58CL  | [链接](https://github.com/YuryRegis/Acer-Nitro5-AN515-54-58CL) |                                                              |                                                  |
| Acer nitro 5 an517-51       | [链接](https://github.com/SaeedHaidar/Nitro-5-an517-51-Hackintosh) |                                                              |                                                  |
| Acer Nitro 5 an517-51-55NT | [链接](https://github.com/sostenesg7/Nitro5-an517-51-55NT-hackintosh-EFI) | | |
| Acer Predator Helios 300    | [链接](https://github.com/PruvostMaxime/Hackintosh-Predator-300) [链接](https://github.com/KadeReolance/Predator-Helios-300-OpenCore-0.6.2)<br />[链接](https://github.com/suryavamsi6/EFI_Acer_Predator_Helios_300) |                                                              |                                                  |
| Acer Predator G3-571        | [链接](https://github.com/geminis3/Predator-G3-571-OC)       |                                                              |                                                  |
| Acer Swift 3                | [链接](https://github.com/FallenChromium/Acer-Swift3-2018-hackintosh) |                                                              | SF315-51-518S                                    |
| Acer Swift 3 52G            | [链接](https://github.com/geekcjj/Clover-Acer-Swift3-SF315-52G) |                                                              | Acer-Swift3-SF315-52G                            |
| Acer Swift 3 SF314-54       | [链接](https://github.com/diepeterpan/Acer-Swift-3-SF314-54-2018-MacOS-Big-Sur) |                                                              |                                                  |
| Acer Swift 3 SF314-55G      | [链接](https://github.com/cjtim/SF314-55G-hackintosh) [链接](https://github.com/cjtim/SF314-55G-hackintosh) |                                                              | Acer Swift 3 2019 SF314-55G                      |
| Acer Swift 5                | [链接](https://github.com/ghayyem/acer_swift_5_1065g7)       |                                                              | i7-1065G7                                        |
| Acer Veriton D430 Gen4/6    | [链接](https://github.com/SummerEmber/ACER-Veriton-D430-Gen4) [链接](https://github.com/SummerEmber/ACER-Veriton-D430-Gen6) |                                                              |                                                  |
| Acer V3-471G                | [链接](https://github.com/oneveb/Acer-V3-471G)               |                                                              |                                                  |
| Acer V3-572G-51MR           | [链接](https://github.com/AnoldmanLiSir/Acer-V3-572G-51MR)   | [链接](https://github.com/AnoldmanLiSir/Acer-V3-572G-51MR/blob/master/README.md) |                                                  |
| Acer V5-572                 | [链接](https://github.com/7ack/Acer-V5-572-Hackintosh)       | [链接](https://github.com/7ack/Acer-V5-572-Hackintosh/blob/master/readme.md) |                                                  |
| Acer Aspire V5-573P         | [链接](https://github.com/xtrs84zk/Aspire-V5-573P-Hackintosh) |                                                              |                                                  |
| Acer VN7-793g               | [链接](https://github.com/cedric-bour/Acer-VN7-793g-Hackintosh) |                                                              |                                                  |
| Acer-K50-10-525V            | [链接](https://github.com/mingslife/Acer-K50-10-525V-Hackintosh) |                                                              |                                                  |
| Acer VX5-591G           | [链接](https://github.com/Chakid/Acer-VX15-Hackintosh)       |                                                              |            宏碁暗影骑士3                |
| Acer TravelMate P246-MG | [链接](https://github.com/sebasrock156/Acer-TravelMate-P246-MG-OpenCore) | | |
| Acer Travelmate P248     | [链接](https://github.com/jamesciq/Acer-Travelmate-P248-hackintosh-EFI) |                                                           |                             |
| Acer TravelMate TX520-G2-MG | [链接](https://github.com/zqlovezone/ACER-TX520-Hackintosh-Opencore) |                                                              |                                                  |
| Acer P258-MG                | [链接](https://github.com/lgs3137/ACER_P258_MG-macOS)        |                                                              |    |
| Acer A315-55G	|[链接](https://github.com/tkkinn/opencore-a315-55g)	|		|		|
| Acer Aspire VX15	|[链接](https://github.com/dongcodebmt/VX5-591G-OpenCore)	|		|		|

### Asus 华硕

| 机型名称                          | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| --------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Asus A43SJ                        | [链接](https://github.com/badruzeus/Hackintosh-Asus-A43SJ)   | [链接](https://github.com/badruzeus/Hackintosh-Asus-A43SJ/blob/master/README.md) | Asus A43SJ                                                   |
| Asus A411UF                       | [链接](https://github.com/faizauthar12/Asus_A411UF_Hackintosh) |                                                              |                                                              |
| Asus A441-A456 | [链接](https://github.com/DanteHub/hackintool-oc-ASUAA441-A456) | | |
| Asus A442UF                       | [链接](https://github.com/ryansat/Hackintosh-A442UF)         |                                                              |                                                              |
| Asus A442URR                      |                                                              |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Asus A455LA                       | [链接](https://github.com/Semutbanyak/Semutbanyak-Asus-A455LA-WX668D-hackintosh-OpenCore) |                                                              | Asus S455LA                                                  |
| Asus A455LF-WX039D Series         | [链接](https://github.com/asepms92/Hackintosh-Asus-A455LF-Notebook) |                                                              |                                                              |
| Asus A456UF(X456UF)               |                                                              |                                                              |                                                              |
| Asus A550JK4200                   | [链接](https://github.com/hehuapei/ASUS-a550jk-4200---macOS) |                                                              |                                                              |
| Asus F455LD                       | [链接](https://github.com/athlonreg/Asus-F455LD-i5-4210u)    |                                                              |                                                              |
| Asus FL5900U                      | [链接](https://github.com/rjm521/asus-fl5900u-hackintosh-oc) |                                                              |                                                              |
| Asus FX55VD DM001D | [链接](https://github.com/fikriardyant/ASUS-fx553vd-dm001d-hackintosh-OC) | | |
| Asus FX504GE-ES72                 | [链接](https://github.com/MegaStood/Hackintosh-FX504GE-ES72) |                                                              |                                                              |
| Asus FX505GD                      | [链接](https://github.com/kreactnative/hackintosh-mojave-fx505gd) |                                                              | ASUS TUF GAMING FX505GD-BQ071T                               |
| Asus FX505GT | [链接](https://github.com/XIONGBAB/ASUS_FX505_EFI) | |  |
| Asus F556U (X556UQK)              | [链接](https://github.com/systemfaliure/Asus-X556UQK-hackintosh#Asus-f556u-x556uqk---high-sierra-hackintosh) | [链接](https://github.com/systemfaliure/Asus-X556UQK-hackintosh/blob/master/README.md) | Asus F556U (X556UQK)                                         |
| Asus FX50J                        | [链接](https://github.com/Xc2333/Hackintosh-Asus-FX50J)      |                                                              |                                                              |
| Asus FX50V                        | [链接](https://github.com/Cyberhan123/Hackintosh-ASUS--FX50V) |                                                              |                                                              |
| Asus FX86FE（FX505GE）                 | [链接](https://github.com/EricCui2333/FX86FE-OpenCore-0.5.5) |                                                              |                                                              |
| Asus FX533VD                      |                                                              |                                                              |                                                              |
| Asus GL503GE                      | [链接](https://github.com/Bimoaryo5/ASUS-GL503GE-Hackintosh-master) |                                                              |                                                              |
| Asus FX86FE（飞行堡垒 6）         | [链接](https://github.com/MEMUZE-Hackintosh/ASUS-FX86FE-OC) [链接](https://github.com/1260839205/FX86FE-OC-EFI) |                                                              |                                                              |
| Asus GL551JW                      | [链接](https://github.com/zacharyrs/GL551JW-Hackintosh)      |                                                              |                                                              |
| Asus GL552VW                      | [链接](https://github.com/originman521/Hackintosh-ASUS-FXPRO-GL552VW) [链接](https://github.com/Armageddon95/ASUS-GL552VW-OC-EFI) |                                                              | 飞行堡垒 2016 FXPRO                                          |
| Asus G60VW                        |                                                              |                                                              |                                                              |
| Asus K501LB                       | [链接](https://github.com/ApolloRisky/EFI_Clover-Asus-K501LB-Mojave) |                                                              |                                                              |
| Asus K550J | [链接](https://github.com/BrandTime/Asus-K550J-Hackintosh) | | |
| Asus K555UB Series                | [链接](https://github.com/sutsurup/ASUS-K555UB-Hackintosh)   | [链接](https://github.com/sutsurup/ASUS-K555UB-Hackintosh/blob/master/README.md) | XO092T - XO093T - XO096T - XO097T<br />XO066T - XO198T - XO266T - XO099D - XO227D |
| Asus K55VD                        | [链接](https://github.com/southernvevo/Asus-K55VD-HACKINTOSH) | [链接](https://github.com/southernvevo/Asus-K55VD-HACKINTOSH/blob/master/README.md) | Asus K55VD                                                   |
| Asus K555LD                       | [链接](https://github.com/kongbg/asus-k555ld-4210U)          | [链接](https://github.com/kongbg/asus-k555ld-4210U/blob/master/README.md) | Asus K555LD                                                  |
| Asus VivoBook M413IA | [链接](https://github.com/AppleOSX/M413IA) |  | R5-4500U |
| Asus N550JK                       | [链接](https://github.com/AlirezaTheH/asus-n550jk-hackintosh) |                                                              |                                                              |
| Asus N550JV                       | [链接](https://github.com/bakedpotato191/asusn550jv-hackintosh) |                                                              |                                                              |
| Asus N551JK                       | [链接](https://github.com/basett1/Asus-N551JK-OC-EFI)        |                                                              |                                                              |
| Asus Laptop N56VZ                 | [链接](https://github.com/signxer/N56VZ-Hackintosh)          |                                                              |                                                              |
| Asus P8P67 PRO                    | [链接](https://github.com/rafaelmaeuer/Asus-P8P67Pro-Hackintosh) | [链接](https://github.com/rafaelmaeuer/Asus-P8P67Pro-Hackintosh/blob/master/readme.md) |                                                              |
| Asus R414U                        |                                                              | [链接](https://github.com/LHB6540/Asus-R414-Hackintosh-10.15.4) | 10.13&10.15                                                  |
| Asus ROG GL502VSK                 | [链接](https://github.com/bursonz/ASUS-ROG-Strix-S5-GL502VSK-Hackintosh) |                                                              |                                                              |
| Asus ROG Strix G15 G512LU         | [链接](https://github.com/MahdiBM/OpenCoreHackintoshEFI)     |                                                              |                                                              |
| Asus ROG Strix G15 - G512LV       | [链接](https://github.com/ehinium/Asus-ROG-Strix-G15-G512LV-OpenCore) |                                                              | i7 10750H                                                    |
| Asus ROG GL552JX                  | [链接](https://github.com/javanesse/Asus-ROG-GL552JX-High-Sierra-10.13-Hackintosh) |                                                              | Asus ROG GL552JX                                             |
| Asus ROG GL552VX                  | [链接](https://github.com/xuanquydsr/Gl552VX-Mojave) [链接](https://github.com/ifuncoding/EFI-OC-ROG-gl552vx) |                                                              |                                                              |
| Asus ROG GL553VD                  | [链接](https://github.com/MohammadtaghiFarkhondekar/macOS-Mojave-For-Asus-ROG-GL553VD) |                                                              |                                                              |
| Asus ROG Strix Hero II GL504GM    | [链接](https://github.com/664235822/EFI-OpenCore)            |                                                              | 华硕玩家国度 ROG 魔霸 2                                      |
| Asus ROG X13 Flow | [链接](https://github.com/zabdottler/ROG-X13-Flow-hackintosh) | | 华硕幻 13 AMD Ryzen 9 5900HS |
| Asus ROG Zephyrus M GM501GS       | [链接](https://github.com/kylergib/Asus-Zephyrus-M-gm501gs-Mojave) |                                                              |                                                              |
| Asus ROG Zephyrus M15 GU502LW     | [链接](https://github.com/RmondJone/ROG-Zephyrus-M15-Hackintosh-GU502LW) |                                                              | 华硕玩家国度幻15                                             |
| Asus ROG Zephyrus S GX531GS       |                                                              |                                                              | 华硕玩家国度冰刃 3                                           |
| Asus ROG-Zephyrus-G14-GA401(2020-2021) | [链接](https://github.com/PIut02/ROG-Zephyrus-G14-GA401-Hackintosh) | | 华硕幻14<br />AMD Ryzen 7 4800HS/5800HS |
| Asus ROG GL703ge                  |                                                              |                                                              |                                                              |
| ASUS ROG GL753VD | [链接](https://github.com/namxg6626/Asus-GL753VD-hackintosh-opencore) | | |
| Asus ROG Strix G17 G712LW | [链接](https://github.com/tueminh192/Asus-g712lw-prebuilt-efi) | | |
| Asus ROG GX701                    | [链接](https://github.com/laeo/hackintosh-rog-gx701-efi)     |                                                              |                                                              |
| Asus S4000VA                      | [链接](https://github.com/stonexing/Asus-S4000VA8550-Hackintosh) |                                                              | 华硕灵耀 i7-8550U                                            |
| Asus S4100V                       | [链接](https://github.com/loong1992/Asus_S4100VN8250U_Hackintosh) |                                                              |                                                              |
| Asus S510UQ                       | [链接](https://github.com/KINGKONG2808/Hackintosh_ASUSS510UQ) [链接](https://github.com/JoK3rLeE/Asus-S510UQ-BQ178T) |                                                              | Asus VivoBook S150UQ-BQ178T                                  |
| Asus S5300FN                      | [链接](https://github.com/Jie2GG/Hackintosh-ASUS-S5300FN)    |                                                              | 华硕灵耀 2 代                                                |
| Asus S530UN                       | [链接](https://github.com/tunglamvghy/AsusS530UN-hackintosh) |                                                              |                                                              |
| Asus TP300LD                      | [链接](https://github.com/danang-id/ASUS-TP300LD-ESP)        |                                                              |                                                              |
| Asus TP412FA | [链接](https://github.com/danang-id/ASUS-TP412FA-ESP) | | |
| Asus TUF Gaming FX504             | [链接](https://github.com/PoomSmart/Asus-FX504GE-Hackintosh) [链接](https://github.com/angeljavan/AUSU-FX80GE-FX504Ge-efi) | [链接](https://github.com/PoomSmart/Asus-FX504GE-Hackintosh/blob/master/README.md) | 华硕 FX80GE FX504GE                                          |
| Asus TUF 505GE                    | [链接](https://github.com/SonHai32/TUF_505GE_EFI_OC_0.6.6_SP_BigSur) |                                                              |                                                              |
| Asus TUF 15 FX506L                | [链接](https://github.com/VGerris/asus-tuf-15-opencore)      |                                                              |                                                              |
| Asus UX32VD | [链接](https://github.com/rafaelmaeuer/Asus-UX32VD-Hackintosh) | | |
| Asus UX461UA                      | [链接](https://github.com/UdaraWanasinghe/Asus-UX461UA-OpenCore-EFI) |                                                              |                                                              |
| Asus UX501JW                      | [链接](https://github.com/firefly917/Hackintosh_Asus-UX501JW_Mojave) |                                                              |                                                              |
| Asus VivoBook 15 X510UQ / S5100UQ | [链接](https://github.com/wishayne/hackintosh-Asus-S5100UQ-X510UQ) |                                                              |                                                              |
| Asus Vivobook S13 S330FN          | [链接](https://github.com/deniro98/s330fn)                   |                                                              |                                                              |
| Asus X441U                        | [链接](https://github.com/Bach0409/EFI-Asusx441u)            |                                                              | 华硕 adol I330FN                                             |
| Asus X441UA-GA348T | [链接](https://github.com/nu99etz/ASUS-X441UA-GA348T-Hackintosh-EFI-OpenCore) | |  |
| Asus X441UB                       |                                                              |                                                              |                                                              |
| Asus X411UF | [链接](https://github.com/itsluquis/ASUS-S14-X411-OpenCore) | | |
| Asus X441UV                       | [链接](https://github.com/MinorityCode/asus-x441uv-hackintosh-files) |                                                              |                                                              |
| Asus VivoBook A412F | [链接](https://github.com/lay870/EFI-OC-Monterey-ASUS-VivoBook-A412F) | | |
| Asus A442URR                      |                                                              |                                                              |                                                              |
| Asus VivoBook FL8000u             | [链接](https://github.com/jacid233/hackintosh-for-fl8000u)   |                                                              |                                                              |
| Asus VivoBook FL8000UQ            | [链接](https://github.com/alexanderkin/ASUS-FL8000UQ-Hackintosh/releases) | [链接](https://github.com/alexanderkin/ASUS-FL8000UQ-Hackintosh) | ASUS FL8000UQ i7-8550U GeForce 940MX                         |
| ASUS VivoBook FL8700JP            | [链接](https://github.com/bilijp153/ASUS-VivoBook-FL8700JP-Hackintosh) |                                                              |                                                              |
| Asus VivoBook Max X441UVK         | [链接](https://alfinauzikri.github.io/Asus-Vivobook-Max-X441UVK-Hackintosh/) |                                                              |                                                              |
| ASUS Vivobook Pro 15 N580GD | [链接](https://github.com/Iwantwater1116/EFI_Hackintosh_ASUS_VivoBook_Pro_15_N580GD_OC7.3) | | |
| Asus VivoBook S15 S510UA          | [链接](https://github.com/tctien342/Asus-Vivobook-S510UA-High-Sierra-10.13-Hackintosh) | [链接](https://github.com/tctien342/Asus-Vivobook-S510UA-High-Sierra-10.13-Hackintosh/blob/master/README.md) | Vivobook S510UA                                              |
| Asus Vivobook S530UA BQ100T       | [链接](https://github.com/superzeldalink/Asus-Vivobook-S530-hackintosh) |                                                              |                                                              |
| Asus Vivobook S510UNR - BQ114     | [链接](https://github.com/dayfly/Asus-S510UN-EFI)            |                                                              |                                                              |
| Asus VivoBook S510UQ-BQ178T       | [链接](https://github.com/JoK3rLeE/Asus-S510UQ-BQ178T)       |                                                              |                                                              |
| Asus VivoBook X510UQR             | [链接](https://github.com/nguyentrucxinh/Asus-VivoBook-X510UQR-Hackintosh) | [链接](https://github.com/nguyentrucxinh/Asus-VivoBook-X510UQR-Hackintosh/blob/master/README.md) |                                                              |
| Asus VivoBook X509FA              | [链接](https://github.com/chuquoctuan2704/Asus_vivobook_X509FA_EFI_OC) |                                                              |                                                              |
| Asus VivoBook X509FB              | [链接](https://github.com/Miracle-Sakuno/Asus-VivoBook-X509FB-Hackintosh) |                                                              |                                                              |
| Asus Vivobook X515JA | [链接](https://github.com/Bhavinjain260/Asus-Vivobook15-X515JA-Opencore) | | |
| Asus VivoBook Y5000U (X507UBR)    | [链接](https://github.com/lgs3137/ASUS_Y5000U_X507UBR-macOS) |                                                              |                                                              |
| Asus W419LD                       | [链接](https://github.com/Yasin27878/Hackintosh-ASUS-W419LD) |                                                              |                                                              |
| Asus X45C                         | [链接](https://github.com/ipang-dwi/efi-high-sierra)         |                                                              |                                                              |
| Asus X450JB                       | [链接](https://github.com/xiaoMGitHub/Asus_X450JB_Hackintosh) |                                                              |                                                              |
| Asus X455LA                       | [链接](https://github.com/FajarBaiz/X455LA-EFI-HACKINTOSH)   |                                                              |                                                              |
| Asus X455LJ                       | [链接](https://github.com/umarhadi/asus-x455lj-mojave)       |                                                              |                                                              |
| Asus X540LJ                       | [链接](https://github.com/shammu2bd/Asus-X540LJ-Hackintosh-OpenCore) |                                                              |                                                              |
| Asus X542u                        | [链接](https://github.com/nguyencuongit96/efi-asus-x542-hackintosh) |                                                              |                                                              |
| Asus X542UN                       | [链接](https://github.com/yCatDev/asus_x542un-hackintosh)    |                                                              |                                                              |
| Asus X550JX                       | [链接](https://github.com/gaoliang/Asus-X550JX-Hackintosh)   |                                                              |                                                              |
| Asus X550VC                       |                                                              |                                                              |                                                              |
| Asus X550VX                       | [链接](https://github.com/lramadhan/hackintosh-asus-x550vx)  |                                                              |                                                              |
| Asus X550VXK                      | [链接](https://github.com/Giovix92/efi_x550vxk)              |                                                              |                                                              |
| Asus X555LB                       | [链接](https://github.com/emre1393/Asus-x555lb-mojave-efi)   |                                                              |                                                              |
| Asus X555UA                       | [链接](https://github.com/trinhdvt/OpenCore-EFI)             |                                                              |                                                              |
| Asus X555UQ                       | [链接](https://github.com/loyio/Asus-X555UQ-hackintosh)      |                                                              | 网卡使用博通 BCM94360HMB,OC 支持 Big Sur                     |
| Asus X556UAK                      | [链接](https://github.com/sumukshashidhar/asus-x556-uak-efi-configuration) |                                                              |                                                              |
| Asus X556UJ                       | [链接](https://github.com/milanista18/ASUSX556UJ)            |                                                              |                                                              |
| Asus X556UQ                       | [链接](https://github.com/IlhamSevensky/ASUS-X556UQ-HACKINTOSH) |                                                              | A556U                                                        |
| Asus X556UV                       | [链接](https://github.com/Amview/ASUS-X556UV-Hackintosh)     |                                                              |                                                              |
| Asus X75VC-TY056D                 | [链接](https://github.com/Jesterjke/ASUS-X75VC-Hackintosh)   |                                                              |                                                              |
| Asus X751LJ                       |                                                              |                                                              |                                                              |
| Asus ZenBook 系列                 | [链接](https://github.com/hieplpvip/Asus-ZENBOOK-HACKINTOSH) | [链接](https://www.tonymacx86.com/threads/guide-Asus-zenbook-using-clover-uefi-hotpatch.257448/) | 支持型号: UX310 - UX330 - UX330<br />UX410 - UX430 - UX430   |
| Asus ZenBook Flip UX360UAK        | [链接](https://github.com/Frizz925/UX360UAK-Hackintosh)      | [链接](https://github.com/Frizz925/UX360UAK-Hackintosh/blob/master/README.md) |                                                              |
| Asus ZenBook UX32VD               | [链接](https://github.com/rafaelmaeuer/Asus-UX32VD-Hackintosh) | [链接](https://github.com/rafaelmaeuer/Asus-UX32VD-Hackintosh/blob/master/readme.md) | Asus UX32VD                                                  |
| Asus ZenBook UX305FA              | [链接](https://github.com/nganhquoc95/clover-ux305fa) [链接](https://github.com/lehoa1806/UX305FA-OpenCore) |                                                              |                                                              |
| Asus ZenBook UX305UA              | [链接](https://github.com/aryamawb/asus-ux305ua-hackintosh)  |                                                              |                                                              |
| Asus ZenBook UX330UAK             | [链接](https://github.com/Rybo713/UX330UA-macOS)             | [链接](https://github.com/Rybo713/UX330UA-macOS/blob/master/README.md) | Asus UX330UAK (Kabylake）                                    |
| Asus Zenbook UX331                | [链接](https://github.com/VortexisTV/Asus-Zenbook-UX331-Hackintosh) |                                                              |                                                              |
| Asus Zenbook UX433FN              | [链接](https://github.com/letanga/UX433FN-OpenCore-EFI)      |                                                              |                                                              |
| Asus Zenbook UX450FDX             | [链接](https://github.com/xvAcid/Hackintosh_Zenbook_UX450FDX) |                                                              |                                                              |
| Asus Zenbook UX463F | [链接](https://github.com/MSzturc/ASUS-Zenbook-Flip-UX463-OpenCore) | | |
| Asus Zenbook 3 UX490              | [链接](https://github.com/VillenaDeveloper/asus-ux490-hackintosh) |                                                              |                                                              |
| 华硕 zx50jx4200                   | [链接](https://github.com/sxz799/zx50jx4200_hackintosh)      |                                                              |                                                              |
| 华硕 A407UB                       | [链接](https://github.com/xinguisoft/Hackintosh-EFI-Asus-A407UB/) |                                                              |                                                              |
| 华硕玩家国度 ROG 魔霸 2           | [链接](https://github.com/664235822/EFI-OpenCore)            |                                                              |                                                              |
| 华硕玩家国度枪神 3                | [链接](https://github.com/DongLinghe/ROG-SCAR-III-Hackintosh-EFI) |                                                              |                                                              |
| 华硕玩家国度 ROG 魔霸 3           | [链接](https://github.com/JOJOJ812/G531-hackintosh)          |                                                              |                                                              |

### DELL 戴尔

| 机型名称                                   | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Alienware 外星人更多机型**               | [链接](https://github.com/RockJesus/Alienware-Hackintosh)    |                                                              | 引用自：RockJesus 维护的仓库                                 |
| Alienware 17 R4 i7-7700HQ                  | [链接](https://github.com/RockJesus/Alienware-17-R4-I7-7700HQ-MacOS-High-Sierra) | [链接](https://github.com/RockJesus/Alienware-17-R4-I7-7700HQ-MacOS-High-Sierra/blob/master/README.md) | 外星人 17 R4，网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Alienware Aurora-R7                        | [链接](https://github.com/jianghaizhi/DELL-Alienware-Aurora-R7-macOS) |                                                              |                                                              |
| Alienware-Aurora-R6/R7/R8                  | [链接](https://github.com/jianghaizhi/DELL-Alienware-Aurora-R7-macOS) |                                                              |                                                              |
| Alienware M15R2 | [链接](https://github.com/wfx1024/Alienware-M15-ALW15M-D4501B-hackintosh-opencore) | | |
| Dell Latitude E7440                        | [链接](https://github.com/ameeno/Dell-E7440-Hackintosh)      |                                                              |                                                              |
| Dell G3 3500                               | [链接](https://github.com/Baio1977/EFI-Varie-Hackintosh/tree/main/EFI%20Laptop%20/DELL/G3%2015%203500%20i7-10750h) |                                                              |                                                              |
| Dell G3 3579                               | [链接](https://github.com/tonyleelyy/OpenCore-Hackintosh-Dell-G3-3579) [链接](https://github.com/MicalShow/DELL-G3-3579-Opencore-Big-Sur) [链接](https://github.com/VersionZKP2356/Dell-G3-3579-OpenCore-Boot-File) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell G3 3590                               | [链接](https://github.com/shadowsss/hackintosh-Dell-3590)    |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell G3 3779                               | [链接](https://github.com/djlucas123456/Dell-G3-3779-Mojave-Catalina-Clover-) |                                                              |                                                              |
| Dell G5 5500                               | [链接](https://github.com/Forever331/Dell_G5_5500_Hackintosh_OpenCore) |                                                              |                                                              |
| Dell G5 5587                               | [链接](https://github.com/Sosueyakiko/Clover_EFI-For-DELL-G5-5587) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com)； |
| Dell G7 7588                               | [链接](https://github.com/geraldoandradee/Hackintosh-Dell-G7-7588) [链接](https://github.com/flyfeng2002/FYQ-Hackintosh) [链接](https://github.com/Juan-VC/Hackintosh-macOS-Dell-G7-7588) [链接](https://github.com/aksm-unmei/g7-7588-hackintosh) |                                                              | 网卡推荐: DW1560 (BCM94352Z芯片組), Fenvi BCM94352Z / BCM94360NG                              |
| Dell Inspiron 14 5447                      | [链接](https://github.com/SinhLv/Dell-Ins-14-5447-hackintosh) | [链接](https://github.com/SinhLv/Dell-Ins-14-5447-hackintosh/blob/master/README.md) | Dell-Ins-14-5447                                             |
| Dell Inspiron 14 7447                      | [链接](https://github.com/Am1nCmd/Dell-Inspiron-14-7447-Pandora-Hackintosh) | [链接](https://github.com/Am1nCmd/Dell-Inspiron-14-7447-Pandora-Hackintosh/blob/master/README.md) | Dell-Inspiron-14-7447                                        |
| Dell Inspiron 15 7000 (i7-8550U)           | [链接](https://github.com/athlonreg/Dell-Inspiron-15-7000-i7-8550u) |                                                              |                                                              |
| Dell Inspiron 3421                         | [链接](https://github.com/LocTran016/EFI)                    |                                                              |                                                              |
| Dell Inspiron 3442                         | [链接](https://github.com/kkzzhizhou/Dell-3443-Hackintosh)   | [链接](https://github.com/kkzzhizhou/Dell-3443-Hackintosh/blob/master/README.md) | Dell 3443                                                    |
| Dell Inspiron 3443                         | [链接](https://github.com/kkzzhizhou/Dell-3443-Hackintosh)   |                                                              |                                                              |
| Dell Inspriron 3459 | [链接](https://github.com/DUr3n/Dell-3459-OC) | | |
| Dell Inspriron 14 3467                     | [链接](https://github.com/b4iterdev/opencore-dell-inspriron-14-3467) |                                                              |                                                              |
| Dell Inspiron 3481                         | [链接](https://github.com/M3ggy-NX/Dell-Inspiron-3481-EFI-Opencore) |                                                              |                                                              |
| Dell Inspiron 3543                         | [链接](https://github.com/meikeeit/Hackintosh_Dell3543)      |                                                              |                                                              |
| Dell Inspiron 3559                         | [链接](https://github.com/WenQinghua/dell-Inspiron-3559-EFI) |                                                              |                                                              |
| Dell Inspiron 15 3567                      | [链接](https://github.com/osx86-ijb/Dell-Inspiron-15-3567-7th-Gen-Core-i3-7100u-macOS-BigSur) |                                                              |                                                              |
| Dell Inspiron 3568                         | [链接](https://github.com/YGQ8988/dell-3568)                 | [链接](https://github.com/YGQ8988/dell-3568)                 | Dell Inspiron 3568                                           |
| Dell Inspirion 15 3576                     | [链接](https://github.com/rootpx404/Dell-Inspirion-15-3576-OPenCore-efi) |                                                              |                                                              |
| Dell Inspiron 3583                         | [链接](https://github.com/Dhroko/HackintoshDell3583)         |                                                              |                                                              |
| Dell Inspiron 3647 | [链接](https://github.com/renanjoppert1/EFI_DELL_INSPIRON_3647_I5) | | |
| Dell Inspiron 3670                         | [链接](https://github.com/gopnikak47/Vostro3670_OpenCore)                                                             |                                                              |                                                              |
| Dell Inspiron 15R N5110 | [链接](https://github.com/Doregon/Inspiron-N5110-SNDB-Hackintosh) | | |
| Dell Inspiron 5370                         | [链接](https://github.com/dreamwhite/dell-inspiron-5370-hackintosh) |                                                              |                                                              |
| Dell Inspiron 14 5400 2-in-1               | [链接](https://github.com/robmagario/DELL-Inspiron-14-5400-2-in-1-LAPTOP-EFI) |                                                              | i3-1005G1                                                    |
| Dell Inspiron 5420                         | [链接](https://github.com/jasper-wan/Dell-Inspiron-5420-Hackintosh) |                                                              |                                                              |
| Dell Inspiron 5447                         | [链接](https://github.com/SinhLv/Dell-Ins-14-5447-hackintosh) [链接](https://github.com/Jay-Wang-zechong/inspiron-14-5447-hacintosh-EFI-clover) |                                                              |                                                              |
| Dell Inspiron 5458 | [链接](https://github.com/icarolim/efi-Dell5458-OC-Monterey) | | |
| Dell Inspiron 5459                         | [链接](https://github.com/lzhoang2601/Dell-Insprison-5459-Hackintosh) [链接](https://github.com/juanxcueva/Dell-inspiron-5459-EFI) |                                                              |                                                              |
| Dell Inspiron 5488                         | [链接](https://github.com/daggeryu/DELL-inspiron-5488)       |                                                              |                                                              |
| Dell Inspiron 5491 2in1                    | [链接](https://github.com/Speeedo83/Dell-Inspiron-5491-2in1-Hakintosh) |                                                              |                                                              |
| Dell Inspiron 5493 / 5593 | [链接](https://github.com/xzz024/OC7.1-EFI-For-Dell-5593-Bigsur) | | |
| Dell Inspiron 5537                         | [链接](https://github.com/thedeadfish59/Dell_Inspiron_5537-Hackintosh) |                                                              |                                                              |
| Dell Inspiron 5548(4528S)                  | [链接](https://github.com/yuppiesnotzhuhao/Hackintosh-Dell-Inspiron-5548) |                                                              |                                                              |
| Dell Inspiron 5557                         | [链接](https://github.com/Mr-Zhang-1/dell5557-bigsur-OC)     |                                                              | i5-6200U 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell Inspiron 5558                         | [链接](https://github.com/jance-hui/DELL-5558-EFI)           |                                                              |                                                              |
| Dell Inspiron 5559                         | [链接](https://github.com/YuZhangWang/Dell-Inspiron-i5-5559-Clover) |                                                              | Dell 5559                                                    |
|  |  | |  |
| Dell Inspiron 5566                         | [链接](https://github.com/matheusliraofficial/inspiron-5566-hackintosh) |                                                              |                                                              |
| Dell Inspiron 5567                         | [链接](https://github.com/MuntashirAkon/HackintoshDellInspiron5567) |                                                              | i3-7100u, Intel HD620                                        |
| Dell Inspiron 15-5567                         | [链接](https://github.com/DellZHackintosh/Dell-Inspiron-5567-OpenCore) |                                                              |                                                              |
| Dell Inspiron 5570                         | [链接](https://github.com/Mateo1234454545/Dell-5570-hackintosh) [链接](https://github.com/stayboogy/Hackintosh_Dell-Inspiron-5570_Catalina) |                                                              |                                                              |
| Dell Inspiron 5577                         | [链接](https://github.com/imAmouse/Clover-EFI-For-Dell-5577) |                                                              |                                                              |
| Dell Inspiron 5579 | [链接](https://github.com/trytosleep-354/Dell-Inspiron5579-2in1-Laptop-Hackintosh-BigSur11.1) | | |
| Dell Inspiron 5584                         | [链接](https://github.com/Hackintoshlifeit/DELL-Inspiron-5584) |                                                              |                                                              |
| Dell Inspiron 5593 | [链接](https://github.com/xzz024/OC7.1-EFI-For-Dell-5593-Bigsur) | | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell Inspiron 5680                         | [链接](https://github.com/EulerBlind/Dell-5680-EFI) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com)； |
| Dell Inspiron 7348                         | [链接](https://github.com/MoozIiSP/dell-7348-hackintosh)     |                                                              |                                                              |
| Dell Inspiron 7391                         | [链接](https://github.com/NotMexican/Dell-Inspiron-7391-Opencore-EFI) |                                                              |                                                              |
| Dell Inspiron 14 7447 Pandora              | [链接](https://github.com/Am1nCmd/Dell-Inspiron-14-7447-Pandora-Hackintosh) |                                                              |                                                              |
| Dell Inspiron 7460 和 7560                 | [链接](https://github.com/xzhih/dell-7460-7560-hackintosh) [链接](https://github.com/HowieHye/Dell-7460-Hackintosh-OC)<br />[链接](https://github.com/allinu/Dell-7560-OC) | [链接](https://github.com/xzhih/dell-7460-7560-hackintosh/blob/master/README.md) | 戴尔 7460 和 7560，网卡推荐：[DW1820A](https://hackintosher.taobao.com)<br /> |
| Dell Inspiron 7472                         | [链接](https://github.com/ic005k/DELL7472)                   |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Dell Inspiron 7472/7572                    | [链接](https://github.com/lyngogogog/Dell-7472-7572-Hackintosh-EFI) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell Inspiron 7501 | [链接](https://github.com/jamieernest/Dell-Inspiron-7501-Hackintosh) | | 网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| Dell Inspiron 7537                         | [链接](https://github.com/Abbasm234/Dell-Inspiron-7537-Opencore-EFI) [链接](https://github.com/mino389/opencore-EFI-for-dell-7537-4210u-haswell) |                                                              |                                                              |
| Dell Inspiron 7548                         |                                                              |                                                              |                                                              |
| Dell Inspiron 7559                         | [链接](https://github.com/JiangHoumin/Dell_G3_3579_Hackintosh) <br />[链接](https://github.com/fengwenhua/dell-7559-hackintosh) [链接](https://github.com/worship76/dell7559_Hackintosh_BigSur) |                                                              | Dell 7559，网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell Inspiron 7560                         | [链接](https://github.com/ashishcomputing/Dell-Inspiron-7560-Hackintosh-Opencore) |                                                              |                                                              |
| Dell Inspiron 7567                         | [链接](https://github.com/Doapeat/Dell7567) [链接](https://github.com/osx86-ijb/osx86-ijb-Dell-Inspiron-15-7567-macOS-BigSur)<br />[链接](https://github.com/seathasky/Dell-Inspiron-7567-OC) [链接](https://github.com/mishailovic/Hackintosh-Dell-7567-OpenCore_Monterey) | [链接](https://github.com/mishailovic/Hackintosh-Dell-7567-OpenCore_Monterey/blob/main/README.md)                                                             |                                                              |
| Dell Inspiron 7570                         | [链接](https://github.com/duongle305/Dell-7570-Hackintosh)   |                                                              |                                                              |
| Dell Inspiron 7577                         | [链接](https://github.com/yakimka/Hackintosh-Dell-7577) [链接](https://github.com/lersy/Dell-7577-Hackintosh-macos-Opencore) |                                                              |                                                              |
| Dell Inspiron 7580 | [链接](https://github.com/queensferryme/Hackintosh-Dell-7580) [链接](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580) | | 链接1和链接2支持`Big Sur`|
| Dell Inspiron 7586 | [链接](https://github.com/hacker1024/Dell-Inspiron-7586-Hackintosh) | | |
| Dell Inspiron 7590                         | [链接](https://github.com/lcyf9102s/dell-inspiron7590-i5-1050-hackintosh-cloverEFI) [链接](https://github.com/Pinming/Dell-Inspiron-7590-Hackintosh-Opencore)  <br /> [链接](https://github.com/vcvvvc/Dell-Inspiron-7590-Ventura) [链接](https://github.com/vcvvvc/Dell-Inspiron-7590-Monterey) |                                                              | 链接 2 支持`Big Sur` 链接 3 支持`Ventura` 链接 4 支持`Monterey`                                        |
| Dell Inspiron 7591                         | [链接](https://github.com/tctien342/Dell-Inspiron-7591-Hackintosh) [链接](https://github.com/Skimige/Inspiron-759x-Hackintosh) [链接](https://github.com/Pinming/Dell-Inspiron-7590-Hackintosh-Opencore) |                                                              | 链接 3 支持`Big Sur`                                         |
| Dell Latitude 3400 | [链接](https://github.com/davidfreitas-dev/EFI-Dell-Latitude-3400) | | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell Latitude 3410 | [链接](https://github.com/WHCMrShi/Dell-Latitude-3410_Hackintosh) | |  |
| Dell Latitude 3440                         | [链接](https://github.com/Yash-Garg/OpenCore-Latitude3440-EFI) |                                                              |                                                              |
| Dell Latitude 5175 | [链接](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc) | | |
| Dell Latitude E5270                        | [链接](https://github.com/ijiki16/Dell-Latitude-E5270-OpenCore) |                                                              |                                                              |
| Dell Latitude 5300 | [链接](https://github.com/ahianf/dell-latitude-5300-hackintosh) | | |
| Dell Latitude 5310 | [链接](https://github.com/daniel-pro/Latitude-5310-EFI) | | |
| Dell Latitude 5411                         | [链接](https://github.com/MokkaSchnalle/macOS-Dell-5411-5511) |                                                              |                                                              |
| Dell Latitude 5511                         | [链接](https://github.com/MokkaSchnalle/macOS-Dell-5411-5511) |                                                              |                                                              |
| Dell Latitude E5270                        | [链接](https://github.com/ijiki16/Dell-Latitude-E5270-OpenCore) |                                                              |                                                              |
| Dell Latitude E5280                        | [链接](https://github.com/xx569029747/EFI-For-Dell-Latitude-5280) |                                                              |                                                              |
| Dell Latitude E5290                        | [链接](https://github.com/laelsirus/Dell-Latitude-5290-2-in-1-UHD620-iGPU-CLOVER) | [链接](https://github.https://github.com/laelsirus/Dell-Latitude-5290-2-in-1-UHD620-iGPU-CLOVER/blob/master/README.md) | Dell-Latitude-5290                                           |
| Dell Latitude 5290 2-in-1                  | [链接](https://github.com/laelsirus/Dell-Latitude-5290-2-in-1-UHD620-iGPU-CLOVER) |                                                              |                                                              |
| Dell Latitude 5300 | [链接](https://github.com/ahianf/dell-latitude-5300-hackintosh) | | |
| Dell Latitude E5400                        | [链接](https://github.com/gouiferda/dell-5400-hackintoch)    |                                                              |                                                              |
| Dell Latitude E5430                        | [链接](https://github.com/osx86-ijb/Dell-Latitude-e5430-3rd-Gen-Core-i5-3210m-macOS-BigSur) |                                                              |                                                              |
| Dell Latitude E5440                        | [链接](https://github.com/alf45tar/Latitude-E5440-EFI-Partition) |                                                              | Dell E5440                                                   |
| Dell Latitude E5470                        | [链接](https://github.com/txt1994/dell_latitude5470_i7-6820hq) |                                                              |                                                              |
| Dell Latitude E5480 | [链接](https://github.com/anunna/Dell_Latitude_5480_EFI_OC) | | |
| Dell Latitude E5490                        | [链接](https://github.com/lijun215021/DELL-5490-hackintosh) [链接](https://github.com/novseje/dell-latitude-5490-hackintosh-clover) |                                                              |                                                              |
| Dell Latitude E5570 | [链接](https://github.com/misa198/dell-latitude-e5570-hackintosh) | | |
| Dell Latitude E5590 | [链接](https://github.com/marousis/Dell-5590-MacOS) | | |
| Dell Latitude E5591                        | [链接](https://github.com/geowoden/DELL-Latitude-5591_osx-clover) |                                                              |                                                              |
| Dell Latitude E6230 | [链接](https://github.com/Hayafumi/dell-latitude-e6230-opencore) | | |
| Dell Latitude E6330                        |                                                              |                                                              |                                                              |
| Dell Latitude E6430                        | [链接](https://github.com/kinoute/Hack-Dell-Latitude-E6430)  |                                                              |                                                              |
| Dell Latitude E6440 | [链接](https://github.com/afzl-wtu/Dell-E6440-Opencore-EFI) | | |
| Dell Latitude E7250                        | [链接](https://github.com/SkyrilHD/Dell-E7250-Hackintosh)    |                                                              |                                                              |
| Dell Latitude E7280                        | [链接](https://github.com/Lorys89/DELL_LATITUDE_7280) |                                                              |                                                              |
| Dell Latitude E7370                        | [链接](https://github.com/mikeTOliu/dell-latitude7370-Hackintosh-EFI-backup) [链接](https://github.com/gazzmanzx6/OC_Dell_Latitude_7370) |                                                              |                                                              |
| Dell Latitude E7390                        | [链接](https://github.com/Swung0x48/Dell-Latitude-7490-Hackintosh-EFI) [链接](https://github.com/PurpleCrumpets/Hackintosh-Dell-Latitude-7390-2-in-1-OpenCore-EFI) [链接](https://github.com/guozenghuang/latitude-E7390-hackintosh) |                                                              | 基于 Latitude 7490。 不保证 7390 可用。（可在 issue 中提出 7390 的问题） |
| Dell Latitude E7440                        | [链接](https://github.com/ameeno/Dell-E7440-Hackintosh)      |                                                              |                                                              |
| Dell Latitude E7450                        | [链接](https://github.com/rahmadsandy/Dell-E7450-DW1530-Catalina) |                                                              |                                                              |
| Dell Latitude E7470                        | [链接](https://github.com/adityabakare/macOS-Dell-Latitude-E7470) |                                                              | PRECISION 7710可用      |
| Dell Latitude E7480                        | [链接](https://github.com/TranNgocKhoa/Dell-Latitude-E7480-Hackintosh) [链接](https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh)|                                                              |                                                              |
| Dell Latitude E7490                        | [链接](https://github.com/Swung0x48/Dell-Latitude-7490-Hackintosh-EFI) |                                                              |                                                              |
| Dell OptiPlex 3050                         | [链接](https://github.com/Leif160519/Dell-OptiPlex-3050-EFI) [链接](https://github.com/superleeyom/Hackintosh-Dell-OptiPlex-3050-OpenCore)<br />[链接](https://github.com/Xhichn/Hackbook_MECHREVO_Umi_Pro_II) | [链接](https://github.com/Leif160519/Dell-OptiPlex-3050-EFI/blob/master/README.md) |                                                              |
| Dell OptiPlex 3060                         | [链接](https://github.com/Drovosek01/hackintosh_DELL_OptiPlex_3060_i5-8500) |                                                              |                                                              |
| Dell OptiPlex 3060 MFF                     | [链接](https://github.com/Lorys89/DELL_OPTIPLEX_3060_MFF)    |                                                              |                                                              |
| Dell Optiplex 5040                         | [链接](https://github.com/lsc1978/Optiplex-5040-EFI-OC) [链接](https://github.com/lsc1978/Optiplex-5040-EFI-CLOVER) |                                                              |                                                              |
| Dell Optiplex 7020                         | [链接](https://github.com/zearp/optimac)                     |                                                              |                                                              |
| Dell OptiPlex 7070 MFF                     | [链接](https://github.com/liaoyudong2/Dell-7070-mff-hackintosh) | [链接](https://github.com/webleon/Hackintosh-OptiPlex-7070-MFF)                                                              |  OC引导，支持 Big Sur / Monterey                                                           |
| Dell OptiPlex 7070 SFF                     | [链接](https://github.com/webleon/Hackintosh-OptiPlex-7070-SFF) |                                                              | OC引导，支持 Big Sur / Monterey                                                             |
| Dell OptiPlex 9020                         | [链接](https://github.com/kyroschow/Dell-Optiplex-9020-Hackintosh-Clover-EFI) |                                                              |                                                              |
| Dell OptiPlex 9020 USFF                    | [链接](https://github.com/Lorys89/DELL_OPTIPLEX_9020_USFF)   |                                                              |                                                              |
| Dell OptiPlex 9020 OpenCore                | [链接](https://github.com/li3p/dell-optiplex-9020-hackintosh-opencore) | [链接](https://github.com/li3p/dell-optiplex-9020-hackintosh-opencore/blob/master/README.md) | 支持 MT/SFF/USFF/Micro 所有机型                              |
| Dell Precision 5510                        | [链接](https://github.com/soulomoon/Dell-Precision-5510-OSX) [链接](https://github.com/PLChinDev/Dell-Precision-5510-Mojave) |                                                              | Dell-Precision-5510<br />链接 2 支持`Catalina`               |
| Dell Precision 5560 | [链接](https://github.com/tueminh192/Dell-5560-Hackintosh) | |  |
| Dell Precision 5591                        | [链接](https://github.com/n0faith/Dell-Precision-5591-Hackintosh) |                                                              |                                                              |
| Dell Precision M3800<br />Dell XPS 15-9530 | [链接](https://github.com/syscl/M3800)                       | [链接](https://github.com/syscl/M3800/blob/M3800/README.md)  | Dell M3800 和 XPS 9530                                       |
| Dell Precision 7520 | [链接](https://github.com/TECHNIKVERBOT/Dell-Precision-7520-OpenCore) |  |  |
| DELL VOSTRO 14 3401 | [链接](https://github.com/callmeumm/Dell-Vostro-14-3401-Hackintosh) | | |
| Dell Vostro 3468                           | [链接](https://github.com/ahianf/dell-vostro-3468-hackintosh) |                                                              |                                                              |
| Dell Vostro 3490                           | [链接](https://github.com/FaneCH/Vostro-3490-hackintosh) [链接](https://github.com/StefanChimu/Vostro-3490-hackintosh) |                                                              | I5-10210u                                                    |
| Dell Vostro 3568                           | [链接](https://github.com/hsed-sys/vostro-3568-clover-efi)   |                                                              |                                                              |
| Dell Vostro 3578                           | [链接](https://github.com/ABCDFAS/dell-vostro-3578-hackintosh-clover-efi) [链接](https://github.com/ABCDFAS/hackintosh-vostro-3578-opencore-EFI) |                                                              |                                                              |
| Dell Vostro 3667 | [链接](https://github.com/Goodmorningmm/Hacktonish-Vostro-3667-EFI) | | |
| Dell Vostro 5370                           | [链接](https://github.com/hellmonky/Hackintosh/tree/master/dell-vostro-5370) |                                                              |                                                              |
| Dell Vostro 5471                           | [链接](https://github.com/Lorys89/DELL_VOSTRO_5471)          |                                                              |                                                              |
| Dell Vostro 5401 (ICE-LAKE)                | [链接](https://github.com/Lorys89/Dell_Vostro_5401-ICE-LAKE) |                                                              |                                                              |
| Dell Vostro 14 5490                        | [链接](https://github.com/msdnna/Dell-Vostro-14-5490-Hackintosh) |                                                              | i5-10210U / **i7-10510U**                                    |
| Dell Vostro 5568                           | [链接](https://github.com/dungnt11/dell-5568-efi-10.15.6)    |                                                              |                                                              |
| Dell Vostro 5581                           | [链接](https://github.com/nghetienhiep/Dell-Vostro-5581-Hackintosh) |                                                              |                                                              |
| Dell Vostro 5590 | [链接](https://github.com/andreibleortu/Dell-Vostro-5590-Hackintosh-EFI) | | 据说适用于 Inspiron 5490/5498/5590/5598 |
| Dell XPS 15 7590                           | [链接](https://github.com/daliansky/XPS15-7590-Hackintosh) [链接](https://github.com/gorquan/OC-XPS-7590) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Dell XPS13 9343                            | [链接](https://github.com/SiGae/macOS-Mojave-on-xps-13-9343) | [链接](https://github.com/haos001/XPS13-9343-Clover)         |                                                              |
| Dell XPS 9350                              | [链接](https://github.com/syscl/XPS9350-macOS) [链接](https://github.com/andrerds/efi-big-sur-mb-asus-M5A97) | [链接](https://github.com/syscl/XPS9350-macOS/blob/master/README.md) | Dell XPS 9350                                                |
| Dell XPS 9360                              | [链接](https://github.com/hoanX/xps13-9360-i7-7560u)         | [链接](https://github.com/hoanX/xps13-9360-i7-7560u/blob/master/README.md) | Dell XPS 9360，网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Dell XPS 9360                              | [链接](https://github.com/ymmshi/XPS-9360) [链接](https://github.com/MasonGao/XPS-9360-Hackintosh) <br />[链接](https://github.com/the-marcus/XPS-9360-hackintosh) [链接](https://github.com/the-darkvoid/XPS9360-macOS) <br />[链接](https://github.com/0xHJK/XPS13-9360-i5-8250U-macOS) [链接](https://github.com/samuelshi/XPS13-9360) | [链接](https://github.com/ymmshi/XPS-9360/blob/master/README.md) | Dell XPS 9360，网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Dell XPS 9370                              | [链接](https://github.com/jieelin/XPS9370-Hackintosh)        |                                                              |                                                              |
| Dell XPS 9380                              | [链接](https://github.com/wdubaiyu/Hackintosh-Dell-XPS-9380) |                                                              |                                                              |
| Dell XPS 15 9500 | [链接](https://github.com/zspherez/Dell-XPS-9500-4K-UHD-Monterey) | | 4K |
| Dell XPS 9530                              | [链接](https://github.com/the-darkvoid/XPS9530-OSX/tree/10.13) | [链接](https://www.tonymacx86.com/threads/guide-dell-xps-9530-clover-uefi-hotpatch.235558/) | XPS 9530                                                     |
| Dell XPS 9550                              | [链接](https://github.com/wmchris/DellXPS15-9550-OSX) [链接](https://github.com/corenel/XPS9550-macOS)[链接](https://github.com/xxxzc/xps15-9550-macos) | [链接](https://github.com/wmchris/DellXPS15-9550-OSX/blob/10.14/README.md) [链接](https://github.com/corenel/XPS9550-macOS/blob/master/README.md) | Dell XPS 9550                                                |
| Dell XPS 9559                              | [链接](https://github.com/darwinboaventura/Dell-XPS-9559-EFIs) |                                                              |                                                              |
| Dell XPS 9560                              | [链接](https://github.com/gunslinger23/XPS15-9560-High-Sierra) | [链接](https://github.com/gunslinger23/XPS15-9560-High-Sierra/blob/master/README.md) | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell XPS 9570                              | [链接](https://github.com/Xigtun/xps-9570-mojave) [链接](https://github.com/bavariancake/XPS9570-macOS) <br />[链接](https://github.com/LuletterSoul/Dell-XPS-15-9570-macOS-Mojave) |                                                              | 感谢：[LuletterSoul](https://github.com/LuletterSoul) 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell XPS 13 9300                           | [链接](https://github.com/leon0410898/XPS13-9300-hackintosh) |                                                              | i7-1065G7                                                    |
| Dell Inspiron 7586                           | [链接](https://github.com/hacker1024/Dell-Inspiron-7586-Hackintosh) |                                                              |                                                    |
| Dell G7 7588                              | [链接](https://github.com/rex-lapis/Hackintosh-Dell-G7-7588-OpenCore) |                                                              |                                                              |
| Dell Precision 7530 7540 7730 7740                  | [链接](https://github.com/lulu-gh/Dell-Precision-E7530-Prototype-OpenCore) |                                                              |       默认是7530工程机EFI，用于量产机型先看说明再安装；默认配置支持AMD独显，用集显自行屏蔽或者换硬件        |

### Gigabyte 技嘉

| 机型名称           | 发布地址                                                 | 教程地址                                                                    | 备注 |
| ------------------ | -------------------------------------------------------- | --------------------------------------------------------------------------- | ---- |
| Gigabyte Aero 15X  | [链接](https://github.com/zacmks/Hackintosh-Aero-15X)    | [链接](https://github.com/zacmks/Hackintosh-Aero-15X/blob/master/README.md) |      |
| Gigabyte Aero 15W  | [链接](https://github.com/Errrneist/Hackintosh-Aero-15W) |                                                                             |      |
| Gigabyte Sabre 15K | [链接](https://github.com/gnehs/Sabre15KClover)          |                                                                             |      |
| Gigabyte-Z390M-GAMING | [链接](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING)          |                                                                             |      |

### Hasee 神舟

| 机型名称                                  | 发布地址                                                     | 教程地址                                           | 备注                                                         |
| ----------------------------------------- | ------------------------------------------------------------ | -------------------------------------------------- | ------------------------------------------------------------ |
| 神舟 A480B                                | [链接](https://github.com/wklxd/A480B)                       |                                                    |                                                              |
| 战神 K610D-i5D3                           | [链接](https://github.com/1zilc/K610d-i5-d3-10.14.5-efi-clover) |                                                    |                                                              |
| 战神 K650D                                | [链接](https://github.com/wklesss/k650D-Hackintosh)          |                                                    | 战神 K650D                                                   |
| 战神 K650D-SL5S1                          | [链接](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1800662) | [链接](https://blog.nyaasu.top/front-end/111.html) | EFI 文件部分有效，无线网卡和电池无法驱动                     |
| 战神 K650D-i5D2                           | [链接](https://github.com/ivothgle/Hackintosh)               |                                                    |                                                              |
| 战神 K670C-g6a1                           | [链接](https://github.com/nitokris/nb50tg-opencore)          |                                                    | 蓝天 nb50tg                                                  |
| 战神 K680E-G6D1                           | [链接](https://github.com/Vnzen/Hackintosh_hasee_k680e-g6d1_clover) [链接](https://github.com/zhboat/k680e-g6d1_Hackintosh) |                                                    |                                                              |
| 战神 K770E-i7D1                           | [链接](https://github.com/Gitawake/Hasee-K770e-i7-D1-Clover) |                                                    | 准系统型号：蓝天 P170SM-A                                    |
| 战神 Z6-SL5D1                             | [链接](https://github.com/Measureless/Hackintosh_Hasee_Z6-SL5D1) |                                                    | 准系统型号： 蓝天 N151RD-HM170                               |
| 战神 Z7-KP7D1 <br> Z7-KP7S1               | [链接](https://github.com/ConnersHua/Clevo-P65xHP-Hackintosh) [链接](https://github.com/hevervie/Hackintosh_HASEE_Z6-KP7S1)<br />[链接](https://github.com/houyp1116/Z7-KP7S1-EFI) |                                                    | 准系统型号：蓝天 P65xHP                                      |
| 战神 Z7-SP5D1                             | [链接](https://github.com/moonheart/Hackintosh-P65xRP6-Z7-SP5D1) |                                                    |                                                              |
| 战神 Z7(M)-KP7/5GZ                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK5CN6X, GK5CN5X                            |
| 战神 Z7(M)-KP7/5Z                         | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK5CN6X, GK5CN5X                            |
| 战神 Z7-KP7EC                             | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GJ5CN64                                     |
| 战神 Z7(M)-KP7/5GC                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GJ5CN64, GI5CN54, by @kirainmoe             |
| 战神 Z7M-KP5GC                            | [链接](https://github.com/CharlesZhou959/Hasee-Z7M-KP5GC-Hackintosh) |                                                    | 准系统型号：同方 GI5CN54, by @CharlesZhou959                 |
| 战神 Z7(M)-KP7/5GA                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GJ5CN64, GI5CN54                            |
| 战神 Z7(M)-KP7/5GE                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GJ5CN64, GI5CN54                            |
| 战神 Z7(M)-KP7/5GH                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GJ5CN64, GI5CN54                            |
| 战神 Z7-CT7/5GK                           | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK5CP6X                                     |
| 战神 Z7M-CT7GS                            | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK5CP5X                                     |
| 战神 Z7(M)-CT7/5GA                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK5CP6V, GK5CP5V                            |
| 战神 Z7(M)-CT7/5VH                        | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK5CP6V, GK5CP5V                            |
| 战神 G7-CT7VK                             | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK7CP6R                                     |
| 战神 G7-CT7RA                             | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)    | [链接](https://www.bilibili.com/video/av81263778)  | 准系统型号：同方 GK7CP6R                                     |
| 战神 Z7(M)-CT7/5NA                        | [链接](https://github.com/bufsnake/Z7-CT7NA-HackIntosh)      |                                                    | 准系统型号： 蓝天 NH50Rx                                     |
| 战神 Z7(M)-CT7/5NA (NK/NT)                | [链接](https://github.com/a328661276/Clevo-NH50-NH70-Hackintosh-macOS10.15.3) [链接](https://github.com/MichaelPan1026/Clevo-NH50-NH70-Hackintosh) |                                                    | 准系统型号：蓝天 NH5xRD/RC/RA/RH(Q)                          |
| 战神 G7-CT7NA (NK/NT)                     | [链接](https://github.com/a328661276/Clevo-NH50-NH70-Hackintosh-macOS10.15.3) [链接](https://github.com/MichaelPan1026/Clevo-NH50-NH70-Hackintosh) |                                                    | 准系统型号：蓝天 NH70RD_RC_RA_RH(Q)                          |
| 战神 G8-CT7NA (NK/NT)                     | [链接](https://github.com/a328661276/Clevo-NH50-NH70-Hackintosh-macOS10.15.3) [链接](https://github.com/MichaelPan1026/Clevo-NH50-NH70-Hackintosh) |                                                    | 准系统型号：蓝天 NH70RD_RC_RA_RH(Q)                          |
| 战神 G8-CU7NA                             | [链接](https://github.com/caoying827/OC)                     |                                                    | 准系统 NHxxDCDD                                              |
| 战神 GX8-CP5/CR6                          | [链接](https://github.com/JokerHYC/P775TM-HACKINTOSH)        |                                                    | 准系统型号：蓝天 P775TM <br> 未来人类 X711，炫龙 V87 等使用蓝天 p775tm 模具的 10 系显卡都支持 |
| 战神 Z6-KP7S1                             | [链接](https://github.com/hevervie/Hackintosh_HASEE_Z6-KP7S1) |                                                    |                                                              |
| 战神 ZX7-CP5SC                            | [链接](https://github.com/bavelee/NB5TK1_TJ1-Hackintosh/)    | [链接](https://bavelee.cn/archives/60.html)        | 准系统型号：蓝天 NB50/60 TJ1/TK1                             |
| 战神 ZX6-CP5S1                            | [链接](https://github.com/bavelee/NB5TK1_TJ1-Hackintosh/)    | [链接](https://bavelee.cn/archives/60.html)        | 准系统型号：蓝天 NB50/60 TJ1/TK1                             |
| 战神 K680E-G6E3/G6D3                      | [链接](https://github.com/bavelee/NB5TK1_TJ1-Hackintosh/)    | [链接](https://bavelee.cn/archives/60.html)        | 准系统型号：蓝天 NB50/60 TJ1/TK1                             |
| 战神 TX7-CT5DS                            | [链接](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1843619&highlight=%C9%F1%D6%DB) |                                                    | 准系统型号：蓝天 N960TC                                      |
| 战神 Z7M-KP7GT                            | [链接](https://github.com/Xin9912/Hackintosh)                |                                                    |                                                              |
| Hases-z7-kp7sc                            | [链接](https://github.com/Bluestar-coder/Hases-z7-kp7sc-10.15.4-OC) |                                                    |                                                              |
| 精盾 U47T1                                | [链接](https://github.com/zhuchuanwu/haseeu47t1)             |                                                    |                                                              |
| 精盾 T96E                                 | [链接](https://github.com/L0ngxhn/Hackintosh-Hasee-T96E)     |                                                    | 准系统型号：蓝天 P950EP6                                     |
| 精盾 K590S                                | [链接](https://github.com/JokerHYC/K590S-HACKINTOSH)         |                                                    | 准系统型号： 蓝天 W350ET                                     |
| 战神 Z7(M)-CT7(5NA/NK/NT)/G7/G8-CT7-NA-NK | [链接](https://github.com/MichaelPan1026/Clevo-NH50-NH70-Hackintosh) |                                                    | 准系统型号： 蓝天 NH50,NH70Rx 系列                           |
| 战神 Z7-SP7S2                             | [链接](https://github.com/tilkofjin/blackMac) [链接](https://github.com/tilkofjin/HASEE-Z7-SP7S2-BigSur) |                                                    |                                                              |

### HP 惠普

| 机型名称                                        | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ----------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| HP ProBook/EliteBook<br />ZBook 系列            | [链接](https://github.com/RehabMan/HP-ProBook-4x30s-DSDT-Patch) | [链接](https://www.tonymacx86.com/threads/guide-hp-probook-elitebook-zbook-using-clover-uefi-hotpatch.261719/) | 除 8x60W,8x70W 系列之外的机型，<br />二代 CPU 及之前的机型仅支持到 10.13.x |
| HP Envy Haswell J/K/Q/N<br />系列笔记本         | [链接](https://github.com/RehabMan/HP-Envy-DSDT-Patch)       | [链接](https://www.tonymacx86.com/threads/guide-hp-envy-haswell-series-j-k-q-n-using-clover-uefi.261724/) | 仅 4 代 envy 机型                                            |
| HP 14S-FQ1000NA                                 | [链接](https://github.com/vijinho/OpenCore-HP14S-FQ1000NA)   |                                                              | AMD Ryzen 5500U                                              |
| HP 15 BS661TX                                   | [链接](https://github.com/sortedcord/hp15bs661tx-hackintosh) |                                                              |                                                              |
| HP 15 D062TU                                    | [链接](https://github.com/khanhtran-cse/hp-15-d062tu-hackintosh) |                                                              |                                                              |
| HP 15 da0004tu                                  | [链接](https://github.com/Flashminat0/hp-15-da0004tu-notbook-big-sur-efi) |                                                              |                                                              |
| HP Zbook G1                                     | [链接](https://github.com/Thatisjigen/OC_Zbook-G1-Big-Sur)   |                                                              |                                                              |
| HP Zbook 15 G2                                  | [链接](https://github.com/cmc3svn/opencore-zbook-15-g2)      |                                                              |                                                              |
| HP 15G BR011TX                                  | [链接](https://github.com/SahilSonar/hackintosh-hp-15g-br011tx) |                                                              |                                                              |
| HP Laptop 14S-DQ1013TU                          |                                                              |                                                              |                                                              |
| HP Laptop 15-da0233ur                           | [链接](https://github.com/DmitriyyyyS/Hackintosh-HP-Laptop-15-da0233ur) |                                                              | i3-7020U                                                     |
| HP Notebook AY073TU                             | [链接](https://github.com/tueminh192/HP-AY073TU-Hackintosh)  |                                                              |                                                              |
| HP Notebook bp1xx                               | [链接](https://github.com/XcHeeZTeam/hackintosh)             |                                                              |                                                              |
| HP Notebook 15ac001tx                           | [链接](https://github.com/lehuutrung1412/Hackintosh-HP-Laptop) |                                                              |                                                              |
| HP 17 BY0062ST                                  | [链接](https://github.com/emilevirus/HP-BY00000-HACKINTOSH)  |                                                              |                                                              |
| HP Envy 13 ad024TU                              | [链接](https://github.com/Astrobr/HackintoshForEnvy13-ad0xx) |                                                              |                                                              |
| HP Envy 13 ad1xxx                               | [链接](https://github.com/ArisHub/Hackintosh_Envy13_10.13.6-10.14.4) | [链接](https://github.com/ArisHub/Hackintosh_Envy13_10.13.6/blob/master/README.md) | 惠普 envy13                                                  |
| HP Envy 13 model ah0002la                       | [链接](https://github.com/jomarnavarro/hp-envy-clover)       |                                                              |                                                              |
| HP Envy15 as109tu                               | [链接](https://github.com/TianNes/Hackintosh-Clover)         |                                                              |                                                              |
| HP Envy 15 as110tu                              | [链接](https://github.com/wing-ho/HP-AS110TU-Hackintosh)     |                                                              |                                                              |
| HP Envy x360 15-aq160sa                         |                                                              |                                                              |                                                              |
| HP ENVY x360 - 15-bp103tx                       | [链接](https://github.com/jay1060950003/HP_ENVY_OC)          |                                                              |                                                              |
| HP Envy DV6 7303ef                              |                                                              |                                                              |                                                              |
| HP Omen AX205                                   | [链接](https://github.com/donxp/HP-OMEN-AX205-HACKINTOSH)    |                                                              |                                                              |
| Hp Omen Ce020tx                                 | [链接](https://github.com/thanatath/hp-omen-ce020tx-mojave-osx) |                                                              |                                                              |
| HP Omen Laptop 15-ce0xx                         | [链接](https://github.com/t-shao/-Hackintosh-OMEN_by_HP_Laptop_15-ce0xx) |                                                              |                                                              |
| HP 250 G2                                       | [链接](https://github.com/MrPotatoBobx/hp250g2opencore)      |                                                              |                                                              |
| HP 250 G6                                       | [链接](https://github.com/snajdovski/HP-250-G6-Mojave-EFI) [链接](https://github.com/Baio1977/HP-250-G6-Kabylake) |                                                              |                                                              |
| HP 348 G5                                       | [链接](https://github.com/zsakvo/hp-348-g5-hackintosh)       |                                                              |                                                              |
| HP Probook 430 G3                               | [链接](https://github.com/mdraan1/HP-Probook-430-G3-macos)   | [链接](https://github.com/Human7900/macOS-HP-Probook-430-G3-Resources) |                                                              |
| HP Probook 430 G5                               |                                                              |                                                              |                                                              |
| HP ProBook 430 G6                               | [链接](https://github.com/YGQ8988/HP-ProBook430G6)           |                                                              | i5-8265U 已卸载内置镁光 nvme SSD(此硬盘不识别)               |
| HP ProBook 440 G2                               |                                                              |                                                              |                                                              |
| HP ProBook 440 G3                               | [链接](https://github.com/code0Artuh/EFI-Probook-440-G3)     |                                                              |                                                              |
| HP Probook 440 G6                               | [链接](https://github.com/fjh1997/HP_Probook_440_G6_hackintosh) |                                                              |                                                              |
| HP Probook 450 G5                               | [链接](https://github.com/Flashminat0/hp-probook-450-g5-big-sur-opencore-efi-files) |                                                              |                                                              |
| HP ProBook 470 G1                               | [链接](https://github.com/mavethee/Hackintosh-OpenCore-HP-ProBook-470-G1) |                                                              |                                                              |
| HP ProBook 650 G1                               | [链接](https://github.com/Hologos/hackintosh-hp-probook-650-g1) |                                                              |                                                              |
| HP Elitebook 820 G3                             | [链接](https://github.com/Fenix46/efi_hp_820g3_monterey)     |                                                              |                                                              |
| HP Elitebook 830 G7                             | [链接](https://github.com/adrianjagielak/HP-Elitebook-850-G7-Hackintosh) |                                                              |                                                              |
| HP Elitebook 840-G1                             | [链接](https://github.com/blint01/hackintosh-mojave-HP-840-G1) | [链接](https://github.com/blint01/hackintosh-mojave-HP-840-G1/blob/master/README.md) |                                                              |
| HP Elitebook 840 G2                             | [链接](https://github.com/AktasC/Hackintosh-Elitebook-840-G2-Broadwell) |                                                              |                                                              |
| HP EliteBook 840 G3                             | [链接](https://github.com/GGorAA/Hackintosh-840) [链接](https://github.com/Innoxious/hackintosh-hp-840-g3-intel-ac8260) |                                                              | Big Sur                                                      |
| HP EliteBook 840 G4                             | [链接](https://github.com/XXCoreRangerX/Hackintosh-HP-EliteBook-840-G4) |                                                              |                                                              |
| HP EliteBook 840 G6                             | [链接](https://github.com/mahdose/Hackintosh-HP-EliteBook-840-G6) |                                                              |                                                              |
| HP EliteBook 840 G7                             | [链接](https://github.com/pdff/Hackintosh-HP-Elitebook840G7) [链接](https://github.com/adrianjagielak/HP-Elitebook-850-G7-Hackintosh) |                                                              |                                                              |
| HP EliteBook 850 G5                             | [链接](https://github.com/kinoute/Hack-HP-EliteBook-850-G5)  |                                                              |                                                              |
| HP Elitebook 850 G7                             | [链接](https://github.com/adrianjagielak/HP-Elitebook-850-G7-Hackintosh) |                                                              |                                                              |
| HP EliteBook Folio 9470m                        | [链接](https://github.com/hackintosh107/Hackintosh-OpenCore-HP-9470m-1366x768) [链接](https://github.com/hackintosh107/Hackintosh-OpenCore-HP-9470m-1600x900) |                                                              |                                                              |
| HP Elitebook 9480m                              | [链接](https://github.com/mrpapersonic/hp-eb-9480m-oc-efi)   |                                                              |                                                              |
| HP EliteBook Folio 1040 G3                      | [链接](https://github.com/meciu/HP-EliteBook-Folio-1040-G3-OpenCore) |                                                              |                                                              |
| HP EliteBook 1040 G4                            | [链接](https://github.com/AustinBoath/HP-EliteBook-1040-G4-Hackintosh) |                                                              |                                                              |
| HP prodesk 600g1-DM/800g1-DM                    | [链接](https://github.com/LomotHo/Hackintosh-600g1-DM-4670t) |                                                              |                                                              |
| HP Pavilion 14-al061nr                          | [链接](https://github.com/ipwndev/14-al061nr-hackintosh)     |                                                              |                                                              |
| HP Pavilion 14-bf033tx                          | [链接](https://github.com/zo98/HP-Pavilion-14-bf033tx-efi)   |                                                              |                                                              |
| HP Pavilion 14-CE2072NL                         | [链接](https://github.com/1alessandro1/HP-Pavilion-CE2072NL-macOS/blob/main/README.md) |                                                              |                                                              |
| HP Pavilion Laptop 14-ce3xxx                    | [链接](https://github.com/MuziShaoxing/HP-Pavilion-Laptop-14-ce3xxx-1035G1) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| HP Pavilion 14-v011tx                           | [链接](https://github.com/PangeranWiguan/HP-Pavilion-14-v011tx-Opencore-EFI) |                                                              |                                                              |
| HP Pavilion 15an051dx                           | [链接](https://github.com/Marcowerjr/macOS-HP-Pavilion-15an051dx) |                                                              |                                                              |
| HP Pavilion 15 au028ur                          | [链接](https://github.com/Drovosek01/hackintosh_HP_Pavilion_15-au028ur_i5-6200U/blob/master/docs/ENG/README.md) |                                                              |                                                              |
| HP Pavilion 15 au067tx                          |                                                              |                                                              |                                                              |
| HP Pavilion15 AU157TX                           |                                                              |                                                              |                                                              |
| HP Pavilion15 au146TX                           | [链接](https://github.com/nabaonan/HP-Pavilion-au146tx-efi)  |                                                              |                                                              |
| HP Pavilion 15 au624tx                          | [链接](https://github.com/kumarayush2104/OC-Hackintosh)      |                                                              |                                                              |
| HP Pavillion 15 da0596                          | [链接](https://github.com/melkyfb/efi-hp-da0596)             |                                                              |                                                              |
| HP Pavilion 15G BR011TX                         | [链接](https://github.com/SahilSonar/hackintosh-hp-15g-br011tx) |                                                              |                                                              |
| HP Pavilion 15 cb008nt                          | [链接](https://github.com/dorukmacdo/Opencore-HP-Pavilion-15-cb008nt) |                                                              |                                                              |
| HP Pavilion 15-cc107nt                          | [链接](https://github.com/ufukynz/HP-Pavilion-15-CC107NT)    |                                                              |                                                              |
| HP Pavilion ce3034nl                            | [链接](https://github.com/Gaggu097/HP-pavillion-ce3034nl-EFI) |                                                              |                                                              |
| HP Pavillion ck069tx                            | [链接](https://github.com/Blizzard57/Hackintosh)             |                                                              |                                                              |
| HP Pavilion 15-cs0093ca                         |                                                              |                                                              |                                                              |
| HP Pavilion 15 cs1xxx                           | [链接](https://github.com/JaeSeoKim/HP-Pavilion-Laptop-15-cs1xxx-Hackintosh) |                                                              |                                                              |
| HP Pavilion 15-CS3005NT                         | [链接](https://github.com/hackintoshman/example-efi-for-HP-Pavilion-15-CS3005NT) |                                                              |                                                              |
| HP Pavilion 16 a000x                            | [链接](https://github.com/steve4655/EFI-for-HP-pavilion-gaming-16) |                                                              |                                                              |
| HP Pavilion 550                                 | [链接](https://github.com/Aster-the-Med-Stu/HP-Pavilion-550-Hackintosh) |                                                              |                                                              |
| Hp Spectre X360                                 | [链接](https://github.com/Just-maple/Hp-spectre-X360-hackintosh) |                                                              |                                                              |
| HP Spectre X360 15-bl112dx                      | [链接](https://github.com/WoadZS/HP-Spectre-X360-15-Hackintosh) |                                                              |                                                              |
| HP Spectre X360 13 late 2018                    | [链接](https://github.com/SeptemberHX/HP-Spectre-X360-13-late-2018-Hackintosh) |                                                              |                                                              |
| HP EliteDesk 800-G3-Mini                        | [链接](https://github.com/francoisminh/Hackintosh-EliteDesk-800-G3-Mini-65W) | [链接](https://github.com/francoisminh/Hackintosh-EliteDesk-800-G3-Mini-65W/blob/master/README.md) |                                                              |
| HP Zhan 66 AMD                                  | [链接](https://github.com/fangqiangfly/HP-ZHAN66-AMD-hackintosh) |                                                              | AMD Ryzen 7 3700U                                            |
| HP Zhan 66 Pro G1                               | [链接](https://github.com/A-Linz/Hackintosh-HP-Zhan-66-Pro-G1) [链接](https://github.com/RenAmamiya/HP-Zhan-66-Pro-G1) |                                                              |                                                              |
| HP ZHAN 66 PRO 14 G2                            | [链接](https://github.com/peihexian/HP-ZHAN-66-Pro-14-G2)    |                                                              |                                                              |
| HP ZHAN99 zbook 15v g5                          | [链接](https://github.com/rote66/Hackintosh_HP_ZBOOK15VG5)   |                                                              |                                                              |
| HP ZHAN99 WorkStation G1                        | [链接](https://github.com/MacsedProtoss/hackintosh)          |                                                              |                                                              |
| 暗影精灵 5 dc1010nr                             | [链接](https://github.com/hibobmaster/HP-15-dc1010nr-hackintosh) | [链接](https://blog.hibobmaster.com/hp-15-dc1010nr-hackintosh/) |                                                              |
| 暗影精灵 4 i5-8300H GTX1050Ti                   | [链接](https://github.com/sunmousn/OMEN-by-HP-Laptop-15-dc0xxx) | [链接](https://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1832126) | 15-DC0xxx                                                    |
| 暗影精灵 2                                      | [链接](https://github.com/Arecall/-Mac-os)                   |                                                              |                                                              |
| 惠普暗影精灵 2 15-ax015TX                       | [链接](https://github.com/a13134455667/HP-15-ax015TX-MAC10.15.4-OC-EFI) |                                                              | OpenCore 0.6.0 / Big Sur                                     |
| 暗影精灵 II 代 Pro <br />HP OMEN 15-ax214TX     | [链接](https://github.com/ZGGSONG/HP-OMEN-15-ax214TX-Hackintosh) |                                                              |                                                              |
| 暗影精灵 2 Pro HP OMEN 15-ax225TX               | [链接](https://github.com/Cruii/HP-OMEN-15-ax225TX) [链接](https://github.com/XStar-Dev/HP_OMEN-2Pro_Hackintosh)<br />[链接](https://github.com/sve1r/OMEN-By-HP-15-ax225TX-Hackintosh-EFI) |                                                              |                                                              |
| 暗影精灵 2 Pro HP OMEN 15-ax218TX               | [链接](https://github.com/liyafe1997/hackintosh-hp-omen-15-2017-EFI) |                                                              | 基于Clover 5151，自用macOS 13 Ventura<br>能往下兼容到10.15甚至更低<br>理论上HP暗影2Pro系列各细分型号通用<br>（ax225TX/218TX/214TX等等） |
| 惠普光影精灵 3(HP Pavilion 15-cb0xx)            | [链接](https://github.com/zty199/HP_Pavilion_15-cb073tx_Hackintosh) |                                                              | 希望能继续维护                                               |
| 暗影精灵 I (惠普 PAVILION Gaming NB 15-ak039TX) | [链接](https://github.com/lgs3137/PAVILION_Gaming_NB-macOS)  |                                                              | 除了独显、Intel 无线网卡，其他功能模块正常(包括 HDMI 视频)   |
| HP Pavillion Gaming Laptop 15-cx0xxx            | [链接](https://github.com/mechtifs/hackintosh-clover-hp-pavillion-15-cx0xxx) |                                                              | 惠普光影精灵 4                                               |
| HP PAVILION Gaming NB 15-cx0172tx               | [链接](https://github.com/ExodazTH/Opencore-on-HP-Pavilion-Gaming-15-cx0172tx) [链接](https://github.com/ExodazTH/Hackintosh-on-HP-Pavilion-Gaming-15-cx0172tx) |                                                              | non-working:GPU(Nvidia 1050TI/GTX)/WiFi( Intel® Wireless-AC 9560 802.11b/g/n/ac) |
| 惠普光影精灵 5                                  | [链接](https://github.com/Tonymiugrey/Garden-by-miugrey) [链接](https://github.com/hibobmaster/HP-15-dc1010nr-hackintosh) |                                                              | 内含 PM981 的补丁                                            |
| HP Omen 15 DC                                   | [链接](https://github.com/kirainmoe/hp-omen15-dc-macos)      |                                                              | 暗影精灵 4 GTX1060 144Hz 版，由于物理屏蔽核显，只能安装 10.13.6 |
| HP Omen 15 dc0003la                             | [链接](https://github.com/rocadavel/HPOmenDC0003LAHackintoshCatalinaOpenCore) |                                                              |                                                              |
| HP Elite X2 G4 平板                             | [链接](https://github.com/lulujyc/EliteX2G4-OpenCore)        |                                                              |                                                              |
| HP合集                                          | [链接](https://github.com/Baio1977/EFI-Varie-Hackintosh/tree/main/EFI%20Laptop%20/HP) |                                                              |                                                              |

### Huawei 华为

| 机型名称                 | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 华为 Matebook X Pro 2020 | [链接](https://github.com/RepoWeaver/MateBook-X-Pro-2020-OpenCore) |                                                              |                                                              |
| 华为 Matebook X Pro 2019 | [链接](https://github.com/laozhiang/MateBook_X_Pro_2019-Hackintosh) | [链接](https://github.com/laozhiang/MateBook_X_Pro_2019-Hackintosh) | 华为 Matebook X Pro 2019                                     |
| 华为 Matebook X Pro      | [链接](https://github.com/gnodipac886/MatebookXPro-hackintosh) [链接](https://github.com/profzei/Matebook-X-Pro-2018) | [链接](https://github.com/gnodipac886/MatebookXPro-hackintosh/blob/master/README-CN.md) | 华为 Matebook X Pro 2018                                     |
| 华为 Matebook X          | [链接](https://github.com/4323770/Hackintosh-For-Matebook-X) |                                                              |                                                              |
| 华为 Matebook 13         | [链接](https://github.com/Edoardo001/Matebook-13-Hackintosh) [链接](https://github.com/ske1996/matebook-13-2019-oc-efi) |                                                              |                                                              |
| 华为 Matebook 14         | [链接](https://github.com/frezs/MateBook14-Hackintosh)       |                                                              |                                                              |
| 华为 Matebook D          | [链接](https://github.com/MOJUNSHOU/MateBooK-D) [链接](https://github.com/Zero-zer0/Matebook_D_2018_Hackintosh_OpenCore) |                                                              | 华为 MateBook D2018 i5-8250U 15.6 寸<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Huawei Matebook D14 AMD (2020) | [链接](https://github.com/herrnst/HuaweiMatebookD14AMD-OpenCore) | | AMD Ryzen 5 3500U |
| 荣耀 Magicbook           | [链接](https://github.com/hjmmc/Honor-Magicbook) [链接](https://github.com/buseQ/magicbook-hackintosh-opencore-i7-8550u) | [链接](https://github.com/hjmmc/Honor-Magicbook/blob/master/README_CN.md) | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| 荣耀 Magicbook-Pro-16.1  | [链接](https://github.com/GatesYang/Magicbook-Pro-16.1-Hackintosh) |                                                              |                                                              |
| 华为 Matebook 14 2020 款 | [链接](https://github.com/Zero-zer0/Matebook_13_14_2020_Hackintosh_OpenCore) |                                                              | 华为 Matebook 13 / 14 2020 十代 通用                         |
| 荣耀 Magicbook Pro 2020 R7-4800H| [链接](https://github.com/Pinghigh/Magicbook-Pro-2020-R7-4800H-Hackintosh) |                                                              | 荣耀 Magicbook Pro 2020 R7-4800H (aka. HLYL-WXX9)   |

### Lenovo 联想

| 机型名称                           | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Lenovo B50-80 80EW | [链接](https://github.com/moneaalhad/LenovoB50.80_Hackintosh) |  |  |
| Lenovo Flex 15                     | [链接](https://github.com/aytic/Lenovo-Flex-15-Hackintosh)   | [链接](https://github.com/aytic/Lenovo-Flex-15-Hackintosh/blob/master/README.md) | Lenovo Flex 15                                               |
| Lenovo Ideapad S145-15IWL          | [链接](https://github.com/boffik/LenovoS145-15IWL_OpenCore) [链接](https://github.com/Ninjacornix/Lenovo-S145-15IWL-Big-sur-OC-EFI) |                                                              |                                                              |
| Lenovo ideapad 3 14iil05           | [链接](https://github.com/DagerDW/Lenovo-ideapad-3-14iil05-Hackintosh) |                                                              | i5-1035G4 Ice Lake-U                                         |
| Lenovo IdeaPad 3 15ALC6 | [链接](https://github.com/mariolandossa/hackintosh_EFI) | | AMD Ryzen 7 5700U |
| Lenovo IdeaPad 100-15IBY | [链接](https://github.com/BugsMover/Hackintosh_IdeaPad-100-15IBY) | |  |
| Lenovo IdeaPad 300-15ISK           | [链接](https://github.com/reaink/lenovo-ideapad-300-15isk-hackintosh)         | [链接](https://github.com/reaink/lenovo-ideapad-300-15isk-hackintosh) |                                                              |
| Lenovo Ideapad 310-14IKB           | [链接](https://github.com/29satnam/LenovoHackintosh)         | [链接](https://github.com/29satnam/LenovoHackintosh/blob/master/README.md) |                                                              |
| Lenovo Ideapad 320-14IKB           | [链接](https://github.com/Ab2774/Lenovo-IdeaPad-320-14-IKB-Hackintosh)         | [链接](https://github.com/Ab2774/Lenovo-IdeaPad-320-14-IKB-Hackintosh/blob/master/README.md) |                                                              |
| Lenovo Ideapad 330-15ICH           | [链接](https://github.com/Baio1977/EFI-Varie-Hackintosh/tree/main/EFI%20Laptop%20/LENOVO/Lenovo%20ideapad%20330-15ICH%20-%20i5%208300H%20-%20GTX%201050) |                                                              |                                                              |
| Lenovo Ideapad 330-15IKB           |                                                              |                                                              |                                                              |
| Lenovo Ideapad 320-15ISK           | [链接](https://github.com/gajjartejas/Lenovo-Ideapad-320-15ISK-Laptop-Hackintosh) |                                                              |                                                              |
| Lenovo IdeaPad 320S 14IKB          | [链接](https://github.com/quocanh1204/EFI-320s)              |                                                              |                                                              |
| Lenovo Ideapad 320-14ISK           | [链接](https://github.com/dickymuliafiqri/Lenovo-Ideapad-320-14ISK-Hackintosh) |                                                              |                                                              |
| Lenovo Ideapad 330s-14IKB          | [链接](https://github.com/chrisru26/LenovoIdeapad330s-14ikb-Hackintosh) |                                                              |                                                              |
| Lenovo Ideapad S340                | [链接](https://github.com/4mitabh/Ideapad_S340) [链接](https://github.com/IvanAleksandrov94/Lenovo-s340-Big-Sur-OpenCore-i5-8265u) |                                                              |                                                              |
| Lenovo Ideapad s340 14api | [链接](https://github.com/ho1yspirt/ideapad-s340-14api-hackintosh) | | AMD  Ryzen 5 3500U |
| Lenovo Ideapad 510-15IKB           | [链接](https://github.com/trgcyln/Lenovo-Hackintosh)         |                                                              |                                                              |
| Lenovo Ideapad S540 14IWL          | [链接](https://github.com/Baio1977/EFI-Varie-Hackintosh/tree/main/EFI%20Laptop%20/LENOVO/Ideapad%20S540%2014IWL) |                                                              |                                                              |
| Lenovo Ideapad 700-15ISK           | [链接](https://github.com/athlonreg/Lenovo-XiaoXin700-15ISK) | [链接](https://github.com/athlonreg/Lenovo-XiaoXin700-15ISK/blob/master/README.md) | Lenovo-XiaoXin700-15ISK                                      |
| Lenovo Ideapad 720s 13IKB          | [链接](https://github.com/xiaominglei001/ideapad-720s-13IKB) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Lenovo IdeaPad Gaming 3i           | [链接](https://github.com/dragons3232/Lenovo-gaming-3-10750h-hackintosh-EFI) |                                                              | i7-10750h                                                    |
| Lenovo IdeaPad Flex 3-1580         |                                                              |                                                              |                                                              |
| Lenovo Ideapad Flex 5 14IIL05 | [链接](https://github.com/Micael106/Lenovo-Ideapad-Flex-5-14IIL05) | | |
| Lenovo G40-70M                     | [链接](https://github.com/jinmu333/Lenovo_G40_70M_EFI)       |                                                              |                                                              |
| Lenovo G40-80                      | [链接](https://github.com/lucasrobaert/efi-lenovo-g40-80-big-sur) |                                                              |                                                              |
| Lenovo G400                        | [链接](https://github.com/autersu/Lenovo_G400_EFI)           |                                                              |                                                              |
| Lenovo G480                        |                                                              |                                                              |                                                              |
| Lenovo G50-80                      | [链接](https://github.com/upupming/Lenovo-G50-80-Clover)     |                                                              |                                                              |
| Lenovo G510                        | [链接](https://github.com/Z39/G510-OS-X-Clover-Hotpatch)     |                                                              | 感谢：[39 军小兵张](http://i.pcbeta.com/space-uid-4472739.html) |
| Lenovo G580 | [链接](https://github.com/TECHNIKVERBOT/Lenovo-G580-OpenCore) | |  |
| 联想 flex3-1470/i5 5200u-hd5500    | [链接](https://github.com/xl120022/FLEX-3-1470-Mac-10.15.3-efi) |                                                              |                                                              |
| Thinkpad E14 Gen 1 | [链接](https://github.com/AniKulkarn/Hackintosh-ThinkPad-E14) | | |
| ThinkPad E40                       | [链接](https://github.com/mendax1234/ThinkPadE40-Clover-EFI) | [链接](http://bbs.pcbeta.com/viewthread-1851317-1-1.html)    | ThinkPad E40                                                 |
| Lenovo 昭阳 E49                    | [链接](https://github.com/pangdahaiNo1/lenovo-E49-macos-efi) |                                                              |                                                              |
| ThinkPad E440                      | [链接](https://github.com/ZzMark/Thinkpad-E440-Hackintosh)   |                                                              |                                                              |
| ThinkPad E450C                     | [链接](https://github.com/zhangxuan1340/Hackintosh_E450C)    |                                                              |                                                              |
| ThinkPad E470                      | [链接(CLOVER)](https://github.com/y010204025/E470-clover) [链接(OC)](https://github.com/ihwf/Lenovo_ThinkPad_E470_Hackintosh)            |                                                              |                                                              |
| ThinkPad E480                      | [链接](https://github.com/aliyoge/Hackintosh-ThinkPad-E480) [链接](https://github.com/SukkaW/ThinkPad-E480-Hackintosh) | [链接](https://github.com/aliyoge/Hackintosh-ThinkPad-E480/blob/master/README.md) |                                                              |
| ThinkPad E490                      | [链接](https://github.com/dievdmitry/Thinkpad-E490-hackintosh) |                                                              |                                                              |
| ThinkPad E490s | [链接](https://github.com/KrauseKurt/e490s-opencore-hackintosh) | | |
| Thinkpad E495 | [链接](https://github.com/EraserCN/ThinkPad-E495-Hackintosh) | | |
| Thinkpad E595 | [链接](https://github.com/EraserCN/ThinkPad-E595-Hackintosh) | | |
| ThinkPad E540                      | [链接](https://github.com/wwbhl/E540)                        |                                                              |                                                              |
| ThinkPad E550                      | [链接](https://github.com/the-braveknight/Lenovo-ThinkPad-E550-DSDT-Patch) | [链接](https://www.tonymacx86.com/threads/guide-lenovo-thinkpad-e550-haswell-using-clover-uefi-10-11.214675/) | E550 四代 CPU                                                |
| ThinkPad E560                      | [链接](https://github.com/rsdev69/Lenovo-E560-Clover)        | [链接](https://www.tonymacx86.com/threads/stable-lenovo-e560-full-work.248842/) |                                                              |
| ThinkPad E570                      | [链接](https://github.com/SysConKonn/E570-Hackintosh)        | [链接](https://www.tonymacx86.com/threads/stable-lenovo-e560-full-work.248842/) |                                                              |
| Lenovo ThinkPad L14 Gen1 | [链接](https://github.com/soft98-top/Lenovo-ThinkPad-L14-Gen1-i7-10510u-Hackintosh) |  | |
| ThinkPad L430                      | [链接](https://github.com/yaza-putu/lenovo-thinkpad-l430)    |                                                              |                                                              |
| ThinkPad L440                      |                                                              |                                                              |                                                              |
| ThinkPad L470                      | [链接](https://github.com/SquarePeace/ThinkPadL470-OpenCoreEFI)  | [链接](https://github.com/SquarePeace/ThinkPadL470-OpenCoreEFI/blob/master/README.md) ||
| ThinkPad L490                      | [链接](https://github.com/twislyn/Hackintosh-ThinkPad-L490)  | [链接](https://github.com/twislyn/Hackintosh-ThinkPad-L490/blob/master/README.md) |                                                              |
| Lenovo miix 520                    | [链接](https://github.com/acai66/lenovo-miix-520-hackintosh-10.14-CLOVER) |                                                              |                                                              |
| Lenovo Rescuer R720-15IKBN         | [链接](https://github.com/happylzyy/Hackintosh-Lenovo-R720)  |                                                              |                                                              |
| Lenovo Thinkpad P1 Gen1 | [链接](https://github.com/p455555555/Thinkpad-P1-EFI) | | |
| ThinkPad P51                       | [链接](https://github.com/MirkoCovizzi/thinkpad-p51-hackintosh) | [链接](https://github.com/MirkoCovizzi/thinkpad-p51-hackintosh/blob/master/README.md) | Thinkpad P51                                                 |
| ThinkPad P52 | [链接](https://github.com/liuyishengalan/ThinkPad-P52-Hackintosh-10.14.X-) [链接](https://github.com/liuyishengalan/ThinkPad-P52-P53-P72-P73-Hackintosh-10.15.x) | | 链接2=P52-P53-P72-P73<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| ThinkPad P15V Gen1                | [链接](https://github.com/ivan19871002/Thinkpad-P15V-Gen1-Hackintosh) |                                                              |                                                              |
| 拯救者 R720                        | [链接](https://github.com/Licoded/R720-15IKBN-EFI)           |                                                              |                                                              |
| 锐 7000                            | [链接](https://github.com/839891627/Lenovo_RUI7000_Hackintosh) |                                                              | 联想 80WB 笔记本电脑                                         |
| ThinkPad S1 2017                   | [链接](https://github.com/bugprogrammer/hackintosh/tree/ThinkPad-S1-2017) |                                                              | ThinkPad S1 2017                                             |
| ThinkPad S1 2018                   | [链接](https://github.com/bugprogrammer/hackintosh/tree/ThinkPad-S1-2018) |                                                              | ThinkPad S1 2018                                             |
| Thinkpad T14 | [链接](https://github.com/nguyenminhhao9988/EFI-thinkpad-T14-gen-2-AMD) | | AMD Ryzen 7 5850U |
| ThinkPad T420 系列                 | [链接](https://github.com/tluck/Lenovo-T420-Clover)          | [链接](https://www.insanelymac.com/forum/topic/285678-lenovo-thinkpad-t420-with-uefi-only/?page=20&tab=comments#comment-1952283) | 包含 T420、T420s、T520、X220X220，<br />可通过修改支持到 10.14.x |
| ThinkPad T430                      | [链接](https://github.com/hai666l/T430-EFI)                  |                                                              |                                                              |
| ThinkPad T430s                     | [链接](https://github.com/hunga1ok/hackintosh-t430si7vga-clover-config) [链接](https://github.com/Xiaoheixu/Thinkpad-T430-s-OpenCorteBootloader) |                                                              |                                                              |
| ThinkPad T440s                     |                                                              |                                                              |                                                              |
| ThinkPad T440p                     | [链接](https://github.com/evy0311/t440p) [链接](https://github.com/jloisel/t440p)<br /> [链接](https://github.com/notthebee/t440p-hackintosh) [链接](https://github.com/VinylNerd/ThinkPad-T440P-OpenCore) | [链接](https://github.com/evy0311/t440p/blob/master/README.md) |                                                              |
| ThinkPad T450                      | [链接](https://github.com/jsassu20/ThinkPad-T450-Mojave)     |                                                              |                                                              |
| ThinkPad T450s                     | [链接](https://github.com/EchoEsprit/Hackintosh-Catalina-OpenCore-Lenovo-T450s-efi) [链接](https://github.com/jianzhao0806/ThinkPad-T450S-Hackintosh)<br />[链接](https://github.com/racka98/Lenovo-Thinkpad-T450-T450s-Hackintosh-Guide-Opencore) [链接](https://github.com/CLAY-BIOS/Lenovo-ThinkPad-T450s-Hackintosh-Big-Sur-OpenCore) |                                                              |                                                              |
| ThinkPad T460 系列                 | [链接](https://github.com/tluck/Lenovo-T460-Clover)          | [链接](http://www.insanelymac.com/forum/topic/315451-guide-lenovo-t460-macos-with-clover/) | 可支持 T460、T560、T470<br /> 和 T470p4 款机型               |
| ThinkPad T460p                     | [链接](https://github.com/totemofwolf/Thinkpad-T460p-OSX-EFI) |                                                              |                                                              |
| ThinkPad T460s                     | [链接](https://github.com/simprecicchiani/Thinkpad-T460s-macOS-OpenCore) |                                                              |                                                              |
| Thinkpad T470                      | [链接](https://github.com/evlon/t470p-oc) [链接](https://github.com/t0mmas0/T470-7300u-Hackintosh) |                                                              | I7-7500u                                                     |
| Thinkpad T470S                     | [链接](https://github.com/Altairko/Lenovo-T470s-Clover) [链接](https://github.com/YBN-JUAN/T470s-OpenCore-EFI) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) `00JT494`联想版 |
| ThinkPad T470p                     | [链接](https://github.com/lohcve/EFI_T470P)                  | [链接](https://github.com/lohcve/EFI_T470P/blob/master/README.md) | ThinkPad T470p                                               |
| ThinkPad T480                      | [链接](https://github.com/rhkjyn/T480-Hackintosh-FULL) [链接](https://github.com/EETagent/T480-OpenCore-Hackintosh) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| ThinkPad T480s                     | [链接](https://github.com/kk1987/T480s-hackintosh) [链接](https://github.com/bdragonh/T480S-BIGSUR-EFI)<br />[链接](https://github.com/bdragonh/T480S-BIGSUR-EFI) | [链接](https://github.com/kk1987/T480s-hackintosh/blob/master/README.md) | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| ThinkPad T480s                     | [链接](https://github.com/kk1987/T480s-hackintosh) <br /> | [链接](https://github.com/kk1987/T480s-hackintosh/blob/master/README.md) | ThinkPad T480s<br />网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| ThinkPad T490                      | [链接](https://github.com/yusifsalam/t490-macos)             |                                                              |                                                              |
| Thinkpad T495 | [链接](https://github.com/EraserCN/ThinkPad-T495-Hackintosh) | | |
| ThinkPad T530                      | [链接](https://github.com/m1qnet/ThinkPad-T530-Hackintosh) [链接](https://github.com/5T33Z0/Lenovo-T530-Hackinosh-OpenCore) |                                                              |                                                              |
| ThinkPad T570                      | [链接](https://github.com/zxr615/ThinkPadT570_EFI)           |                                                              |                                                              |
| ThinkPad T580                      | [链接](https://github.com/CrazyPegAsus/ThinkPad-T580-Hackintosh) |                                                              | 鸣谢：[CrazyPegasus](https://github.com/CrazyPegasus)        |
| Lenovo U330/U430/U530 系列         | [链接](https://github.com/RehabMan/Lenovo-U430-Touch-DSDT-Patch) | [链接](https://www.tonymacx86.com/threads/guide-lenovo-ideapad-u330-u430-u530-using-clover-uefi.261722/) |                                                              |
| Lenovo V1000                       | [链接](https://github.com/LiuJiangshan/Lenovo-V1000-FHD)     |                                                              | 联想小新笔记本 V1000 FHD                                     |
| Lenovo V110-15ISK                  | [链接](https://github.com/ciccio-90/Lenovo_V110-15ISK_Hackintosh_OpenCore_macOS) |                                                              | i3-6006U                                                     |
| Lenovo V3000                       | [链接](https://github.com/Xc2333/Hackintosh-Lenovo-v3000-ISE) | [链接](https://github.com/Xc2333/Hackintosh-Lenovo-v3000-ISE/blob/master/README.md) | Lenovo V3000                                                 |
| Lenovo V310 15iKB                  | [链接](https://github.com/jacobmesier/V310-Hackintosh)       |                                                              |                                                              |
| Lenovo V330 15IKB                  | [链接](https://github.com/Leebais/v330-15ikb-clover)         | [链接](https://www.tonymacx86.com/threads/guide-lenovo-v330-15ikb-using-clover-uefi-hotpatch.265841/) |                                                              |
| Lenovo V730-15IKB                  | [链接](https://github.com/VictorScilifen/LenovoV730-15IKB-Hackintosh) |                                                              |                                                              |
| Lenovo ThinkPad W530               | [链接](https://github.com/nghiant96/EFI-Thinkpad-W530-Hackintosh) |                                                              |                                                              |
| Lenovo-WEI6(威 6)                  | [链接](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh) |                                                              | **Lenovo Thinkbook 13S**                                     |
| Lenovo xiaoxin air13 6th           |                                                              |                                                              | Intel 酷睿 i5 6200U                                          |
| Lenovo XiaoXin Air 13 IWL          | [链接](https://github.com/daliansky/Lenovo-Air13-IWL) [链接](https://github.com/darpaxyz/Lenovo-Air13-IWL-Hackintosh) <br /> | [链接](https://blog.daliansky.net/Lenovo-Xiaoxin-Air-13-macOS-Mojave-installation-tutorial.html) | 联想小新 Air 13 2018 IWL<br />网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Lenovo XiaoXin Air15 IKBR          | [链接](https://github.com/czy1024/XiaoXin-Air15-IKBR-2018-EFI) [链接](https://github.com/wtsjw/XiaoXin-Air15-IKBR-2018-EFI) |                                                              |                                                              |
| Lenovo XiaoXin14 IWL 2019          | [链接](https://github.com/superbboy/Lenovo-XIAOXIN-14-2019-IWL-Hackintosh) |                                                              | 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Lenovo XiaoXin Air 14 2019 IML     | [链接](https://github.com/lietxia/XiaoXinAir14IML_2019_hackintosh) |                                                              | 小新 Air14-2019 IML 10 代 i5-10210u                          |
| Lenovo XiaoXin Pro 13 2019/2020    | [链接](https://github.com/daliansky/XiaoXinPro-13-2019-hackintosh) |                                                              | 联想小新 Pro 2019，网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo XiaoXin Chao 5000           | [链接](https://github.com/Xc2333/Hackintosh-Lenovo-chao5000) [链接](https://github.com/masonsxu/Hackintosh-Lenovo-Chao5000) |                                                              | 联想潮 5000                                                  |
| Lenovo XiaoXin Rui 7000            | [链接](https://github.com/Erf172/Lenovo_XiaoXin_Rui7000_Hackintosh) | [链接](https://github.com/Erf172/Lenovo_XiaoXin_Rui7000_Hackintosh/blob/10.12/README.md) |                                                              |
| Lenovo XiaoXin Chao 7000           | [链接](https://github.com/periky/lenovo-xiaoxinchao7000-14ikbr-efi) |                                                              | 联想小新潮 7000，已支持 14 寸、<br />12.5 寸、13.3 寸，15 寸以及 <br />13.3 寸的完美支持后续会添加，<br />请期待…… |
| Lenovo XiaoXin V4000               | [链接](https://github.com/IBeliveDream/i7-5500u-macos)       |                                                              |                                                              |
| Lenovo Xiaoxin-15ARE 2020 | [链接](https://github.com/Zrc00/Lenovo-Xiaoxin-15ARE-AMD-4800U-Hackintosh) | | AMD 4800U |
| ThinkBook 13s G3 | [链接](https://github.com/HornHon/ThinkBook-13s-G3-ACN-OpenCore) | | AMD 5600U |
| ThinkPad X1 3rd                    | [链接](https://github.com/shockingpants/ThinkpadX1Y3) [链接](https://github.com/daipham31/ThinkPadX1-Gen3-EFI-Catalina)<br />[链接](https://github.com/CLAY-BIOS/Lenovo-ThinkPad-T450s-Hackintosh-Big-Sur-OpenCore) | [链接](https://www.tonymacx86.com/threads/guide-thinkpad-x1-yoga-3rd-gen-20ld-with-mojave.261823/) | ThinkPad X1 3 代                                             |
| ThinkPad X1 Carbon 2015            | [链接](https://github.com/transtone/hackintosh/tree/master/x1c-2015) [链接](https://github.com/Derekxxzzyy/Thinkpad-X1-Carbon-3rd-Hackintosh-OC-EFI) <br />[链接](https://github.com/CLAY-BIOS/Lenovo-ThinkPad-T450s-Hackintosh-Big-Sur-OpenCore) |                                                              |                                                              |
| ThinkPad X1 Carbon 2016            | [链接](https://github.com/lzjqsdd/Thinkpad-X1C4-Hackintosh)  |                                                              | ThinkPad X1 Carbon 4th Gen                                   |
| ThinkPad X1 Carbon 5th gen         | [链接](https://github.com/B0hrer/Thinkpad-x1c-5th-gen-Hackintosh) |                                                              | (5th gen, released 2017)                                     |
| ThinkPad X1 Carbon 6th Gen         | [链接](https://github.com/tylernguyen/x1c6-hackintosh) [链接](https://github.com/RyoIkarashi/hackintosh-x1c6-with-native-wifi-card)<br />[链接](https://github.com/kushwavez/lenovo-x1c6-clover-efi) | [链接](https://github.com/tylernguyen/x1c6-hackintosh/blob/master/README.md) | Thinkpad X1 Carbon 6th Gen                                   |
| ThinkPad X1 Yoga / Carbon          | [链接](https://github.com/LukaJankovic/Thinkpad-X1-20FQ-Hackintosh) | [链接](https://github.com/LukaJankovic/Thinkpad-X1-20FQ-Hackintosh/blob/master/README.md) | Thinkpad X1 Yoga / Carbon                                    |
| ThinkPad X1 Yoga 2018              | [链接](https://github.com/Jamesxxx1997/thinkpad-x1-yoga-2018-hackintosh) |                                                              |                                                              |
| ThinkPad X1 Extreme                | [链接](https://github.com/Errrneist/Hackintosh-Thinkpad-X1-Extreme) [链接](https://github.com/zysuper/Thinkpad-X1-extreme-EFI) | [链接](https://www.tonymacx86.com/threads/macos-10-14-0-thinkpad-x1-extreme-igpu-issue.263916/) | 如果没猜错，这货就是 x1 隐士，<br />好几个人问过，这下省事了 |
| ThinkPad X1C 6th                   | [链接](https://github.com/tylernguyen/x1c6-hackintosh)       | [链接](https://github.com/tylernguyen/x1c6-hackintosh/blob/master/README.md) | ThinkPad X1c 6th                                             |
| Thinkpad X1 Carbon Gen 7           | [链接](https://github.com/aidanchandra/x1c7-hackintosh)      |                                                              |                                                              |
| Thinkpad X1 Carbon Gen 8           | [链接](https://github.com/gammons/laptop-hackintosh-efi)     |                                                              |                                                              |
| ThinkPad X13                     | [链接](https://github.com/shuai132/ThinkPad-X13-EFI)                                                                                                                                                                                                                                                                                |                                                                                                                                                               | i5-10210u                                                                         |
| ThinkPad X220                      | [链接](https://github.com/b-ggs/x220-hackintosh)             | [链接](https://github.com/b-ggs/x220-hackintosh/blob/master/README.md) | 支持 10.14+                                                  |
| ThinkPad X220                      | [链接](https://github.com/laris/Hackintosh-ThinkPad-X220-MacOS) |                                                              | ThinkPad-X220                                                |
| ThinkPad X230                      | [链接](https://github.com/littlegtplr/Hackintosh-X230-macOS) [链接](https://github.com/mighildotcom/X230-Hackintosh) | [链接](https://github.com/littlegtplr/Hackintosh-X230-macOS/blob/master/README.md) | ThinkPad X230                                                |
| ThinkPad X230                      | [链接](https://github.com/banhbaoxamlan/X230-Hackintosh)     |                                                              | ThinkPad X230                                                |
| ThinkPad X230i                     | [链接](https://github.com/fivestrong/Hackintosh-X230i-macOS) |                                                              |                                                              |
| ThinkPad X250                      | [链接](https://github.com/Janolan/x250-hackintosh) [链接](https://github.com/qwerty12/X250-Hackintosh) [链接](https://github.com/teddytaod/mac-catalina-thinkpad-x250) [链接](https://github.com/CLAY-BIOS/Lenovo-ThinkPad-T450s-Hackintosh-Big-Sur-OpenCore) |                                                              |                                                              |
| ThinkPad X260 系列                 | [链接](https://github.com/daliansky/ThinkPad-X260-hackintosh) | [链接](https://github.com/daliansky/ThinkPad-X260-hackintosh/blob/master/README.md) | ThinkPad X260<br />网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Thinkpad x390-yoga                 | [链接](https://github.com/Liu-wenxiang/Thinkpad-X390-Yoga-Clover) |                                                              |                                                              |
| ThinkPad X390                      | [链接](https://github.com/mendax1234/ThinkpadX390-Opencore-EFI) | [链接](http://bbs.pcbeta.com/viewthread-1852139-1-1.html)    | ThinkPad X390(39CD)                                          |
| Lenovo Y50(70) 系列                | [链接](https://github.com/RehabMan/Lenovo-Y50-DSDT-Patch) <br />[链接](https://github.com/GeekyCoder7/OpenCore-EFI-Lenovo-Y50-70) | [链接](https://www.tonymacx86.com/threads/guide-lenovo-y50-uhd-or-1080p-using-clover-uefi.261723/) | Y50(70)1080P 和 4K 版本<br />网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Lenovo IdeaPad 530s                | [链接](https://github.com/corint1/Hackintosh-Lenovo-IdeaPad-530s-14ikb) |                                                              | 感谢：[39 军小兵张](http://i.pcbeta.com/space-uid-4472739.html) |
| Lenovo Ideapad S340/S540           | [链接](https://github.com/IvanAleksandrov94/Lenovo-s340-s540-Big-Sur-OpenCore-i5-8265u) |                                                              |                                                              |
| Lenovo IdeaPad Y410P               | [链接](https://github.com/Z39/Y410p-OS-X-Clover-Hotpatch)    |                                                              | 感谢：[39 军小兵张](http://i.pcbeta.com/space-uid-4472739.html) |
| Lenovo IdeaPad Y430P               | [链接](https://github.com/Z39/Y430p-OS-X-Clover-Hotpatch)    |                                                              | 感谢：[39 军小兵张](http://i.pcbeta.com/space-uid-4472739.html) |
| Lenovo IdeaPad Y510P               | [链接](https://github.com/Z39/Y510p-OS-X-Clover-Hotpatch)    |                                                              | 感谢：[39 军小兵张](http://i.pcbeta.com/space-uid-4472739.html) |
| Lenovo Y520/Y720                   | [链接](https://github.com/the-braveknight/Lenovo-Y520-macOS) [链接](https://github.com/adrianjagielak/lenovo_y520_efi) | [链接](https://www.tonymacx86.com/threads/guide-lenovo-legion-y520-y720-using-clover-uefi.261009/) | 联想 Y520 及 Y720                                            |
| Lenovo Legion 5 17ACH6H | [链接](https://github.com/danielrumata/Legion-5800H-Hackintosh) |  | AMD Ryzen 5800H & NVIDIA RTX 3060 |
| Legion 5 15IMH05a                | [链接](https://github.com/abhishek110022/Legion-5-15IMH05a-Hackintosh)                                                                                                                                                                                                                                                              |                                                                                                                                                               |                                                                                   |
| Legion 5 15ARH05H | [链接](https://github.com/Aliezan/Legion-5-15ARH05H-EFI) | | **AMD RYZEN7 4800H** |
| Lenovo Legion 5i                   | [链接](https://github.com/LuckyCrack/Legion-5i-EFI) [链接](https://github.com/abhishek110022/Legion-5-15IMH05a-Hackintosh) |                                                              | i5-10300H                                                    |
| Lenovo Legion Y520                 | [链接](https://github.com/adrianjagielak/lenovo_y520_efi)    |                                                              |                                                              |
| Lenovo Legion Y530                 | [链接](https://github.com/adrianjagielak/lenovo_y530_efi)    |                                                              |                                                              |
| Lenovo Legion Y545                 | [链接](https://github.com/indowebdeveloper/LegionY545_BigSur) |                                                              |                                                              |
| Lenovo Y700-17ISK | [链接](https://github.com/thedaveesky/lenovo-y700-hackintosh) | | |
| Lenovo Legion Y7000                | [链接](https://github.com/hnie-xwz/EFI)                      | [链接](https://github.com/hnie-xwz/EFI/blob/macOs10.14/readme.md) | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo Legion Y7000-1060           | [链接](https://github.com/TioaTyan/Lenovo_Legion_Y7000-1060_Hackintosh) | [链接](https://github.com/TioaTyan/Lenovo_Legion_Y7000-1060_Hackintosh/blob/master/README.md) | Lenovo_Legion_Y7000-1060                                     |
| Lenovo Legion Y7000<br />Y530 系列 | [链接](https://github.com/xiaoMGitHub/Lenovo_Y7000-Y530_Hackintosh/) [链接](https://github.com/ahossny/Legion-Y530-Hackintosh) |                                                              | 全新完美 EFI，舍弃了小键盘                                   |
| Lenovo Y7000P 81T1                 | [链接](https://github.com/gclm/Hackintosh-LEGION-Y7000P-I7-9750H) |                                                              | I7-9750H                                                     |
| Lenovo Y9000X                      | [链接](https://github.com/programbw/y9000x) [链接](https://github.com/hsd815/Y9000X-4K-hackintosh) [链接](https://github.com/WangRicky/Y9000X-HACKINTOSH) [链接](https://github.com/snxiang/Y9000X-Hackintosh-FHD-OpenCore) |                                                              | 支持 CNVi 直插 m.2 网卡，网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo R9000P | [链接](https://github.com/EricMoin/R9000P2021-AMD5800H-Hackintosh) | | AMD 5800H |
| Lenovo Y9000X 2020                 | [链接](https://github.com/Corazon0513/Y9000X-2020-i9-Hackintosh) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo Yoga 3 Pro 1370             | [链接](https://github.com/gdllzkusi/hackintosh--lenovo-Yoga-3-Pro-1370) | [链接](https://github.com/gdllzkusi/hackintosh--lenovo-Yoga-3-Pro-1370/blob/master/README.md) | 联想 yaga3/pro                                               |
| ThinkPad Yoga 12                   | [链接](https://github.com/gartempe/MacOS-Thinkpad-Yoga-12) [链接](https://github.com/kymodoke/MacOS-Thinkpad-Yoga-12) | [链接](https://github.com/gartempe/MacOS-Thinkpad-Yoga-12/blob/master/README.md) [链接](https://github.com/kymodoke/MacOS-Thinkpad-Yoga-12/blob/master/README.md) |                                                              |
| Thinkpad S1 Yoga 12                | [链接](https://github.com/Huarch/Thinkpad-S1-yoga12-Hackintosh) [链接](https://github.com/tidelust/OC-ThinkPad-Yoga-12) | [链接](https://github.com/Huarch/Thinkpad-S1-yoga12-Hackintosh) |                                                              |
| Lenovo Yoga3 14                    |                                                              |                                                              |                                                              |
| Lenovo Yoga3 11                    |                                                              |                                                              |                                                              |
| Lenovo Yoga 13IKB                  | [链接](https://github.com/dragonflylee/Yoga13-Hackintosh)    |                                                              |                                                              |
| Lenovo Yoga 370                    | [链接](https://github.com/ouxuebo/YOGA370-clover) [链接](https://github.com/geoleonsh/clover-EFI-yoga-370) |                                                              |                                                              |
| Lenovo Yoga X390 | [链接](https://github.com/Chitpixel/X390-OC-EFI) | | |
|  |  | | |
| Lenovo Yoga 520 14IKB              | [链接](https://github.com/gasperTheGhost/Yoga-520-Hackintosh) |                                                              |                                                              |
| Lenovo Yoga 710-14isk 80TY         | [链接](https://github.com/yutayouguan/EFI)                   |                                                              | i5-6200U                                                     |
| Lenovo Yoga 710                    | [链接](https://github.com/xiaoxx970/Hackintosh-Mojave-for-Lenovo-Yoga710) [链接](https://github.com/newham/yoga710-7500u-oc-bigsur)<br />[链接](https://github.com/newham/yoga710-7500u-oc-bigsur) |                                                              |                                                              |
| Lenovo Yoga 720                    | [链接](https://github.com/bugprogrammer/hackintosh/tree/Lenovo-yoga-720-13ikb-7200u) |                                                              | Lenovo Yoga 720-13IKB                                        |
| Lenovo Yoga 720                    |                                                              |                                                              | Lenovo Yoga 720-12IKB                                        |
| Lenovo Yoga 730                    | [链接](https://github.com/dragonflylee/Yoga-730-hackintosh)  |                                                              | Lenovo Yoga 730-13IKB                                        |
| Lenovo Yoga C740-14IML             | [链接](https://github.com/ThrRip/OpenCore-EFI-Laptop-Lenovo-YOGA-C740-14IML) [链接](https://github.com/Carlosjavierdlp/C740-14iml-BigSur) |                                                              |                                                              |
| Lenovo Yoga S740                   | [链接](https://github.com/frozenzero123/YOGA-S740)           |                                                              | i7 1065G7                                                    |
| Lenovo Yoga 910 13IKB              | [链接](https://github.com/wjz304/Hackintosh-EFI-Lenovo-Yoga-910-13IKB) |                                                              |                                                              |
| Lenovo Yoga Duet 2020 | [链接](https://github.com/eenie/YogaDuet-Hackintosh-EFI-OC) | | |
| Lenovo Z50(40)/70 系列             | [链接](https://github.com/the-braveknight/Lenovo-X50-macOS)  | [链接](https://www.tonymacx86.com/threads/guide-lenovo-z50-70-z40-70-g50-70-g40-70-using-clover-uefi.261787/) | Lenovo Z50-70/Z40-70 Lenovo G50-70/G40-70                    |
| Lenovo Miix510                     | [链接](https://github.com/Aexus/hackintosh-ideapad-miix510) [链接](https://github.com/liuwaei/Lenovo-Miix510-EFI-Clover-for-MacOS-10.14.X) |                                                              | Lenovo-Miix510                                               |
| Lenovo Miix-520                    | [链接](https://github.com/acai66/lenovo-miix-520-hackintosh-10.14-CLOVER) | [链接](https://github.com/acai66/lenovo-miix-520-hackintosh-10.14-CLOVER) | Lenovo-Miix-520                                              |
| Lenovo Miix4                       |                                                              |                                                              | Lenovo-Miix4（700）                                          |
| Lenovo Miix720                     | [链接](https://github.com/jennie26/Lenovo-Miix-720-Hackintosh) |                                                              |                                                              |
| Thinkstation P910                  | [链接](https://github.com/crazyi/Hackintosh_Thinkstation_P910) |                                                              |                                                              |
| Lenovo Yoga 920 13IKB              | [链接](https://github.com/qxuchn/YOGA920-Hackintosh)         |                                                              |                                                              |
| Lenovo Z410                        | [链接](https://github.com/chencaidy/Hackintosh-OC-Lenovo-Z410) |                                                              |                                                              |

### LG

| 机型名称               | 发布地址                                                     | 教程地址 | 备注     |
| ---------------------- | ------------------------------------------------------------ | -------- | -------- |
| LG Gram 13z980         | [链接](https://github.com/suzuke/LG-Gram-13z980-Opencore)    |          | OC       |
| LG 14U53               | [链接](https://github.com/vivzero/LG14u53-hackintosh)        |          |          |
| LG Gram 14Z90N         | [链接](https://github.com/vivzero/LG-14Z90N-hackintosh)      |          |          |
| LG Gram 14z980         | [链接](https://github.com/ShiningXu/LG-Gram-macOS)           |          |          |
| LG Gram14 Z990         | [链接](https://github.com/myd986/LG-gram-14z990)             |          |          |
| LG Gram 15Z980-G.AA52C | [链接](https://github.com/ice-black-tea/LG-15Z980)           |          |          |
| LG Gram17 Z90n         | [链接](https://github.com/whca/lg-gram-17z90n-EFI) [链接](https://github.com/AskDavis/LG-Gram-17Z90N) |          | OC 0.6.9 |
| LG Gram Z980           | [链接](https://github.com/ShiningXu/LG-Gram-macOS)           |          |          |

### Mechrevo 机械革命

| 机型名称                 | 发布地址                                                                                               | 教程地址                                                           | 备注                                |
| ------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------ | ----------------------------------- |
| Mechrevo Z2              | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo Z2 Air          | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo X8ti            | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo X8ti Plus       | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo S1              | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh) [链接](https://github.com/lgs3137/MR_S1-macOS) | [链接](https://github.com/lgs3137/MR_S1-macOS/tree/master/Install) | I5-8250U/I7-8550u Mx150             |
| Mechrevo S1              | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | I5-8265U/I7-8565u Mx250             |
| Mechrevo X2              | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo S1 PLUS         | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo X7TI            | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | I7-6700HQ/I7 7700HQ                 |
| Mechrevo X7TI-S          | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | I7-7700HQ GTX1070/GTX1060           |
| Mechrevo X6TI            | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-8750H/i5-8300H GTX1050ti/GTX1060 |
| Mechrevo X6TIS           | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    |                                     |
| Mechrevo X1              | [链接](https://github.com/cmbs2019/Mechrevo-Hackintosh)                                                |                                                                    | i7-7700HQ/GTX1060                   |
| Mechrevo Z2 / X8Ti 系列  | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)                                              | [链接](https://www.bilibili.com/video/av81263778)                  | 准系统型号：同方 GK5CN6Z/GK5CN5Z    |
| Mechrevo Z2 Air          | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)                                              | [链接](https://www.bilibili.com/video/av81263778)                  | 准系统型号：同方 GK5CN6X/GK5CN5X    |
| Mechrevo Z2-G / Z2 Air-G | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)                                              | [链接](https://www.bilibili.com/video/av81263778)                  | 准系统型号：同方 GK5CP6X/GK5CP5X    |
| Mechrevo X3              | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)                                              | [链接](https://www.bilibili.com/video/av81263778)                  | 准系统型号：同方 GK7CP6R            |
| 机械革命 Umi Pro 2       | [链接](https://github.com/Xhichn/Hackbook_MECHREVO_Umi_Pro_II)                                         |                                                                    |                                     |

### MSI 微星

| 机型名称                  | 发布地址                                                                                                                                                                                                  | 教程地址                                                                             | 备注            |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | --------------- |
| MSI GE60 2OC/2OD/2OE      | [链接](https://github.com/xusos/Hackintosh-EFI)                                                                                                                                                           |                                                                                      |                 |
| MSI GE60 2PL-403XCN       | [链接](https://github.com/ice-black-tea/MSI-GE60) [链接](https://github.com/cs950809/MSI-GE60-2PL-403XCN-Hackintosh)                                                                                      |                                                                                      |                 |
| MSI GE63 Raider RGB 8RE   | [链接](https://github.com/skyline75489/Hackintosh-MSI-GE63-Raider-RGB-8RE)                                                                                                                                |                                                                                      |                 |
| MSI GE70 2OE              | [链接](https://github.com/psety/MSI-GE70-2OE-Catalina-Hackintosh)                                                                                                                                         |                                                                                      |                 |
| MSI GE70 2PC              | [链接](https://github.com/alxzoomer/msi-ge70-2pc-hackintosh)                                                                                                                                              |                                                                                      |                 |
| MSI GE72 2QE              | [链接](https://github.com/ksmrp/msi-ge70-2qe-hackintosh)                                                                                                                                                  |                                                                                      |                 |
| MSI GE72VR Apache Pro-416 |                                                                                                                                                                                                           |                                                                                      |                 |
| MSI GF63                  | [链接](https://github.com/oscarrock/hackintosh-msi-gf63-thin-9SC)                                                                                                                                         |                                                                                      |                 |
| MSI GF63 8RD | [链接](https://github.com/yasinerarslan/GF63.8RD.Hackintosh.OpenCore) | | |
| MSI GF63 9SCSR 846VN | [链接](https://github.com/estherowo/MSI-GF63-9SCSR-846VN-OpenCore) | | |
| MSI GF63-10               | [链接](https://github.com/rohanbojja/MSI-GF-63-10)                                                                                                                                                        |                                                                                      |                 |
| MSI GF63 thin 9sc         | [链接](https://github.com/LongBody/EFi-Hackintosh-MSi-GF63-thin-9sc)                                                                                                                                      |                                                                                      |                 |
| MSI GF75                  | [链接](https://github.com/PeenkLion/Laptop-Hackintosh-EFI)                                                                                                                                            |                                                                                                                                            |                 |
| MSI GL62M 7RD             | [链接](https://github.com/0ranko0P/GL62M-7RD-Hackintosh)                                                                                                                                                  |                                                                                      |                 |
| MSI GL62M 7RDX            | [链接](https://github.com/ForceGT/Hackintosh--MSIGL62M-7RDX)                                                                                                                                              |                                                                                      |                 |
| MSI GL62M 7REX            | [链接](https://github.com/rlindsberg/Hackintosh-On-MSI-GL62m-7REX)                                                                                                                                        |                                                                                      |                 |
| MSI GL 63-8RC             | [链接](https://github.com/devendramilmile121/msigl638rc-hackintosh-efi)                                                                                                                                   |                                                                                      |                 |
| MSI GL63-8RE              |                                                                                                                                                                                                           |                                                                                      |                 |
| MSI GL65 Leopard 9SCXR | [链接](https://github.com/dushan12k/msi-gl65-leopard-9scxr-) | | |
| MSI GL72M-7RDX            | [链接](https://github.com/jbwharris/hackintosh-msi-GL72M-7RDX)                                                                                                                                            | [链接](https://github.com/jbwharris/hackintosh-msi-GL72M-7RDX/blob/master/README.md) |                 |
| MSI GP62 6QG-1071XCN      | [链接](https://github.com/chuxubank/MSI-GP62-Hackintosh)                                                                                                                                                  |                                                                                      | 微星 GP62       |
| MSI GP76 10th      | [链接](https://github.com/y010204025/MSI_GP76_10th_macOS)  |                                                                                      | 微星 GP76 10th,可能还适用于GT76、GE76、GE66、GS66等9代、10代机型，未测试，可以尝试在这基础上修改       |
| MSI GS63VR-7RF            | [链接](https://github.com/guitaoliu/MSI-GS63VR-Hackintosh)                                                                                                                                                |                                                                                      |                 |
| MSI GS65	|[链接](https://github.com/charlesSheep/-gs65-opencore-eif#msi-gs65-261n-opencore-eif)	|[GS75](https://github.com/ErrorErrorError/msi-gs65-gs75-hackintosh) [GS75](https://github.com/ErrorErrorError/msi-gs65-8se-opencore-macos)	|		|
| MSI GS65 Stealth Thin 8RF | [链接](https://github.com/vladichimescu/msi-gs65-hackintosh)                                                                                                                                              |                                                                                      |                 |
| MSI GS65 8SE              | [链接](https://github.com/ErrorErrorError/msi-gs65-8SE-hackintosh)                                                                                                                                        |                                                                                      |                 |
| MSI GS65 9SE | [链接](https://github.com/gkShine/MSI_GS65_9SE_EFI) | | |
| MSI GS66 Stealth | [链接](https://github.com/zhujinle/MSI-GS66-Stealth-OC-Hackintosh) | | |
| MSI GS73VR 7RF            | [链接](https://github.com/dogukanoksuz/msi-gs73vr-7rf-macOS)                                                                                                                                              |                                                                                      |                 |
| MSI GT60 16F4 | [链接](https://github.com/lakent/MSI-16F4-Hackintosh) | | |
| MSI GV62 7RE              | [链接](https://github.com/amogh-w/Hackintosh-MSI-GV62-7RE)                                                                                                                                                |                                                                                      |                 |
| MSI Modern 15 A10M        | [链接](https://github.com/hla63/Msi-modern-15-Hackintosh) [链接](https://github.com/AndresGarciaSobrado91/MSI-Modern15-Hackintosh)                                                                        |                                                                                      |                 |
| MSI Modern 15 A5M         | [链接](https://github.com/saeidex/ryzentosh-msi-modern-15)                                                                                                                                                |                                                                                      | AMD Ryzen 5 5500u |
| MSI PL62 7RC              | [链接](https://github.com/juanlatorre/MSI-PL62-7RC-OC-Hackintosh)                                                                                                                                         |                                                                                      | Intel i5-7300HQ |
| MSI Prestige 15           | [链接](https://github.com/KerKerOgh/MSI-Prestige-15-Hackintosh) [链接](https://github.com/wgjas2/MSI-Prestige-15-Hackintosh)<br />[链接](https://github.com/naturalBlacksmith/hackintosh-msi-prestige-15) |                                                                                      |                 |
| MSI PS63 Modern 8RC       |                                                                                                                                                                                                           |                                                                                      |                 |


### Razer Blade 雷蛇

| 机型名称                           | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Razer Blade 15 Base Model          | [链接](https://github.com/DocSystem/razerbladehackintosh) [链接](https://github.com/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur) | [链接](https://github.com/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur) | 链接 2 支持`Big Sur`                                         |
| Razer Blade Stealth 雷蛇灵刃潜行版 | [链接](https://github.com/widmonstertony/razer-blade-stealth-hackintosh) |                                                              |                                                              |
| Razer Blade 15 Advanced            | [链接](https://github.com/doanhmaple/Razer-Blade-15-Advanced-2018-Hackintosh) [链接](https://github.com/Errrneist/Hackintosh-Razer-Blade-Advanced) |                                                              | i7-8750H 网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| Razer_Blade_Advanced_early_2019    | [链接](https://github.com/stonevil/Razer_Blade_Advanced_early_2019_Hackintosh) |                                                              | [链接](https://github.com/stonevil/Razer_Blade_Advanced_early_2019_Hackintosh) |
| Razer Blade 17 Pro 2020            | [链接](https://github.com/steelbrain/razer-blade-17-pro-2020-hackintosh) |                                                              |                                                              |

### Samsung 三星

| 机型名称                        | 发布地址                                                     | 教程地址 | 备注 |
| ------------------------------- | ------------------------------------------------------------ | -------- | ---- |
| 三星 Samsung NP300E4C           |                                                              |          |      |
| 三星 Samsung NP300E5L           | [链接](https://github.com/bearkfear/SAMSUNG-NP300E5L-HACKINTOSH) |          |      |
| 三星 Samsung NP300E5M           |                                                              |          |      |
| 三星 Samsung NP350U-2B          | [链接](https://github.com/rahmanhadi/EFI-Clover_SAMSUNG-NP350U) |          |      |
| 三星 Samsung NP350XAA-KF3BR     | [链接](https://github.com/augustoperes1/Hackintosh-Essentials-E30-Open-Core) |          |      |
| 三星 Samsung NP900X3L(NT900X3L) | [链接](https://github.com/justiceserv/NT900X3L-Hackintosh)   |          |      |
| Samsung NT350XCR-AD5AS          | [链接](https://github.com/PKRN0/Samsung-NT350XCR-AD5AS-Opencore) |          |      |
| 三星 Samsung NP950XCR-G58A      | [链接](https://github.com/wei756/NT950XCR-G58A-Hackintosh/blob/master/README-en.md) |          |      |

### Shinelon 炫龙

| 机型名称                       | 发布地址                                                                                         | 教程地址                                                                                | 备注                                                                                                            |
| ------------------------------ | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| 炫龙 A40L-i7                   | [链接](https://github.com/i0Ek3/Hackintosh_4_Hasee_Shinelon_A40L)                                | [链接](https://github.com/i0Ek3/Hackintosh_4_Hasee_Shinelon_A40L/blob/master/README.md) |                                                                                                                 |
| 炫龙 耀 7000                   | [链接](https://github.com/jinmu333/Shinelon_YAO_7000_efi)                                        | [链接](https://github.com/jinmu333/Shinalon_YAO_7000_efi/blob/efi/README.md)            | 准系统型号：同方 GK5CN5X, by @jinmu333                                                                          |
| 炫龙 耀 7000                   | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)                                        | [链接](https://www.bilibili.com/video/av81263778)                                       | 准系统型号：同方 GK5CN5X, by @kirainmoe                                                                         |
| 炫龙 耀 9000-II                | [链接](https://github.com/kirainmoe/hasee-tongfang-macos)                                        | [链接](https://www.bilibili.com/video/av81263778)                                       | 准系统型号：同方 GK5CN6X                                                                                        |
| 神舟战神 X5<br />炫龙阿尔法 L9 | [链接](https://github.com/Raysamatoken/macOS-HaseeX5-ShinelonL9)                                 |                                                                                         |                                                                                                                 |
| 炫龙毒刺 X6                    | [链接](https://github.com/JS1993/Shinelon-X6-EFI)                                                |                                                                                         |                                                                                                                 |
| 炫龙 T3TI                      | [链接](https://github.com/283330601/shinelon-t3ti-Hackintosh)                                    |                                                                                         | 9750H+1660TI                                                                                                    |
| Shinelon T50TI                 | [链接](https://github.com/LINGJP/Hackintosh-Shinelon-T50TI-EFI)                                  |                                                                                         |                                                                                                                 |
| 炫龙 DC/DD                     | [链接](https://github.com/JoyZgq/EFI-For-CLEVO_W650dd)                                           |                                                                                         | 蓝天 W650dc，蓝天 W650dd                                                                                        |
| 炫龙 DC2/DD2                   | [链接](https://github.com/bavelee/DC2_Hackintosh) [链接](https://github.com/yuedashen88/DC2_EFI) | [链接](https://bavelee.cn/index.php/archives/60/)                                       | 准系统型号：蓝天 NB50/60 TJ1/TK1 <br> yuedashen88 基于大佬 BaveLee 之前的 EFI 的修改版本,修复了 HDMI 热插拔问题 |
| 炫龙 KP3 Plus                  | [链接](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1843619&highlight=%C9%F1%D6%DB)        |                                                                                         | 准系统型号：蓝天 N960TC                                                                                         |

### Toshiba 东芝 

| 机型名称                      | 发布地址                                                     | 教程地址 | 备注 |
| ----------------------------- | ------------------------------------------------------------ | -------- | ---- |
| Toshiba B654L                 | [链接](https://github.com/yxb2018/toshiba-B654L-clover-efi)  |          |      |
| Toshiba L55W C5320            | [链接](https://github.com/martinmenchon/Hackintosh-Toshiba-L55W-C5320) |          |      |
| Toshiba Satellite C805        | [链接](https://github.com/nan1jueze/TOSHIBA-C805-HM76-CLOVER-Hackintosh) |          |      |
| Toshiba L840                  | [链接](https://github.com/dickymuliafiqri/EFI-Toshiba-L840-OC) |          |      |
| Toshiba Satelite Pro L850-1UJ | [链接](https://github.com/soup-bowl/Toshiba-L850-macOS-EFI)  |          |      |


### XiaoMi 小米

| 机型名称             | 发布地址                                                                                                                                | 教程地址                                                                                                    | 备注                                                                                                        |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Mi Notebook 14 2020  | [链接](https://github.com/itsdrnoob/Mi-NoteBook-14-Hackintosh)                                                                          |                                                                                                             | Intel Core i5-10210U / i3-10110U                                                                            |
| XiaoMi Air 2019      | [链接](https://github.com/szpinc/Hacintosh_MiBookAir13.3_i5-8250U_with_10.13.5)                                                         |                                                                                                             |                                                                                                             |
| XiaoMi Air           | [链接](https://github.com/billhhh/MiAir-Hackintosh)                                                                                     | [链接](https://github.com/billhhh/MiAir-Hackintosh/blob/master/README.md)                                   | XiaoMiAir_i7 7500u                                                                                          |
| XiaoMi Air           | [链接](https://github.com/johnnync13/Xiaomi-Mi-Air)                                                                                     | [链接](https://github.com/johnnync13/Xiaomi-Mi-Air/blob/master/README.md)                                   | 小米 Air                                                                                                    |
| XiaoMi Air           | [链接](https://github.com/ourfor/Mibook-air)                                                                                            | [链接](https://github.com/ourfor/Mibook-air/blob/master/README.md)                                          | 小米 Air                                                                                                    |
| XiaoMi Air           | [链接](https://github.com/whtiehack/XiaoMi-Air)                                                                                         |                                                                                                             |                                                                                                             |
| XiaoMi Air           | [链接](https://github.com/johnnync13/Xiaomi-Notebook-Air-6200u)                                                                         | [链接](https://github.com/johnnync13/Xiaomi-Notebook-Air-6200u/blob/master/README.md)                       | 小米 Notebook Air                                                                                           |
| XiaoMi Air           | [链接](https://github.com/whtiehack/XiaoMi-Air)                                                                                         | [链接](https://github.com/whtiehack/XiaoMi-Air/blob/master/README.md)                                       | XiaoMi NoteBook Air                                                                                         |
| XiaoMi Air 1gen      | [链接](https://github.com/johnnync13/Xiaomi-Notebook-Air-1Gen)                                                                          |                                                                                                             |                                                               |
| XiaoMi Air Skylake   | [链接](https://github.com/johnnync13/EFI_XIAOMI_NOTEBOOK_AIR_SKYLAKE)                                                                   | [链接](https://github.com/johnnync13/EFI_XIAOMI_NOTEBOOK_AIR_SKYLAKE/blob/master/README.md)                 |                                                                                                             |
| XiaoMi Air Kabylake  | [链接](https://github.com/jasper-wan/Xiaomi-Air-i5-7200U)                                                                               |                                                                                                             | Xiaomi Notebook Air 13.3 i5-7200U 指纹版                                                                    |
| XiaoMi Gaming        | [链接](https://github.com/johnnync13/XiaomiGaming)                                                                                      |                                                                                                             |                                                                                               |
| XiaoMi Pro 系列      | [链接](https://github.com/daliansky/XiaoMi-Pro/releases)                                                                                | [链接](https://blog.daliansky.net/MacOS-installation-tutorial-XiaoMi-Pro-installation-process-records.html) | 小米 Pro 系列                                                                                               |
| XiaoMi Ruby 15.6    | [链接](https://github.com/Jxh98/XiaoMi-Ruby-15.6-2019) [链接](https://github.com/XenOriginal/XiaoMi-Ruby-15.6-UMA-only) |                                                              | 目前ALC256声卡外放无法驱动<br />网卡推荐：[DW1820A](https://hackintosher.taobao.com) |
| XiaoMi 游戏本 8 代  | [链接](https://github.com/daliansky/XiaoMi-GLP)              |                                                              |                                              |
| XiaoMi Air          | [链接](https://github.com/hevervie/Hackintosh_XIAOMI_AIR-13.3) |                                                              |                 |
| XiaoMi Air           | [链接](https://github.com/wilsonnkwan/Hackintosh-Xiaomi-Air-13.3-2018-Catalina)                                                         |                                                                                                             |                                                                                                             |
| XiaoMi Air 13.3      | [链接](https://github.com/teojs/Xiaomi-Air-i7-8550u-EFI)                                                                                |                                                                                                             | i7-8550U                                                                                                    |
| 红米 redmibook mx250 | [链接](https://github.com/ming1234jpi/hackintosh_redmibook)                                                                             |                                                                                                             | i5-8265u、i7-8650u                                                                                          |
| 红米 G               | [链接](https://github.com/Xhichn/Hackbook_Redmi_G)                                                                                      |                                                                                                             |                                                                                                             |
| Redmibook14 增强版   | [链接](https://github.com/haoey/-)                                                                                                      |                                                                                                             |                                                                                                             |
| RedmiBook14II | [链接](https://github.com/codeMauguin/RedmiBook14II-i5-1035G1-EFI) | | i5-1035G1 |
| Xiaomi Redmibook 16  | [链接](https://github.com/elishevatavori/Xiaomi-Redmibook-16-Hackintosh)                                                                |                                                                                                             | i7-1065G7                                                                                                   |
| Redmibook 14 XMA1901-AI | [链接](https://github.com/THLIVSQAZ/Redmibook14-XMA1901-AI-OpenCore) |            | i5-8250u|

### Intel 英特尔

| 机型名称                                            | 发布地址                                                                                                                           | 教程地址                                                                                                     | 备注                                                |
| --------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------- |
| Intel DH67GD, DH67BL, <br />DH67CF, DH67CL 系列主板 | [链接](https://github.com/RehabMan/Intel-DH67XX-DSDT-Patch)                                                                        | [链接](https://www.tonymacx86.com/threads/guide-intel-dh67xx-with-hd3000-using-clover-uefi-hotpatch.233257/) | Intel DH67GD, DH67BL, <br />DH67CF, DH67CL 系列主板 |
| Surface Pro 3                                       |                                                                                                                                    |                                                                                                              |                                                     |
| Surface Pro 4                                       | [链接](https://github.com/Neil-Steven/SurfacePro4-Hackintosh) [链接](https://github.com/bigsadan/surface-pro-4-hackintosh-10.14.3) [链接](https://github.com/Afanyiyu/surface-pro-4-hackintosh-big-sur) | [链接](https://github.com/Neil-Steven/SurfacePro4-Hackintosh/blob/master/README.md) [链接](https://github.com/Afanyiyu/surface-pro-4-hackintosh-big-sur/blob/master/README.md)                         | surfacePro 4                                        |
| Surface Pro 6                                       | [链接](https://github.com/molie34/Surface-Pro-6-macOS)                                                                             | [教程](https://github.com/molie34/Surface-Pro-6-macOS)                                                       |                                                     |

### Other 其它

| 机型名称                     | 发布地址                                                                            | 教程地址                                                                     | 备注                                                                                                        |
| ---------------------------- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| avita liver v-14 |  |  |  |
| Clevo NH5x/NH70 | [链接](https://github.com/MichaelPan1026/Clevo-NH50-NH70-Hackintosh) | | |
| Clevo P950HR                 | [链接](https://github.com/MegaCookie/Clevo-P950HR-Hackintosh)                       |                                                                              | 蓝天 P950HR，猜的                                                                                           |
| 火影地狱火 X6                | [链接](https://github.com/gaofeicm/DiYuHuo-X6-MacOS-Mojave-10.14.3-Hackintosh)      |                                                                              |                                                                                                             |
| 火影金刚 GTX                 | [链接](https://github.com/Sherlockouo/Hackintosh)                                   |                                                                              |                                                                                                             |
| Thunderobot 911 Air          | [链接](https://github.com/athlonreg/Thunderobot-911-Air-i7-9750h)                   |                                                                              |                                                                                                             |
| Thunderobot 911 Air2         | [链接](https://github.com/athlonreg/Thunderobot-911-Air-i7-9750h)                   |                                                                              |                                                                                                             |
| 雷神笔记本黑苹果套件         | [链接](https://github.com/athlonreg/Thunderobot-Hackintosh)                         |                                                                              |                                                                                                             |
| Airbook 颜值版 i5 6200u  (Mojave) | [clover版链接](https://github.com/nabaonan/airbook-6200u-efi/tree/master)  [oc版链接](https://github.com/nabaonan/airbook-6200u-efi/tree/oc) | [教程](https://juejin.cn/post/6983945097658253320)  | 网卡推荐：[DW1820A](https://blog.daliansky.net/DW1820A_BCM94350ZAE-driver-inserts-the-correct-posture.html)  OC 0.7.2 系统：10.14.6 |
| Airbook 颜值版 i5 6200u  (Catalina) | [链接](https://github.com/nabaonan/airbook-6200u-efi/tree/catalina) |  | OC: 0.7.2 系统：Catalina 10.15.7 |
| Airbook 颜值版 i5 6200u（BigSur） | [链接](https://github.com/nabaonan/airbook-6200u-efi/tree/bigsur) |  | OC：0.7.2   系统：BigSur 11.5.1 |
| Airbook 颜值版 i5 6200u（Monterey） | [链接](https://github.com/nabaonan/airbook-6200u-efi/tree/monterey) | | OC: 0.7.5  系统:  Monterey12.0.1 及以上 |
| Airbook 颜值版 i5 6200u（Ventura） | [链接](https://github.com/nabaonan/airbook-6200u-efi/tree/ventura) | | OC: 0.8.3  系统: Ventura 13.0及以上 |
| 同方 GI5CN5E                 | [链接](https://github.com/rodgomesc/AVELL-G1513-FOX-7-TONG-FANG-GI5CN5E-HACKINTOSH) |                                                                              |                                                                                                             |
| GPD P2 MAX                   | [链接](https://github.com/Azkali/GPD-P2-MAX-Hackintosh)                             |                                                                              |                                                                                                             |
| 微星准系统 ProBox23          | [链接](https://github.com/Twilightlee/MSI_ProBox23_hackintosh)                      |                                                                              |                                                                                                             |
| MaiBenBen_Damai5             | [链接](https://github.com/jasminebd/MaiBenBen-Damai5)                               |                                                                              | 麦本本-大麦 5                                                                                               |
| Sony VAIO pro13              | [链接](https://github.com/raydoom/hackintosh-sony-vaio-pro13)                       |                                                                              |                                                                                                             |
| Sony VAIO SVS1512X9E/SVS1512X9EB | [链接](https://github.com/huhugh221/Efi-Hackintosh-SVS1512X9E-B-VAIO) | | |
| Terrans Force/Devil Rays DR7 | [链接](https://github.com/Jie2GG/Hackintosh-Devil-Rays-DR7)                         |                                                                              | 未来人类                                                                                                    |
| MONSTER Tulpar T7 V20.1      | [链接](https://github.com/sutsurup/MONSTER-Hackintosh)                              | [链接](https://github.com/sutsurup/MONSTER-Hackintosh/blob/master/README.md) |                                                                                                             |
| 壹号本 OneMix3 Pro           | [链接](https://github.com/lulujyc/OneMix3Pro-OpenCore)                              |                                                                              |                                                                                                             |
| 松下 Let's Note CF-SZ5       | [链接](https://github.com/waldoxhm/Panasonic_CF-SZ5_SZ5PDYVS_hackintosh_EFI)        |                                                                              |                                                                                                             |
| 机械师 F117B1                | [链接](https://github.com/Lusior/F117B-Hackintosh)                                  |                                                                              |                                                                                                             |
| 未来人类 T5                  | [链接](https://github.com/jojo176/TerransForce-T5SKYLAKE-67SH1-Hackintosh-OpenCore) |                                                                              |                                                                                                             |
| 未来人类 X599 初款           | [链接](https://github.com/WarsFeng/P750ZM-Hackintosh)                               |                                                                              | 关联蓝天 P750ZM                                                                                             |
| FUJITSU 富士通 S762          | [链接](https://github.com/hongweizhu163/Hackintosh-EFI-for-FUJITSU-S762)            |                                                                              |                                                                                                             |
| 51nb X210 ThinkPad 副厂主板  | [链接](https://github.com/lulujyc/51nb-X210-Hackintosh)                             |                                                                              |                                                                                                             |
| CHUWI Minibook               | [链接](https://github.com/THEDEVIOUS1/CHUWI-MINIBOOK-HACKINTOSH)                    |                                                                              |                                                                                                             |
| Chuwi CoreBookX 14 | [链接](https://github.com/weachy/CoreBookX-14-Hackintosh) | | |
| 海尔 Haier Y11C              | [链接](https://github.com/HussainTaj-W/haier-y11c-efi-oc-hackintosh-big-sur)        |                                                                              |                                                                                                             |
| 51nb T70 ThinkPad 副厂主板  | [链接](https://github.com/51nbT70CLOVER/51nb-T70-Hackintosh)                         |                                                                              |                                                                                                             |
| Medion Erazer P7647 | [链接](https://github.com/axemre/OpenCore-Medion-Erazer-P7647) | | |
| Infinix INBook X1 | [链接](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore_INBook_X1_XL11_i3-) | | |
| Mechrevo Jiaolon-76Q | [链接](https://github.com/top1Ashier/Mechrevo-Jiaolong-76Q-Hackintosh) | | AMD Ryzen 7 5800h |


### 笔记本更多的机型

| 机型名称     | 发布地址                                 | 教程地址 | 备注                                                                  |
| ------------ | ---------------------------------------- | -------- | --------------------------------------------------------------------- |
| **更多机型** | [链接](https://github.com/sqlsec/clover) |          | 引用自：国光之前维护的仓库                                            |
|              | [链接](https://zhih.me/hackintosh/#/)    |          | 底噪出品：**[one-key-hidpi](https://github.com/xzhih/one-key-hidpi)** |

### 笔记本相关资源

| **笔记本相关资源**   |                                                |                                                              |                                                              |
| -------------------- | ---------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                      | **hotpatch**                                   |                                                              |                                                              |
| P-little             | [链接](https://github.com/daliansky/P-little)  | `Clover` 部件热修复(hotpatch)                                | 宪武做的一套 ThinkPad 补丁，刚开始上传，请期待               |
| OC-little            | [链接](https://github.com/daliansky/OC-little) | `OpenCore` 部件热修复(hotpatch)                              | 感谢：@宪武                                                  |
|                      | **触摸板**                                     |                                                              |                                                              |
| VoodooI2C-PreRelease |                                                | 触摸设备 DSDT 修补补充                                       | [Bat.bat](https://github.com/williambj1)搞的                 |
| GenI2C               | [链接](https://github.com/williambj1/GenI2C)   | 生成 SSDT 触摸板的热修复补丁(hotpatch)，以便支持`VoodooI2C`  |                                                              |
|                      | **无线网卡**                                   |                                                              |                                                              |
| 推荐无线网卡         | **MiniPCIe** 接口(推荐 BCM4352HMB、DW1510)     | **博通**：BCM94322HM8L、Asus BCM94352、AzureWave AW-CE123H、AzureWave AW-NB290H、DW1510、DW1520、DW1550、 | **高通**：DW1515、DW1705、AR5BHB92、AR5BHB112 AR9285 芯片在 10.14 将不再被支持 |
|                      | **PCIe** 接口                                  | **博通**：BCM94331CD、BCM94322MC、[BCM94360CD](https://hackintosher.taobao.com) | **高通**：AR5BXB72、AR5BXB92、AR5BXB112                      |
|                      | **M.2** 接口                                   | **博通**：BCM94352Z(AE)、DW1560，DW1830<br />BCM94350Z(AE)/[DW1820A](https://hackintosher.taobao.com)<br />BCM94360Z3 / [BCM94360Z4](https://hackintosher.taobao.com) |                                                              |
|                      | **USB** 无线网卡                               | RealTek 系列                                                 | [链接](https://github.com/chris1111/Wireless-USB-Adapter-Clover) |

## 台式机

## AMD Ryzen

| **台式**                           | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| AMD Vanilla OpenCore               | [链接](https://github.com/AMD-OSX/AMD_Vanilla)               | [链接](https://blog.csdn.net/qq_43547885/article/details/105687341) | AMD 通用安装补丁                                             |
| AMD Ryzen 安装教程                 | [链接](https://github.com/MrNegativeTW/Ryzen-Hackintosh-Tutorial) [链接](https://github.com/doesprintfwork/Intel-AMD-Hackintosh-Guide) | [链接](https://mtwstudio.gitbook.io/ryzentosh/)              | 适用于`10.12` `10.13` `10.14`                                |
| ASRock B450 Gaming-ITX/ac          | [链接](https://github.com/LemoFire/OpenCore-ASRock-B450-Gaming-ITX-ac) |                                                              |                                                              |
| ASRock B450M Pro4                  | [链接](https://github.com/dr03m/ASRock-B450M-Pro4-USB-Patch) |                                                              |                                                              |
| ASRock B450M Steel Legend          | [链接](https://github.com/marcustut/Hackintosh)              |                                                              |                                                              |
| ASRock Fatal1ty B450 Gaming K4     | [链接](https://github.com/X-c0d3/EFI_Opencore_Catalina)      |                                                              |                                                              |
| ASRock H470M ITX                   | [链接](https://github.com/FTWH/asrock-h470m-itx-opencore-i5-10500-RX5700-EFI) |                                                              |                                                              |
| ASRock B550M Steel Legend          |                                                              |                                                              |                                                              |
| Asrock X399m Taichi                | [链接](https://github.com/cmd2001/X399m-Taichi-Ryzen-Threadripper-2970wx-RX550-Monterey-Opencore) |                                                              | AMD Ryzen Threadripper 2970wx                                |
| ASRock x570M Pro4                  | [链接](https://github.com/kriskbx/ryzentosh)                 |                                                              | RX 5700XT<br />                                              |
| ASRock X570 taichi                 | [链接](https://github.com/yhl452493373/ryzen-hackintosh-efi) |                                                              |                                                              |
| ASRock X570 Phantom Gaming ITX/TB3 | [链接](https://github.com/aluveitie/RyzenMacPro) [链接](https://github.com/radianttap/EFI-ASRock-X570-ITX-iMacPro1-1)<br />[链接](https://github.com/bassrock/opencore-efis) |                                                              | AMD Ryzen 9 3900X<br />Sapphire Radeon RX 5500<br />支持`Big Sur` |
| Asus M5A97                         | [链接](https://github.com/andrerds/efi-big-sur-mb-asus-M5A97) |                                                              | AMD FX6300                                                   |
| Asus Prime A320M-K                 | [链接](https://github.com/ZaRdEc22/Hackintosh-Ryzen-7-EFI)   |                                                              |                                                              |
| Asus ROG STRIX B350-I GAMING       | [链接](https://github.com/vsnotme/B350I-EFI-opencore)        |                                                              |                                                              |
| Asus B350 Plus                     | [链接](https://github.com/mikigal/ryzen-hackintosh) [链接](https://github.com/Salcedoandrew/RYZEN-OPENCORE-0.5.9) |                                                              | AMD Ryzen 7 1700/MSI RX Vega 64                              |
| Asus ROG B450-E                    | [链接](https://github.com/rice512/ROG-STRIX-B450-E-GAMING-OpenCore) |                                                              |                                                              |
| Asus ROG STRIX B450-F              | [链接](https://github.com/nqcshady/rog-strix-b450f-opencore) |                                                              |                                                              |
| Asus ROG Strix B450-F Gaming       | [链接](https://github.com/Mattis-Schulte/hackintosh-catalina) |                                                              |                                                              |
| Asus Prime B450M-A                 | [链接](https://github.com/hwangmin88/macOS-Asus-Prime-B450M-A) |                                                              |                                                              |
| Asus Rog Strix B450-I              | [链接](https://github.com/fuermosi777/hackintosh-asus-b450i-oc) [链接](https://github.com/willza3/macOS-strix-B450i) |                                                              |                                                              |
| Asus ROG Strix B450-I GAMING       | [链接](https://github.com/solosoyfranco/macOS-nVidia-strix-B450i) |                                                              |                                                              |
| Asus TUF B450M                     | [链接](https://github.com/Pai2Chen/OpenCore-Asus-TUF-B450M-Plus-Gaming) [链接](https://github.com/maomingyang1314/MACOS--AMD-3700X-TUFB450-ROG5700XT-) |                                                              |                                                              |
| Asus TUF B450 TUF PRO Gaming       | [链接](https://github.com/maomingyang1314/MACOS--AMD-3700X-TUFB450-ROG5700XT-) |                                                              |                                                              |
| Asus TUF B450-Plus Gaming          | [链接](https://github.com/arg0dev/Ryzen-R7-2700-3800x-macOS-Stable-EFI-Repository) |                                                              |                                                              |
| Asus ROG STRIX B550-A GAMING       | [链接](https://github.com/jerryhan77/asus-strix-b550-a-opencore) |                                                              |                                                              |
| Asus ROG Strix B550-F Gaming       | [链接](https://github.com/FloridaMan7588/MacOS-efi)          |                                                              |                                                              |
| Asus Rog Strix B550i               | [链接](https://github.com/huukhai/hackintosh-rog-b550i) [链接](https://github.com/tahmid-H/Asus-ROG-B550I-EFI) |                                                              |                                                              |
| Asus TUF Gaming B550M-Plus         | [链接](https://github.com/ahmetdereli/Hackintosh-Opencore-Asus-TUF-Gaming-B550M-Plus-WI-FI-RX570) [链接](https://github.com/Purple-CSGO/Hackintosh-OpenCore-B550M-TUF-PLUS-WIFI-MacOS-EFI) 或 [R5-5600-550M-RX6600-6750GRE](https://github.com/goozyshi/RYZENTOSH-5600-550M-RX6600-6750GRE)|                                                              |                                                              |
| Asus ROG CROSSHAIR VI HERO         | [链接](https://github.com/YWQBX/RyzenProEFI)                 |                                                              |                                                              |
| Asus Crosshair VIII Hero           | [链接](https://github.com/steeve/ryzentosh)                  |                                                              |                                                              |
| Asus X470 Pro                      | [链接](https://github.com/danielskowronski/BigSur_Hackintosh_on_ASUS_X470-PRO) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Asus ROG Strix X570-E Gaming       | [链接](https://github.com/ezaul/EFI-Asus-ROG-X570-E)         |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Asus ROG Strix X570-F Gaming       | [链接](https://github.com/JoHoop/ryzentosh-efi-big-sur)      |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Asus ROG Strix X570-I              | [链接](https://github.com/ChanceArthur/macOS-EFI-Asus-X570I) |                                                              |                                                              |
| Asus Strix GAMING X570-I           | [链接](https://github.com/reimertz/hackintosh-x570i-3950x) [链接](https://github.com/ChanceArthur/macOS-EFI-Asus-X570I) |                                                              | Ryzen 9 3950x/Reden Vega 64<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| Asus TUF Gaming X570               | [链接](https://github.com/hermanzhaozzzz/My-Opencore-EFI-for-AMD3900X-5700XT-TUF-x570-Hackintosh) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Asus TUF X570 Gaming Plus          | [链接](https://github.com/MenschLennart/AsusTUFX570GamingPlusWIFI) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Asus PRIME X570-P                  | [链接](https://github.com/buzuddha/ASUS-X570-P-OpenCore-EFI) |                                                              |                                                              |
| Asus B350 Plus                     | [链接](https://github.com/mikigal/ryzen-hackintosh)          |                                                              | MSI GTX 1080 Gaming X                                        |
| Asus M5A97 LE R2.0                 | [链接](https://github.com/pexcn/hackintosh-amd)              |                                                              | AMD FX 6300/NVIDIA GTX 650                                   |
| Biostar Racing x370 gun            | [链接](https://github.com/evertonresende/EFI-BIOSTAR-RACING-X370-GTN-RYZEN5-2600-RX590) |                                                              |                                                              |
| Colorful CVN X570M GAMING PRO V14  | [链接](https://github.com/TroyJim/ryzen-x570-hackintosh)     |                                                              |                                                              |
| Gigabyte AB350 Gaming 1            | [链接](https://github.com/ThatsNiceGuy/ab350-gaming-hack)    |                                                              | AMD Ryzen 5 1600                                             |
| Gigabyte Aorus Pro wifi B450 MITX  | [链接](https://github.com/zarboz/Open-Core-GB-b450)          |                                                              |                                                              |
| Gigabyte B450M DS3H                | [链接](https://github.com/AbhijithGo/Hackintosh-BigSur-11.0.1-EFI) [链接](https://github.com/shivankpal/CatalinaEFI)<br />[链接](https://github.com/ctaetcsh/hackintosh/tree/master/Current-Hackintosh-Desktop) |                                                              |                                                              |
| Gigabyte B450M-S2H                 | [链接](https://github.com/fishaffair/b450m-s2h-catalina)     |                                                              |                                                              |
| Gigabyte B450M Aorus Elite         | [链接](https://github.com/ExodazTH/RyzenHackintosh) [链接](https://github.com/awesometic/hackintosh-gigabyte-x570-aorus-elite) |                                                              |                                                              |
| Gigabyte X399 Aorus Extreme        | [链接](https://github.com/SchmockLord/Hackintosh-Threadripper-1950x-Gigabyte-X399-Aorus-Extreme) |                                                              | Threadripper 1950x@4.0Ghz                                    |
| Gigabyte X399 Aorus Xtreme         | [链接](https://github.com/shahyar/opencore-x399-aorus-xtreme-threadripper) |                                                              |                                                              |
| Gygabyte B550i Aorus Pro AX        | [链接](https://github.com/aleixsr/Ryzentosh) [链接](https://github.com/masbroo69/OpenCore-EFI-for-Gigabyte-B550I-Aorus-Pro-AX)<br />[链接](https://github.com/radianttap/EFI-B550I-Aorus) |                                                              |                                                              |
| Gigabyte X570 I Arous Pro Wifi     | [链接](https://github.com/rexding97/AMD-Hackintosh-OpenCore6.1-EFI) |                                                              |                                                              |
| Gigabyte X570 AORUS PRO            | [链接](https://github.com/simon-fauconnier/ryzen-hackintosh) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Gigabyte X570 UD                   | [链接](https://github.com/MrInternauta/EFI_Ryzentosh)        |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Gigabyte B660M Aorus Pro       | [链接](https://github.com/taruyato/b660m-aorus-pro-ddr4-hackintosh)        |                                                              | 网卡推荐：BCM94360CD |  
| MSI B450 GAMING PRO CARBON AC      | [链接](https://github.com/jinhaozcp/Hackintosh-Ryzen-MSI-B450-Gaming-Pro-carbon-ac) |                                                              | Ryzen 7 3700X / RX5700                                       |
| MSI B450M MORTAR                   | [链接](https://github.com/harpsword/hackintosh-ryzen)        |                                                              |                                                              |
| MSI B450M-A PRO MAX                | [链接](https://github.com/EraserCN/B450M-Hackintosh)       |                                                              |                                                              |
| MSI B450 TOMAHAWK MAX              | [链接](https://github.com/kasik96/B450-TOMAHAWK-MAX-RYZEN-5-3600-RX-570) [链接](https://github.com/bakedpotato191/ryzentosh)<br />[链接](https://github.com/bilal78619/Ryzen-7-3700x-Opencore-EFI) [链接](https://github.com/bakedpotato191/ryzentosh) |                                                              | Ryzen 5 3600 / RX570<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI B450 Tomahawk Max ATX AM4      | [链接](https://github.com/osx86-ijb/MSI-B450-Tomahawk-Max-Ryzen5-3600-macOS-BigSur) |                                                              |                                                              |
| MSI B350M Gaming Pro               | [链接](https://github.com/nghuunghiaa111/Hackintosh-IMac)    |                                                              | AMD Ryzen 5 1400<br />MSI RX580 8GB Armor                    |
| MSI B450I Gaming Plus AC           | [链接](https://github.com/portrayer/Hackintosh-Ryzen-MSI-B450I) [链接](https://github.com/delbertbeta/macOS-msi-b450i-OC)<br />[链接](https://github.com/Jasonzj/Hackintosh-EFI-Ryzen-MSI-B450I) |                                                              |                                                              |
| MSI B450M Gaming Plus Max          | [链接](https://github.com/lay870/EFI-Big-Sur)                |                                                              |                                                              |
| MSI B450m 迫击炮                   | [链接](https://github.com/heyxiaobai/MSI-B450m-MORTAR-Hackintosh) [链接](https://github.com/Cluas/MSI-b450m-OC) |                                                              | AMD R5 3600x/蓝宝石 RX 570<br />开发分支支持`Big Sur`        |
| MSI B450M Mortar Max               | [链接](https://github.com/VanXNF/Hackintosh-Ryzen-3500X-MSI-B450M-Mortar-MAX) [链接](https://github.com/erhuoL/hackintosh-B450m-mortar-max)<br />[链接](https://github.com/mckarsi/opencore-efi) [链接](https://github.com/vince523/AMD_3A_Hackintosh_EFI)<br />[链接](https://github.com/Whosydd/MSI-B450m-Hackintosh-BigSur) [链接](https://github.com/dhruvanbhalara/b450-msi-mortar-max-hackintosh)<br />[链接](https://github.com/anokic/ryzen-hackintosh) [链接](https://github.com/tomseanmy/BigSur-2600xEFI) |                                                              |                                                              |
| MSI B450M PRO-VDH MAX              |                                                              |                                                              |                                                              |
| MSI B550 A-Pro                     | [链接](https://github.com/Shidil/opencore-5600x-B550)        |                                                              |                                                              |
| MSI MAG B550M MORTAR WIFI          | [链接](https://github.com/ybakime/Hackintosh-Opencore-MAG-MSI--B550M-MORTAR-WIFI-EFI) |                                                              |                                                              |
| MSI X370 Krait Gaming              | [链接](https://github.com/yhl452493373/ryzen-hackintosh-efi) |                                                              | 10.14.6                                                      |
| MSI X370 KRAIT GAMING              | [链接](https://github.com/yhl452493373/ryzen-hackintosh-efi) |                                                              |                                                              |
| MSI X399                           | [链接](https://github.com/lulujyc/MSI-X399-Gaming-Pro-Carbon-AC-1950X-Hackintosh-OpenCore-EFI) |                                                              |                                                              |
| MSI X470 Gaming Pro                | [链接](https://github.com/Przeblysk/MSI_X470_GAMING_PRO_AMD_2700X_NVIDIA_1070Ti_MacOS-High-Sierra) |                                                              | Nvidia 1070Ti 显卡原因安装的是 High-Sierra 10.13.6           |
| MSI X470 Gaming Pro Carbon         | [链接](https://github.com/MaximumQuiet/ryzentosh)            |                                                              |                                                              |
| MSI X470 gaming PRO MAX            | [链接](https://github.com/wokilp/MSI_X470_GAMING_PRO_MAX-AMD-R5-2600-EFI) [链接](https://github.com/Cole987/EFI-MSI-X470-Monterey) |                                                              |                                                              |
| MSI MEG X570 ACE                   |                                                              |                                                              |                                                              |
| MSI MAG X570 TOMAHAWK WIFI         | [链接](https://github.com/theHari08/MSI-MAG-X570-TOMAHAWK-WIFI-Hackintosh) |                                                              |                                                              |
| MSI MPG X570 GAMING PLUS           | [链接](https://github.com/SuperY/OpenCore-EFI-for-MSI-MPG-X570-Gaming-Plus) |                                                              |                                                              |
| Asus ROG Strix B450-F Gaming       | [链接](https://github.com/Desousak/macOS-strix-b450F)        |                                                              |                                                              |
| MS-iCraft B550M WIFI               | [链接](https://github.com/wuwuwu223/Hackintosh-Opencore-MS-iCraft-B550M-WIFI-EFI) |                                                              |                                                              |


## INTEL CPU 系列

### ASRock 华擎

| **台式（部分）**                   | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| ASRock B150M-HDV                   | [链接](https://github.com/Z-fly/ASRock-B150M-HDV-OpenCore-Hackintosh) |                                                              | 原则上支持 6~9 代 Intel 所有 CPU，核显请自行修改。持续更新，类似配置可参考 |
| ASRock deskmini 110                | [链接](https://github.com/suxiaogang/asrock-deskmini-110-hackintosh) |                                                              |                                                              |
| ASRock deskmini 310                | [链接](https://github.com/liminghuang/asrock_deskmini310_hackintosh) [链接](https://github.com/huangyanan/Hackintosh-EFI-for-deskmini-310-dw1820)<br />[链接](https://github.com/vainhope/Hackintosh-Deskmini310-EFI) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| ASRock deskmini H470               | [链接](https://github.com/lugeek/Asrock-Deskmini-H470-Opencore) [链接](https://github.com/SamCsquared/Deskmini-H470-Opencore-EFI) |                                                              |                                                              |
| Asrock deskmini H470m              | [链接](https://github.com/mirkcale/hackintosh_asrock_deskmini_h470) |                                                              |                                                              |
| ASRock B85 Pro4                    | [链接](https://github.com/VidocqH/Hackintosh-EFI-E3-1230v3-RX580) |                                                              | Intel Xeon E3-1230 v3                                        |
| ASRock B360-ITX/ac                 | [链接](https://github.com/jhelgert/hackintosh)               |                                                              |                                                              |
| ASRock B360M-HDV                   | [链接](https://github.com/RealKiro/Hackintosh)               |                                                              |                                                              |
| ASRock B360M Pro4                  | [链接](https://github.com/Joehaivo/hackintosh)               |                                                              |                                                              |
| ASRock Fatal1ty B360M              | [链接](https://github.com/osx86-ijb/ASRock-Fatal1ty-B360M-Performance-macOS-Catalina) |                                                              |                                                              |
| ASRock B365M                       | [链接](https://github.com/punjasin/Opencore-EFI-AsrockB365M) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock B365M-ITX                   | [链接](https://github.com/imzhengziyi/ASRock-B365M-ITX-AC-opencore/releases) |                                                              |                                                              |
| ASRock B365M Pro4                  | [链接](https://github.com/andynvt/hackintosh-asrock-b365m-pro4-i7-8700-rx-580) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock B460m HDV                   | [链接](https://github.com/aditnanda/EFI-Asrock-B460m-HDV-Core-i5-10400F) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock B460M-ITX/AC                | [链接](https://github.com/ansonliao/Asrock-B460m-ITX-AC-OC-EFI) |                                                              |                                                              |
| ASRock B460M Pro4                  | [链接](https://github.com/yrambler2001/Hackintosh-Intel-i5-10600-iGPU-AsRock-B460M-Pro4) |                                                              | i5-10600 / 核显<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASRock B460M Steel Legend          | [链接](https://github.com/ducnm9/Hackintosh-Intel-i5-10400-Asrock-B460M-Steel-Legend) [链接](https://github.com/VictorZheng1010/Hackintosh_EFI) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock B560M-HDV                   | [链接](https://github.com/kreactnative/asrock-b560-hdv-11400-rx-560-big-sur) |                                                              |                                                              |
| ASRock B560M-ITX                   | [链接](https://github.com/yohan8901/ASRock-B560M-ITX-Hackintosh) [链接](https://github.com/jalalabdulaziz/Asrock-B560M-ITX-ac) |                                                              |                                                              |
| ASRock B560 Steel Legend           | [链接](https://github.com/ExodazTH/ASROCK-B560-STEEL-LEGEND-INTEL-CORE-I5-11400-BIG-SUR) [链接](https://github.com/asumi233/Asrock-b560m-steel-6800xt-OC)<br />[链接](https://github.com/uranium81/hackintosh-intel-11th-gen) | [链接](https://github.com/uranium81/hackintosh-intel-11th-gen) | 链接3：i5-11600K+Nvidia Quadro K420                          |
| ASRock H410M-ITX/AC                | [链接](https://github.com/lishican/OpenCore6.4-EFI-AsRock-H410M-ITX-AC-i3-10100-igpu) [链接](https://github.com/vlazhuv/OpenCore-0.6.8-EFI-AsRock-H410M-ITX-AC-10500ES-iGPU) |                                                              |                                                              |
| ASRock H510M-HDV                   | [链接](https://github.com/Vincent3Hsia/ASRock-H510M-HDV-M.2-i5-10400-Hackintosh) |                                                              |                                                              |
| ASRock H61M-S1 Plus                | [链接](https://github.com/SanjayRavindran/HackintoshCatalina-Aug2020) |                                                              |                                                              |
| ASRock X99 Extreme3                | [链接](https://github.com/stefan2225/Asrock-X99-Extreme3-Opencore-Hackintosh) |                                                              |                                                              |
| ASRock X299                        | [链接](https://github.com/mohdropi/EFI-Catalina) [链接](https://github.com/mohdropi/EFI-BigSur) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock X299E-ITX/ac                | [链接](https://github.com/cmd2001/X299e-itx-ac-i9-7960x-RX5500-Monterey-Opencore/tree/master/EFI) |                                                              |                                                              |
| ASRock Z170 Gaming K4              | [链接](https://github.com/olwimo/EFI)                        |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock Z370M-ITX/ac                | [链接](https://github.com/Yellowpal/ASRock-Z370M-ITX-AC-OpenCore) |                                                              | OpenCore                                                     |
| ASRock Z370 Pro4                   | [链接](https://github.com/athlonreg/ASRock-Z370-Pro4-Hackintosh) [链接](https://github.com/apure123/asrock-z370pro4-hackintosh) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock Z390M-ITX/ac                | [链接](https://github.com/chinalichen/ASRock_Z390M_ITX_Clover_EFI) [链接](https://github.com/jjrccop/ASRockZ390M-ITX-acHackintosh) |                                                              |                                                              |
| ASRock Z390M Pro4                  | [链接](https://github.com/XiongMing/ASRock-Z390M-Pro4-EFI)   |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock Z390 Phantom Gaming itx     | [链接](https://github.com/haiyang1992/Hackintosh-Opencore-Asrock_Z390_Phantom_Gaming_ITX) [链接](https://github.com/icyleaf/EFI-ASRock-Z390-Phantom-Gaming-ITX) [链接](https://github.com/bydavy/EFI-ASRock-Z390-Phantom-Gaming) <br />[链接](https://github.com/kcunanan/Jared-PC/) [链接](https://github.com/befuture/EFI-ASRock-Z390-Phantom-Gaming) [链接](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX) |                                                              | 华擎 Z390 Phantom Gaming itx/ac                              |
| ASRock Z390 Phantom ITX            | [链接](https://github.com/zanderzhng/EFI_Asrock_Z390_Phantom_ITX) [链接](https://github.com/seanzhang98/ASRock-Z390-Phantom-ITX-OpenCore-Hackintosh-2020) |                                                              |                                                              |
| ASRock Z490M ITX/ac                | [链接](https://github.com/Lorys89/ASROCK_Z490M-ITX-AC) [链接](https://github.com/Old-Black-Dog/Hackintosh-ASRock-Z490M-ITX-ac) [链接](https://github.com/huijiewei/ASRock-Z390m-ITX-ac-Opencore)<br />[链接](https://github.com/ruibeard/OpenCore-ASRock-Z490M-ITX-ac) |                                                              |                                                              |
| Asrock Z490M Pro4m                 | [链接](https://github.com/xuanquydsr/z490m-pro4-10700k-hackintosh) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| ASRock Z490 ITX/TB3                | [链接](https://github.com/kreactnative/EFI-ASRock-Z490-ITX-TB3-RX580) |                                                              |                                                              |
| ASRock Z490 Phantom Gaming ITX/TB3 | [链接](https://github.com/papadiche/10900K-ASRock-Z490-Phantom-Gaming-ITX-TB3-RX-5600-XT) |                                                              |                                                              |
| ASRock Z490 Steel Legend           | [链接](https://github.com/sqlsec/AsRock-Z490-Steel-Legend-i7-10700)[链接](https://github.com/xiaoyaowx/Hackintosh-Z490-ASRock-Steel-Legend-Intel-10700) |                                                              | I7-10700 / 蓝宝石 RX 5600XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |

### ASUS 华硕

| **台式（部分）**               | 发布地址                                                     | 教程地址 | 备注                                                         |
| ------------------------------ | ------------------------------------------------------------ | -------- | ------------------------------------------------------------ |
| Asus B85 Pro Gamer             | [链接](https://github.com/xl120022/ASUS-B85PG-E3-RX570-MAC10.15) |          | e3-1231v3 / rx570                                            |
| Asus B85MG | [链接](https://github.com/samleong123/i5-4570-B85MG-HD4600-BigSur-Opencore-EFI) | | i5-4570 |
| Asus P8H61-M LX3 | [链接](https://github.com/thincen/H61-i3-3220-GTX650-EFI) | |  |
| Asus P8P67 EVO | [链接](https://github.com/Qraxin/Asus-P8P67-OpenCore-EFI) | | i7-2600k |
| ASUS Chromebox CN62            | [链接](https://github.com/waldoxhm/asus-chromebox-cn62-guado-hackintosh) |          |                                                              |
| ASUS B250M                     | [链接](https://github.com/zsyshuyang/Hackintosh-EFI-For-ASUS-B250M-PLUS-i5-7500-RX580) [链接](https://github.com/laijingwei/CLOVER-EFI) |          |                                                              |
| ASUS PRIME B250M-K | [链接](https://github.com/amervelic/efi-b250m-k) | | |
| Asus EX-B460M-V5 | [链接](https://github.com/anhduong28/ex-b460m-v5-i5-10400-hackintosh) | | |
| Asus Prime H310I-M             | [链接](https://github.com/xLidoni/i3-8100-H310I-Hackintosh_OC) |          |                                                              |
| Asus Prime H310M-F R2.0 | [链接](https://github.com/hanandjun/Hackintosh-Pentium-G5420) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG Strix B360-i          | [链接](https://github.com/jiangwweie/ROG-B360I-EFI) [链接](https://github.com/NEEPUCS/Ausu-ROG-Strix-B360i-HACKINTOSH-OPENCORE-EFI) |          |                                                              |
| Asus TUF B360M-PLUS-S          | [链接](https://github.com/Zerah64/hackintosh_9400f_b360_vega56) [链接](https://github.com/swlfigo/HackintoshEFI) |          ||
| Asus TUF B360M-GAMING-PLUS          | [链接](https://github.com/secretandanon/hackintosh-asus-tuf-B360m-gaming-efi)  |          ||
| ASUS TUF B460M                 | [链接](https://github.com/SmallKi-d/ASUS-B460M-TUF-I5-10500ES-RX5700) [链接](https://github.com/SeanChan0901/ASUS-B460M-TUF-HACKINTOSH-OPENCORE-EFI) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Rog Strix B460-G Gaming   | [链接](https://github.com/huytbt/Hackintosh-Desktop-CometLake-B460G-Board-OpenCore) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus B460m Plus                | [链接](https://github.com/CasperNan/opencore-ASUS-B460m-plus-10400) |          | Intel 10400 / AMD 5500XT<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Asus ROG Strix B460-I          | [链接](https://github.com/jalalabdulaziz/ROG-Strix-B460-I) [链接](https://github.com/intihyan/OC-b460i-strix-i7-10700)<br />[链接](https://github.com/lqsahut/ROG_B460i_Hackintosh) |          | I7-10700 / RX570<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Asus TUF Gaming B460M PLUS        | [链接](https://github.com/Swayyyyy/ASUS-TUF-GAMING-B460M-PLUS-RX570-Hackintosh-Opencore) [链接](https://github.com/lukeckt2/EFI-10400-B560m-TUF-WIFI) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Asus TUF GAMING B460M-PRO | [链接](https://github.com/SourceLink/ASUS-TUF-GAMING-B460M-PRO-RX570-Hackintosh-Opencore) | |  |
| Asus ROG STRIX B560-I GAMING WIFI | [链接](https://github.com/NOXCIS/OpenCore-ROG-B560I) | | |
| Asus TUF Gaming B560M PLUS | [链接](https://github.com/JoveYu/ASUS-TUF-GAMING-B560M-PLUS-WIFI-EFI) | |  |
| Asus TUF Gaming B660M PLUS | [链接](https://github.com/Xmingbai/ASUS-TUF-GAMING-B660M-PLUS-Wi-Fi-D4-Hackintosh) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus H110M-C2 MoBo | [链接](https://github.com/mrmac189/OpenCore-H110M-HD530) | |  |
| Asus H170M-PLUS | [链接](https://github.com/riccardo4zan/Opencore-EFI) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus H370i                     | [链接](https://github.com/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI) |          |                                                              |
| Asus ROG STRIX H370-I GAMING | [链接](https://github.com/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI) | | |
| Asus ROG STRIX H370-F GAMING | [链接](https://github.com/ChengYen-Tang/ROG-STRIX-H370-F-GAMING-Hackintosh) | | |
| Asus Sabertooth z87            |             |          |                                                              |
| Asus Z97K 4980HQ               | [链接](https://github.com/efsg/ASUS-Z97K-4980HQ-Hackintosh)  |          | I7-4980HQ                                                    |
| Asus Z170 Deluxe | [链接](https://github.com/kushwavez/asus-z170-deluxe-clover-efi) | |  |
| Asus Z170-P                    | [链接](https://github.com/Sharlion/z170_6700k_hackintosh)    |          | 华硕Z170-P+6700K+RX470                                       |
| Asus Z170-Pro | [链接](https://github.com/DaveC96/HackintoshEFI) | |  |
| Asus ROG Maximus X Hero Z370   | [链接](https://github.com/RainshawGao/Hackintosh) [链接](https://github.com/Urufu19/EFI-OPENCORE-BIG-SUR-ASUS-z370) |          | Vega 56 <br />网卡推荐：[DW1820A](https://hackintosher.taobao.com) / [BCM94360CD](https://hackintosher.taobao.com) |
| ROG Maximus XI Hero Wi-Fi M11H | [链接](https://github.com/ttdevs/EFI-Z390-ROG-MAXIMUS-XI-HERO-WIFI-i7-8700K) |          |                                                              |
| Asus ROG STRIX H370-I GAMING   | [链接](https://github.com/Autocrit/Asus-ROG-STRIX-H370-I-GAMING-Hackintosh-Guide) [链接](https://github.com/sheva007/H370i_RX580_OC0.6.1) |          | mini-ITX H370 motherboard                                    |
| Asus STRIX Z270-E              | [链接](https://github.com/BradenM/Hackintosh-7700k-R9_390-iGPU) |          | Asus STRIX Z270-E                                            |
| Asus ROG Strix Z270G Gaming    | [链接](https://github.com/marknotton/OpenCore-EFI)           |          |                                                              |
| Asus ROG Strix Z390-E          | [链接](https://github.com/xiedonghang/hackintosh) [链接](https://github.com/lbrdev/asus_z390e_opencore_hackintosh) |          | Intel i9-9900k+UHD630核显                                    |
| ASUS ROG STRIX Z390-E GAMING   | [链接](https://github.com/xinsui01/hackintosh_ASUS_ROG_Z390) [链接](https://github.com/xiedonghang/hackintosh) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASUS ROG Z390-F Gaming | [链接](https://gitee.com/GMYmengyuan/Asus-ROG-STRIX-Z390-F-Gaming-EFI) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG STRIX Z390-I GAMING | [链接](https://github.com/imotoboy/EFI) [链接](https://github.com/iscaswcm/z390i-radeonvii-efi) | | |
| Asus Prime H410M | [链接](https://github.com/laijingwei/OpenCore-EFI) | |  |
| Asus Prime H410M-E | [链接](https://github.com/Erics-Lab/H410M-E-Opencore-0.6.5-EFI) | | |
| Asus Prime Z370-P              |  |          | `强制RGB模式（EDID覆盖）`                                    |
| Asus PRIME Z390                | [链接](https://github.com/dhckdgjs/ASUS-PRIME-Z390-A-HACKINTOSH-Clover-iGPU-with-dGPU-UHD630-RX580) |          | ASUS-PRIME-Z390<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Prime Z390-A              | [链接](https://github.com/ErickAgrazal/hackinstosh-efi) [链接](https://github.com/DiZhou92/ROG-STRIX-Z490-G-WIFI-ASUS) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Prime Z390-P              | [链接](https://github.com/vastxie/ASUS-PRIME-Z390-P_i5-9600K_RX5500XT) [链接](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens) <br />[链接](https://github.com/jhihhe/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_OpenCore-0.7.0) |          | i5-9600K + RX5500XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASUS Prime Z390M PLUS          | [链接](https://github.com/Lyrance/ASUS-Prime-Z390M-PLUS-EFI) [链接](https://github.com/LHB6540/Asus-R414-Hackintosh-10.15.7)<br />  |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus TUF Z390-PLUS GAMING (WI-FI) | [链接](https://github.com/zpengcom/opencore-efi) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Z490 AORUS PRO AX | [链接](https://github.com/zxyboy/i9-10850K-Z490-AORUS-PRO-AX) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Prime Z490-A              | [链接](https://github.com/yilmazca/intel-i9-10900K-Asus-prime-Z490A-hackintosh) [链接](https://github.com/evenlinyf/hackintosh-EFI-Z490A-i710700k-5700xt) |          | OC: Intel i9-10900K 核显DP<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Z490 A GAMING             | [链接](https://github.com/ngocdoan/hackintosh-z490-A-Gaming-10900k-5700) [链接](https://github.com/evenlinyf/hackintosh-EFI-Z490A-i710700k-5700xt) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG STRIX Z490-A Gaming 吹雪 | [链接](https://github.com/evenlinyf/hackintosh-EFI-Z490A-i710700k-5700xt) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG Here                  | [链接](https://github.com/kreactnative/EFI-z490-rog-hero-XII-10900k-bigSur) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG STRIX Z490-E          | [链接](https://github.com/taoche/Z490-E-Hackintosh)          |          | i7-10700k + RX5700XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG STRIX Z490-F GAMING | [链接](https://github.com/ocean-bee/asus-strix-z490f-hackintosh) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG STRIZX Z490I          | [链接](https://github.com/jergoo/Hackintosh-ROG-STRIX-Z490I) |          | OC: i7-10700k + Radeon VII                                   |
| Asus ROG STRIX Z490-G WIFI     | [链接](https://github.com/DiZhou92/ROG-STRIX-Z490-G-WIFI-ASUS) [链接](https://github.com/tienthanght96/Asus-Rog-Z490-G-Hackintosh) [链接](https://github.com/LightFocus/ASUS-ROG-STRIX-Z490G-Hackintosh) |          |                                                              |
| ASUS Z490M Plus   | [链接](https://github.com/stevenliuit/Hackintosh-Intel-i7-10700k-ASUS-Z490m-plus-5500xt)          |          | INTEL® CORE™ i7-10700k + RX5500XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Z490 MAXIMUS XII FORMULA  | [链接](https://github.com/shijij/OSX_EFI_Asus_Z490_MAXIMUS_FORMULA) |          | i7-10700k + RX5700XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus TUF Z490 Plus             | [链接](https://github.com/horphi/Asus-TUF-Z490-Plus) [链接](https://github.com/raofeng/ASUS_TUF_Z490_PLUS_WIFI_EFI) |          | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus ROG MAXIMUS XIII HERO | [链接](https://github.com/Dave1482/Maximus-XIII-Hero-Z590-11900K-6800XT-OpenCore-EFI-Public) | |  |
| ASUS PRIME Z590-P | [链接](https://github.com/rafaelmaeuer/Asus-Z590-P-Hackintosh) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASUS ROG Z590-A-Gaming-WIFI-II | [链接](https://github.com/cuihairu/ROG-STRIX-Z590-A-i910900K-RX6900XT-Hackintosh) | | i9-10900k + RX6900XT <br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASUS ROG STRIX Z690-A GAMING WIFI | [链接](https://github.com/cuihairu/ROG-STRIX-Z690-A-GAMING-WIFI-i513600KF-RX6600XT-Hackintosh) | | i5-13600kF + RX6600XT <br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASUS ProArt Z690 CREATOR WIFI | [链接](https://github.com/cuihairu/ProArt-Z690-CREATOR-WIFI-W5700-i912900K-Hackintosh/blob/main/README.md) | | i9-12900K + W5700 <br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus Prime Z690M Plus | [链接](https://github.com/Xmingbai/ASUS-Z690M-PLUS-hackintosh) | |  |
| ASUS TUF GAMING B760M-PLUS WIFI | [链接](https://github.com/cuihairu/TUF-GAMING-B760M-PLUS-WIFI-i714700KF-RX6950XT-Hackintosh) | | i7-14700kF + RX6950XT <br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| ASUS PRIME Z790 P WIFI D4 | [链接](https://github.com/Fu-Yuxuan-hub/ASUS-PRIME-Z790-P-WIFI-D4-HACKINTOSH) | | |
| ASUS ProArt Z790 CREATOR WIFI | [链接](https://github.com/cuihairu/ProArt-Z790-CREATOR-WIFI-RX6950XT-i914900K-Hackintosh) | | i9-14900k + RX6950XT <br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus X299 PRIME DELUXE II      | [链接](https://github.com/yifan-gu/hackintosh)               |          | i9 7980XE + Radeon VII<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus X299                      |      |          |                                                              |
| Asus ROG STRIX X299-E GAMING   | [链接](https://github.com/Fansaly/X299-STRIX-macOS)          |          | INTEL® CORE™ i7-7800X<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Asus合集 | [链接](https://github.com/Baio1977/EFI-Varie-Hackintosh/tree/main/EFI%20Desktop/ASUS) | |  |


### Dell 戴尔

| **台式（部分）**                           | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Dell ChengMing 3980                        | [链接](https://github.com/Triment/efi-hackintosh-chengming3980) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Dell ChengMing 3991                        | [链接](https://github.com/istarmeow/Hackintosh-Dell.ChengMing.3991-OpenCore.0.7.0-macOS.Big.Sur.11.4) |                                                              |                                                              |
| Dell Inspirion 3670                        | [链接](https://github.com/trunglemobiledev/oc_dell_inspiron_3670) |                                                              |                                                              |
| Dell Insprion 3881                         | [链接](https://github.com/H-Duy/Hackintosh-EFI)              |                                                              |                                                              |
| Dell OptiPlex 760                          |                                                              |                                                              |                                                              |
| Dell Optiplex 3046 SFF                     | [链接](https://github.com/JackCHENxx/Dell-Optiplex-3046-MFF-hackintosh-EFI) |                                                              |                                                              |
| Dell OptiPlex 3050                         | [链接](https://github.com/Leif160519/Dell-OptiPlex-3050-EFI) [链接](https://github.com/fgprodigal/Optiplex-3050-EFI-OC)<br />[链接](https://github.com/mxltxt/Dell-OptiPlex-3050-OC-EFI) |                                                              |                                                              |
| Dell OptiPlex 3070                         | [链接](https://github.com/bfrorum10/DELL-3070-MFF-Catalina-10.15.6-OC-0.5.9) [链接](https://github.com/zzkenkashjzz/Dell3070SFF-EFI-OpenCore)<br />[链接](https://github.com/pdff/Hackintosh-Dell-Optiplex3070SFF) [链接](https://github.com/ifantasyw/dell-3070mff-efi) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell OptiPlex 3080                         | [链接](https://github.com/ifantasyw/dell-3080mff-efi) [链接](https://github.com/ChunixZ/dell-optiplex-3080mff-opencore) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell Optiplex 5040                         | [链接](https://github.com/PeckishLeopard/OPTIPLEX-5040-Catalina-Big-Sur-EFI) |                                                              |                                                              |
| Dell Optiplex 5060MFF                      | [链接](https://github.com/uouuou/OpenCore_DELL_5060MFF_EFI)  |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell Optiplex 5070mff                      | [链接](https://github.com/WingLim/Dell-Optiplex-5070mff-Hackintosh) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)<br />MicFix:[链接](https://github.com/WingLim/MicFix) |
| Dell Optiplex 7010                         | [链接](https://github.com/Abbasm234/Dell_Optiplex_7010_Opencore0.6.5_EFI) [链接](https://github.com/karam-araby/dell-optiplex-7010-bigsur-EFI-Open-Core-0.6.6) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell Optiplex 7020 SFF/MT                  | [链接](https://github.com/zearp/OptiHack)                    |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell OptiPlex 7040                         | [链接](https://github.com/optiplex-osx/Dell-OptiPlex-7040-Clover-EFI) [链接](https://github.com/monaive/DELL-OptiPlex-7040-Clover) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell OptiPlex 7050                         | [链接](https://github.com/kuaima/Dell-OptiPlex-7050-Clover-EFI) [链接](https://github.com/linkev/Dell-Optiplex-7050-Micro-Hackintosh) | [链接](https://github.com/linkev/Dell-Optiplex-7050-Micro-Hackintosh) | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com)      |
| Dell OptiPlex 7060<br />Dell OptiPlex 7070 | [链接](https://github.com/W-MS/OptiPlex-7060and7070-Catalina) [链接](https://github.com/Jianhua-Wang/DELL-Optiplex-7060-7040-Clover)<br />[链接](https://github.com/webleon/Hackintosh-OptiPlex-7060-MFF) |                                                              | Increase DVMT to 64M `setup_var 0x8DC 0x2` ，不支持 96M 模式，<br />切勿使用 0x3 或在其他型号使用此命令。支持 Catalina。<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell OptiPlex 7060 Micro                   | [链接](https://github.com/binwan-dev/Hackintosh-OC-Dell-Optiplex-7060-Micro) |                                                              |                                                              |
| Dell OptiPlex 7080 MFF                     | [链接](https://github.com/jerryhan77/dell-optiplex-7080mff-opencore) [链接](https://github.com/webleon/Hackintosh-OptiPlex-7080-MT) |                                                              |                                                              |
| Dell OptiPlex 7080 MT                      | [链接](https://github.com/webleon/Hackintosh-OptiPlex-7080-MT) |                                                              |                                                              |
| Dell OptiPlex 9020M                        | [链接](https://github.com/mingcheng/dell-optiplex-9020m-hackintosh) [链接](https://github.com/JimLee1996/Hackintosh_OptiPlex_9020)<br /> [链接](https://github.com/W-MS/OptiPlex-9020-Catalina) [链接](https://github.com/chencaidy/Hackintosh-OC-Optiplex-9020M)<br />[链接](https://github.com/daliansky/Dell-OptiPlex-9020M-Hackintosh) |                                                              | Disable MSR 0xE2 (i.e. cfg lock) `setup_var 0xDA2 0x00`<br /> Increase DVMT to 96M `setup_var 0x263 0x03`<br /> 链接 3 支持 Catalina<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell PowerEdge T30                         | [链接](https://github.com/cstrouse/Dell-PowerEdge-T30-Hackintosh) |                                                              |                                                              |
| Dell Precision 3240                        | [链接](https://github.com/billzhong/dell-precision-3240-compact-hackintosh) [链接](https://github.com/billzhong/dell-precision-3240-compact-hackintosh) |                                                              | i5 10500 / 10600                                             |
| Dell Pricision 3520                        | [链接](https://github.com/sdh0618/Pricision-3520-EFI-Catalina) |                                                              |                                                              |
| Dell Precision T3610                       | [链接](https://github.com/cstrouse/Dell-T3610-Hackintosh)    |                                                              |                                                              |
| Dell Precision T3620                       | [链接](https://github.com/fivestrong/Hackintosh-Dell-Precision-T-3620) |                                                              |                                                              |
| Dell Precision M4800                       | [链接](https://github.com/hansyao/Hackintosh_Monterey_M4800) |                                                              |                                                              |
| Dell Precision 7520                        | [链接](https://github.com/TECHNIKVERBOT/Dell-Precision-7520-OpenCore) |                                                              |                                                              |
| Dell Vostro 3267                           | [链接](https://github.com/Drovosek01/hackintosh_DELL_Vostro_3267_i5-6400/blob/master/docs/ENG/README.md) |                                                              |                                                              |
| Dell Vostro 3669                           | [链接](https://github.com/daliansky/Dell_Vostro_3669_Hackintosh) |                                                              |                                                              |
| Dell Vostro 3470                           | [链接](https://github.com/sunnycityf/Dell-Vostro-3470-OpenCore-EFI) |                                                              |                                                              |
| Dell Vostro 3681                           | [链接](https://github.com/wjx0912/dell_3681_hackintosh_opencore) |                                                              | i7-10700 + intel AX210                                       |
| Dell XPS 8940                              | [链接](https://github.com/daniyo27/XPS8940-OpenCore)         |                                                              | 可能也支持 Dell G5 5090 Gaming Desktop<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Dell XPS 8940                              | [链接](https://github.com/LongTaiJun/Dell-XPS-8940-Hackintosh) |                                                              |                                                              |

### Gigabyte 技嘉

| **台式（部分）**                | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Gigabyte GB-BXi5H-4200 系列主板     | [链接](https://github.com/RehabMan/Gigabyte-BRIX-s-DSDT-Patch) | [链接](https://www.tonymacx86.com/threads/guide-gigabyte-brix-using-clover-uefi-gb-bxi5h-4200-gb-bxi5-4570r-gb-bxi7-4770r.261710/) | 技嘉 GB-BXi5H-4200 系列主板                                  |
| Gigabyte B85-HD3                | [链接](https://github.com/lttztt/B85-i5_4590-HACKINTOSH-Clover-EFI) |                                                              | i5-4590 / RX570                                              |
| Gigabyte GA-B85M-D3H            | [链接](https://github.com/zbum/EFI_OC)                       |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte GA-B150-DS3H           | [链接](https://github.com/Mr-he199696/I7-7700-GA-B150-DS3H-RX570) |                                                              |                                                              |
| Gigabyte B150M-VP               | [链接](https://github.com/migftw/Skylake-Hackintosh-Catalina) |                                                              |                                                              |
| Gigabyte B250M-D3H              | [链接](https://github.com/beyondgary/Hackintosh_i5-7500_B250_HD630_EFI) |                                                              |                                                              |
| Gigabyte B365M AORUS            | [链接](https://github.com/BenjaminZWQ001/AORUS-B365M-EFI)          |                                                              |                                                              |
| Gigabyte B360M AORUS PRO        | [链接](https://github.com/liangzhenduo0608/hackintosh-efi) [链接](https://github.com/HoracePeng/hackintosh-b360m-opencore)<br />[链接](https://github.com/FFFFOX/Gigabyte-B360M-Aorus-Pro-Hackintosh-EFI) |                                                              | 备注：链接 2/3 为 OC                                       |
| Gigabyte B360 M AORUS PRO ATX   | [链接](https://github.com/wangwanjie/Gigabyte-B360-EFI)      |                                                              |                                                              |
| Gigabyte B360 AORUS Gaming 3    | [链接](https://github.com/littlegtplr/Hackintosh-Clover-folder-for-Coffee-Lake-builds) |                                                              |                                                              |
| Gigabyte B360M D2V | [链接](https://github.com/Matchas-xiaobin/EFI-B360m_d2v_OpenCore_dvi_uhd630) | | 技嘉B360m，支持DVI输出 |
| Gigabyte B360M D3H              | [链接](https://github.com/laelsirus/GA-B360M-D3H-with-UHD630-iGPU-AMD-dGPU-CLOVER) |                                                              | GA-B360M-D3H                                                 |
| Gigabyte B360M DS3H             | [链接](https://github.com/sqlsec/B360M-DS3H-I5-9600KF-RX580-CLOVER) |                                                              | 国光自用：i5-9600KF RX580                                    |
| Gigabyte B365M Aorus Elite      | [链接](https://github.com/ChuanfengZhang/Gigabyte-B365M-UHD630-Clover) [链接](https://github.com/hookybaby/hackintoshEFI) | [链接](https://www.bugprogrammer.me/2020/05/27/Hackintosh_for_Z490_10900K.html) | Gigabyte B365M i5-9400 UHD630 Clover config<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Gigabyte B460M Aorus Pro        | [链接](https://github.com/dovtuan/Gigabyte-B460M-Aorus-Pro-Hackintosh-Open-Core) [链接](https://github.com/duongnguyensr/opencore-efi)<br />[链接](https://github.com/nhd2106/EFI-Hackintosh-B460M-Aorus-Pro-Core-i5-10400-RX-580-wifi-intel-AX200) |                                                              | i5-10400 / RX570<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte B460M-DS3H             | [链接](https://github.com/bangbaew/Gigabyte-B460M-DS3H-Hackintosh) |                                                              | i5-10400 / RX480<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte B560M AORUS PRO        | [链接](https://github.com/Vepoe/Gigabyte_B560m_Aorus_Pro-10400-5500xt-EFI) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabytes B560M AORUS Pro AX | [链接](https://github.com/geminiwen/Gigabyte_B560m_AORUS_PRO_AX_i5_11600K) [链接](https://github.com/imcczy/Gigabyte_B560m_AORUS_PRO_AX_10850K_6900XT_EFI) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte C246 WU4               | [链接](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC) |                                                              | Intel Xeon E-2278G / Sapphire RX 5500XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Designaire Z390        | [链接](https://github.com/baughmann/designaire-z390-intel-i9-9900k-opencore) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| G1 sniper M7 intel B150M        | [链接](https://github.com/infonekingdom/G1M7)                |                                                              |                                                              |
| Gigabyte H81M-D2 | [链接](https://github.com/cmd2001/GA-H81M-D2-i5_4590-GT730-Opencore-BigSur) | | |
| Gigabyte H110M-H                | [链接](https://github.com/suggested-username/EFI-GIGABYTE-H110M-H-BIGSUR-OPENCORE) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte mdh11ki                | [链接](https://github.com/wtsjw/Gigabyte-mdh11ki-hackinosh-EFI) |                                                              | 也适用于 Gigabyte mdh11hi                                    |
| Gigabyte H110m sh2              | [链接](https://github.com/DMNerd/Hackintosh_EFI)             |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte H110M S2HP             | [链接](https://github.com/teodorcucu/Hackintosh-Skilake-GA-H110M-S2HP-EFI) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte H170 HD3               | [链接](https://github.com/yrambler2001/Hackintosh-Intel-Core-i5-6500-Gigabyte-GA-H170-HD3-iGPU-OpenCore) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte H310M A 2.0 R1 | [链接](https://github.com/dclive/H310MA20r1) | |  |
| Gigabyte H310M DS2 2.0 | [链接](https://github.com/hid0/efi-oc-hackintosh-coffeelake-i3-9100f) | | |
| Gigabyte H370m D3h              | [链接](https://github.com/ahmedrafayat/OC-EFI-i7-8700)       |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte H370 HD3               | [链接](https://github.com/ktg5/H370-HD3-Hackintosh-OC)       |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte H410MH                 | [链接](https://github.com/aspisklov/EFI_i3-10100-Gigabyte-H410M-H) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte H410M S2H              | [链接](https://github.com/Pass-Ingby/Hackintosh-EFI-Gigabyte-H410M-S2H-i5-10400-iGPU-UHD630-OpenCore-v067) |                                                              |                                                              |
| Gigabyte H470I AORUS PRO AX     | [链接](https://github.com/ljzxzxl/gigabyte-h470i-hackintosh-efi) |                                                              |                                                              |
| Gigabyte X299 Aorus Ultra Gamin | [链接](https://github.com/Inmike02/X299-EFI)                 |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte X299 Designare EX | [链接](https://github.com/Inmike02/X299-EFI) | |  |
| Gigabyte X370N                  | [链接](https://github.com/qinkangdeid/z370n-wifi-hackintosh) |                                                              | Gigabyte Z370N                                               |
| Gigabyte H87M-D3H               | [链接](https://github.com/aqeebimtiaz/EFI-for-Mojave-Hackintosh-Gigabyte-H87M-D3H-i34440-HD4600-8GB) |                                                              |                                                              |
| Gigabyte GA-Z170XP-SLI          | [链接](https://github.com/novseje/ga-z170xp-sli-hackintosh-clover) |                                                              |                                                              |
| Gigabyte Z270X-UD3              | [链接](https://github.com/cfryerdev/efi-opencore-7700K-Z270X-UD3) |                                                              | OpenCore 0.6.0<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z270X-UG               | [链接](https://github.com/icedterminal/ga-z270x-ug)          | [链接](https://github.com/icedterminal/ga-z270x-ug/blob/master/README.md) | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z370N WIFI             | [链接](https://github.com/b166ar/Mac-Mini-Killer) [链接](https://github.com/yangbe/z370n-wifi-vega64) [链接](https://github.com/zhangdongpo/Z370N-Wi-Fi-Hackintosh-EFI)<br />[链接](https://github.com/edenpulse/z370n-i7-8700K-RX5700XT-Odin) [链接](https://github.com/bdragonh/T480S-BIGSUR-EFI) |                                                              | Mac-Mini-Killer<br />Z370N WIFI VEGA64                       |
| Gigabyte Z370 HD3               | [链接](https://github.com/Hasodikis/GA-Z370-HD3-Hackitosh-BIG-SUR) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z370 HD3P              | [链接](https://github.com/kinoute/Hack-Z370-HD3P-i5-8400)    |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 AORUS             | [链接](https://github.com/cmer/gigabyte-z390-aorus-master-hackintosh) |                                                              | **备注：**<br />如果不是 9900k/9700k/8500/8700k CPU，<br />需要打`Device RTC`补丁<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 AORUS ELITE       | [链接](https://github.com/liusming/hackintosh)               |                                                              | I9-9900K/Intel (Z380) HD 630 2G<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 Aorus Pro         | [链接](https://github.com/sarkrui/Hackintosh-Z390-Aorus-Pro-9700K-RX580) |                                                              | OpenCore/i7-9700K/蓝宝石 RX580 8G<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 AORUS PRO         | [链接](https://pcpartpicker.com/product/L9YLrH/gigabyte-z390-i-aorus-pro-wifi-mini-itx-lga1151-motherboard-z390-i-aorus-pro-wifi) |                                                              | WIFI Mini ITX<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 AORUS PRO WIFI    | [链接](https://github.com/shiruken/hackintosh) [链接](https://github.com/FlopRe/hackintosh-Z390-gigabyte-aorus-pro-wifi-OpenCore-9600K-iGPU) |                                                              | i7-9700K + Radeon RX 5700 XT                                 |
| Gigabyte Z390 Master            | [链接](https://github.com/felixyin/clover-z390master-i99900k-rx580-970pro) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 AORUS MASTER ATX  | [链接](https://github.com/vmzhivetyev/hackintosh-efi)        |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 DESIGNARE         | [链接](https://github.com/joostiphone/Z390-Hackintosh-Joost) [链接](https://github.com/Mac944/Opencore-i9-9900K-Z390-Designare-RX-6800XT) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 I Aorus Pro WiFi  | [链接](https://github.com/vfalanis/opencore-aorus-z390i-pro-wifi) [链接](https://github.com/WJingC/Gigabyte-Z390-I-Hackintosh-OpenCore) |                                                              |                                                              |
| Gigabyte Z390 M Gaming          | [链接](https://github.com/tspng/gigabyte-z390-m-gaming-hackintosh) |                                                              | 技嘉 Z390m<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 gaming            |                                                              | 小辉自用: i5-9600k RX580 2304sp 矿                           | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 Gaming X          | [链接](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh) [链接](https://github.com/L0ngxhn/hackintosh-GIGABYTE-Z390-GAMING-X) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 M                 | [链接](https://github.com/xxiaofeng132/Gigabyte-Z390M-Gaming-Hackintosh) |                                                              | 技嘉 Z390m-gaming<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390 Ultra             | [链接](https://github.com/mrpaulphan/gigabyte-z390-ultra-master-hackintosh) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z390-UD                | [链接](https://github.com/kong-git/Z390-OC-UHD630) [链接](https://github.com/kong-git/Z390-UD-RX580)<br />[链接](https://github.com/shayinqi/Hackintosh-opencore-giga-z390ud-efi-5700xt) |                                                              | OpenCore 核显/RX580 独显<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 AORUS ELITE       | [链接](https://github.com/bugprogrammer/hackintosh/tree/Z490-AORUS-ELETE+10900K+RX5700XT) [链接](https://github.com/tuanht/hackintosh-10600k-z490-aorus-elite-5700xt) |                                                              | OC: 10900K+5700XT<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 AORUS Pro AX      | [链接](https://github.com/ankanpratik/Gigabyte-Z490-AORUS-Pro-AX-EFI-OpenCore-) [链接](https://github.com/zxyboy/i9-10850K-Z490-AORUS-PRO-AX) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 AORUS Master      | [链接](https://github.com/hoangviet/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Aorus-Master) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 Aorus Ultra       | [链接](https://github.com/tagyro/Hackintosh_Gigabyte_Z490_Aorus_Ultra) [链接](https://github.com/rayovims/Hackintosh-EFI-Partion) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 UD                | [链接](https://github.com/adrianlungu/OpenCore-Z490-UD-rev-10) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 Vision D          | [链接](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D) [链接](https://github.com/xiaovie/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D)<br />[链接](https://github.com/rursache/Hackintosh-i9-10900k-Z490-Vision-G) [链接](https://github.com/eos-alchemist/EFI.Z490.Vision.D) |                                                              | OC: 10900K+Radeon VII<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 Vision G          | [链接](https://github.com/georgetree/hackintosh-10700k-Gigabyte-Z490-Vision-g) [链接](https://github.com/samuel21119/Intel-i9-10900-Gigabyte-Z490-Vision-G-Hackintosh)<br />[链接](https://github.com/5T33Z0/Gigabyte-Z490-Vision-G-Hackintosh-OpenCore) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490 Gaming X          | [链接](https://github.com/weiyien/Hackintosh_GIGABYTE_Z-490_I5-10400) [链接](https://github.com/SwimmingPig/Hackintosh-Intel-i5-10400-Gigabyte-Z490M-Gaming-X) |                                                              | OC:10400+RX5500XT(核显没驱动,另外处理)<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490M Gigabyte Z490 | [链接](https://github.com/Matt-dere/Hackintosh-Intel-i9-10850k-Gigabyte-Z490-AirDrop-AMD-580-IGPU) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z490I AORUS ULTRA      | [链接](https://github.com/abing258/z490i-i9-10850k-5500xt)   |                                                              | i9-10850k RX5500XT                                           |
| Gigabyte Z590 Aorus  Master | [链接](https://github.com/Cam396/Aorus-Z590-Master-EFI) | |  |
| Gigabyte Z590 Vision D | [链接](https://github.com/luchina-gabriel/GIGABYTE-Z590-VISION-D-10900K-RX-6900XT) | | |
| Gigabyte Z590 Vision G | [链接](https://github.com/chuihairu/GIGABYTE-Z590-G-i510500-RX5600XT-Hackintosh)| | i510500K + RX5600XT + 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)  |
| Gigabyte Z590M Gaming X | [链接](https://github.com/luchina-gabriel/EFI-GIGABYTE-Z590M-GAMING-X-11900K-ES-QV1K-RX6900XT) | | |
| Gigabyte Z690 Aorus Elite AX | [链接](https://github.com/luchina-gabriel/EFI-GA-Z690-AORUS-ELITE-AX-12900K-RX6900XT) [链接](https://github.com/rursache/Hackintosh-13900k-Z690-AORUS-ELITE-AX-DDR5-AMD-6900XT) | | 链接2为Intel 13900k |
| Gigabyte Z690 Aorus Pro | [链接](https://github.com/kreactnative/Z690-12900K-RX6600XT-DDR5-Monterey) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z690I Aorus | [链接](https://github.com/glekner/Z690I-AORUS-OC-EFI) | | |
| Gigabyte Z690 Gaming X          | [链接](https://github.com/bestplay9384/EFI-GIGABYTE-Z690-Gaming-X-DDR4-12700K-RX5700XT-Hackintosh) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| Gigabyte Z790 Aorus Elite | [链接](https://github.com/Xmingbai/Gigabyte-Z790-Aorus-Elite-13900KF-hackintosh) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z790 Aorus Master | [链接](https://github.com/casstsai/13900k-z790-aorus-master) | | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| Gigabyte Z77P D3                | [链接](https://github.com/cloverkits/GA-Z77P-D3-EFI)         |                                                              | GA-Z77P-D3                                                   |
| Gigabyte Z77X D3H               | [链接](https://github.com/nickw444/opencore-efi)             |                                                              |                                                              |
| Gigabyte GA-Z77X-DS3            | [链接](https://github.com/tdyn2000/GIGA-Z77X-DS3-Catalina-EFI) |                                                              |                                                              |
| Gigabyte Z97n WiFi              | [链接](https://github.com/POP3UR/EFI-Opencore-z97n-Big-Sur)  |                                                              |                                                              |
| Gigabyte Z97 D3H                | [链接](https://github.com/betteray/OpenCore-EFI-Actions) |                                                              | GIGABYTE Z97n WiFi                                           |
| Gigabyte Z97X Gaming 5          | [链接](https://github.com/amogh-w/Hackintosh-4790K-Z97X-GTX-960) [链接](https://github.com/maximum-maxness/Z97MX-Gaming-5-4790K-Hackintosh) |                                                              |                                                              |
| Gigabyte 合集                   | [链接](https://github.com/Baio1977/EFI-Varie-Hackintosh/tree/main/EFI%20Desktop/GIGABYTE) |                                                              |                                                              |

### HP 惠普

| **台式（部分）**             | 发布地址                                                     | 教程地址 | 备注              |
| ---------------------------- | ------------------------------------------------------------ | -------- | ----------------- |
| HP 288 Pro G5 | [链接](https://github.com/liuqqqhuan/HP-288PRO-G5-EFI) |  |  |
| HP Compaq Pro 4300           | [链接](https://github.com/ichelash/HP4300EFI)                |          |                   |
| HP EliteDesk 400 G1 DM       |                                                              |          |                   |
| HP EliteDesk 800 G1 DM/USDT  |                                                              |          |                   |
| HP EliteDesk 800 G2          | [链接](https://github.com/taitran91095/HP800-G2-Mini-OpenCore) [链接](https://github.com/impulse/OpenCore-EliteDesk-800-G2SFF) |          |                   |
| HP EliteDesk 800 G2 DM       | [链接](https://github.com/randyzhong/HP-EliteDesk-800-G2-DM-Hackintosh) |          |                   |
| HP EliteDesk 800 G2 Tower PC | [链接](https://github.com/sakoula/HP-EliteDesk-800-G2-6700)  |          | i7-6700 (Skylake) |
| HP EliteDesk 800 G3          | [链接](https://github.com/lavjamanxd/hp-elitedesk-g3-hackintosh) |          |                   |
| HP EliteDesk 800 G3 DM       | [链接](https://github.com/randyzhong/OS-X-HP-EliteDesk-800-G3-DM-Clover) |          |                   |
| HP EliteDesk 800 G3 Mini     | [链接](https://github.com/francoisminh/Hackintosh-EliteDesk-800-G3-Mini-65W) |          |                   |
| HP EliteDesk 800 G4 DM       | [链接](https://github.com/jerry31279/HP-EliteDesk-800-G4-DM-35W-RX560) |          |                   |
| HP EliteDesk 800 G4 Mini     | [链接](https://github.com/itskaizad/Elitedesk-800-G4-Hackintosh) [链接](https://github.com/Shadowghost/elitedesk-800-g4-mini-macos-efi) |          |                   |
| HP EliteDesk 800 G5 Mini     | [链接](https://github.com/Haveacry/OpenCore_HP-EliteDesk-800-G5-DM) [链接](https://github.com/m-zaw/HP-EliteDesk-800-G5-Mini-Hackintosh) |          |                   |
| HP Elite Slice               | [链接](https://github.com/demon3434/Hackintosh-EFI-HP_Elite_Slice)                                                                         |      | 网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com)    |
| HP Hamar-powered PC | [链接](https://github.com/QuanTrieuPCYT/HPHamar_Hackintosh) | | |
| HP Omen 30L                                     | [链接](https://github.com/ethlocker/hp_omen_30L_big_sur_hackintosh) |                                                              | CPU: Core i9-10000k Comet lake<br />AMD Radeon RX 580        |
| Hp Prodesk 400G2 DM          | [链接](https://github.com/july929/Hackintosh-Hp-Prodesk-400G2-DM-EFI) |          |                   |
| HP Prodesk 400 G4 MT         |                                                              |          |                   |
| HP Prodesk 400 G6            | [链接](https://github.com/duccnv-1684/OC_HP_Prodesk_400_G6)  |          |                   |
| HP ProDesk 480 G4            | [链接](https://github.com/SummerEmber/HP-ProDesk-480-G4)     |          |                   |
| HP Prodesk 600 G1 DM         | [链接](https://github.com/ZqinKing/EFI-HP-ProDesk-600-G1-DM) [链接](https://github.com/Mr-Zhang-1/600G1-DM-BigSur-OC) |          |                   |
| HP Prodesk 600 G1 SFF        | [链接](https://github.com/kidddjh/HP-Prodesk-600-G1-SFF)     |          |                   |
| HP ProDesk 600 G2 DM         | [链接](https://github.com/wcjxixi/HP-ProDesk-600G2-DM-Hackintosh) [链接](https://github.com/ningye2012/HP-600G2-DM-Hackintosh) |          |                   |
| HP Prodesk 600 G3 | [链接](https://github.com/omriberchman/HP-prodesk-600-G3-Hackintosh-EFI-OpenCore-) | | |
| HP ProDesk 600 G4            |                                                              |          |                   |
| HP Z420                      | [链接](https://github.com/yansheng1003/Hackintosh) [链接](https://github.com/joepool/Hackintosh-HP-Z420-OpenCore) |          | E5 1650v2         |
| HP ProDesk 680 G3 Mt         | [链接](https://github.com/ivan19871002/HP-ProDeks-680-G3-MT-Hackintosh)	|		|		|
| HP Z600 Workstation          |                                                              |          | Mac-Mini-Killer   |
| HP Z620 Workstation          | [链接](https://github.com/d4vinder/HP-Z620-Hackintosh-macOS-Catalina) [链接](https://github.com/mokiii/HP-Z620-Hackintosh-macOS_10.13-10.15) |          |                   |
| HP ZBook G1	|[链接](https://github.com/bangmaple/HP-ZBook-G1-OpenCore)	|		|		|
| HP EliteBook 850G3	|[链接](https://github.com/lucasrequile/OCEliteBook850G3)	|		|		|
| HP Z230 SFF Workstation	|[链接](https://github.com/keczejo/HP-Z230-Hackintosh)	|		|		|
| HP ZHAN 99 Pro G1 MT         | [链接](https://github.com/Z-fly/HP-ZHAN-99-Pro-G1-MT-Hackintosh) |          | UHD630            |

### Intel 英特尔

| **台式（部分）**          | 发布地址                                                                                                                                                                         | 教程地址                                                                                                                          | 备注                                            |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Intel NUC 5、6、7、8 系列 | [链接](https://github.com/RehabMan/Intel-NUC-DSDT-Patch)                                                                                                                         | [链接](https://www.tonymacx86.com/threads/guide-intel-kaby-lake-nuc7-using-clover-uefi-nuc7i7bnh-nuc7i5bnk-nuc7i3bnh-etc.261711/) | mini 主机                                       |
| **NUC9QNX** | [链接](https://github.com/daliansky/Intel-NUC9-Hackintosh) | [链接](https://item.taobao.com/item.htm?id=732931461537) [链接](https://blog.daliansky.net/Intel-NUC9-Hackintosh-and-macOS-Sonoma-Installation-Tutorial.html) | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| NUC5I5RYH                 | [链接](https://github.com/rangerwill/nuc5i5ryh-hackintosh-efi-catalina-10.15.7)                                                                                                  |                                                                                                                                   |                                                 |
| NUC6I5SYH                 | [链接](https://github.com/AnhTu6610/EFI-intel-nuc6i5syh)                                                                                                                         |                                                                                                                                   |                                                 |
| NUC8-BEH/BEK            | [链接](https://github.com/Lorys89/Intel-NUC8-Hackintosh)                                                                                                                                                         |                                                                                                                                 |                                        |
| NUC8I5BEH                 | [链接](https://github.com/dongyubin/nuc8i5beh) [链接](https://github.com/csrutil/NUC8I5BEH)                                                                                      | [链接](https://chengxuxiaohei.cn/mac-anzhuang.html) [链接](https://osy.gitbook.io/hac-mini-guide/)                                |                                                 |
| NUC8i5BEK                 | [链接](https://github.com/Hyejeongdd/NUC8i5BEK-Hackintosh)                                                                                                                       |                                                                                                                                   |                                                 |
| NUC8i7BEH                 | [链接](https://github.com/sarkrui/NUC8i7BEH-Hackintosh-Build) [链接](https://github.com/wilsonnkwan/Hackintosh-NUC8i7BEH-Catalina) [链接](https://github.com/honglov3/NUC8I7BEH) | [链接](https://osy.gitbook.io/hac-mini-guide/)                                                                                    | 链接 3 为`OC`                                   |
| NUC9I7QNX            | [链接](https://github.com/bemble/Hackintosh-NUC9I7QNX-OpenCore)                                                                                                                                                         |                                                                                                                                 |                                        |
| NUC7i7BNH                 | [链接](https://github.com/calebchow9/Intel-NUC7i7BNH-Hackintosh)                                                                                                                 |                                                                                                                                   |                                                 |
| NUC7i5BEK                 | [链接](https://github.com/331296441/NUC7i5BEK)                                                                                                                                   |                                                                                                                                   |                                                 |
| NUC10i7/i5/i3             | [链接](https://github.com/mbarbierato/Intel-NUC10i3FNK) [链接](https://github.com/HawkysCC/Hackintosh-NUC10i7) [链接](https://github.com/nuc-hackintosh/nuc10-efi)<br />[链接](https://github.com/hackintosh-efi/intel-nuc10)            |                                                                                                                                   | 支持 BigSur<br />链接 2 支持最新的 AirportItlwm |
| H610 | [链接](https://github.com/cuihairu/H610-i5-12400F-RX5600XT-Hackintosh) | | i5-12400F + RX5600XT + Intel AX210 |

### Lenovo 联想

| **台式（部分）**                           | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 联想 Lenovo 启天 M415-D339                 | [链接](https://github.com/static-host/Hackintosh-OpenCore)   |                                                              |                                                              |
| 联想 Lenovo 启天 M420-D046(C)              | [链接](https://github.com/crysehillmes/Hackintosh-Lenovo-M420-D046-C) [链接](https://github.com/july929/Lenovo-QiTian-M420-i3-8100-UHD630-OpenCore-EFI) | [链接](https://github.com/crysehillmes/Hackintosh-Lenovo-M420-D046-C/blob/main/README.cn.md) |                                                              |
| Lenovo TianQi M420                         | [链接](https://github.com/july929/Lenovo-QiTian-M420-i3-8100-UHD630-OpenCore-EFI) |                                                              |                                                              |
| 联想启天M425-N050 | [链接](https://github.com/bpefei/Lenovo-QiTian-M425-N050-OpenCore-EFI) | | |
| Lenovo 天逸 510S                           | [链接](https://github.com/274860460/lenovo-510s-i5-9400_HUD630_Hackintosh_EFI) |                                                              | i5-9400 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo 天逸 510S Mini                      | [链接](https://github.com/daliansky/Lenovo-TianYi-510S-Mini-Hackintosh) |                                                              | 联想天逸 510S Mini 小主机<br />小兵自用，长期维护<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo Ideacenter A340 | [链接](https://github.com/comp-labs/macOS-Kexts-for-Lenovo-Ideacenter-A340) | |  |
| Lenovo ThinkCentre M4500q                  | [链接](https://github.com/samawong/hackintosh-clover-configure-for-lenovo-m4500q-n000-model) |                                                              |                                                              |
| Lenovo ThinkCentre M710Q                   | [链接](https://github.com/daliansky/Lenovo-M710Q-Hackintosh) |                                                              | 小兵自用，长期维护<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo ThinkCentre M720Q                   | [链接](https://github.com/fronttang/Lenovo-ThinkCentre-M720Q-Hackintosh) [链接](https://github.com/tobagin/m720q-OpenCore-Catalina/)<br />[链接](https://github.com/revunix/ThinkCentre-M720Q) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo ThinkCentre e 73                    | [链接](https://github.com/riku2015/Efi-files-for-lenovo-e73) |                                                              |                                                              |
| Lenovo M73 Tiny                            | [链接](https://github.com/rehandalal/m73-tiny-hackintosh) [链接](https://github.com/yingw/Lenovo-ThinkCentre-M73-Tiny-Hackintosh)<br />[链接](https://github.com/SakuraiLH/Thinkcentre-m73-hackintosh-OPENCORE-EFI) |                                                              |                                                              |
| Lenovo ThinkCentre M93p Tiny               | [链接](https://github.com/mingcheng/lenovo-thinkcentre-m93p-hackintosh) [链接](https://github.com/SummerEmber/Lenovo-ThinkCentre-M93p-Tiny)<br />[链接](https://github.com/julioalvarezrd/ThinkCentre-M93p-Tiny-BigSur) [链接](https://github.com/riverLethe9/Thinkcentre-m93p-Tiny-EFI) |                                                              |                                                              |
| Lenovo Thinkcentre M910x                   | [链接](https://github.com/ylen0l/Hackintosh-Lenovo-Thinkcentre-M910x-OpenCore-Efi) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo ThinkCentre M920X | [链接](https://github.com/immwind/m920x-efi) | | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo ThinkStation P320 Tiny              | [链接](https://github.com/chencaidy/Hackintosh-OC-Lenovo-P320-Tiny) |                                                              |                                                              |
| Lenovo ThinkStation P340 Tiny | [链接](https://github.com/juebanlin/P340_Tiny_Opencore_EFI) | | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo Thinkcentre M920q                   | [链接](https://github.com/yuppiesnotzhuhao/Lenovo_M920Q_Hackintosh_Bigsur_OC) |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo Thinkpad P1 <br />MobileWorkStation | [链接](https://github.com/p455555555/Thinkpad-P1-EFI)        |                                                              | 网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Lenovo B360                                | [链接](https://github.com/ThrRip/OpenCore-EFI-Lenovo-B360-i5-8400) |                                                              | RX5500XT<br />                                               |
| Lenovo v410z                               | [链接](https://github.com/harriedgemusic/macOS_Catalina_Lenovo_v410z_CLOVER_EFI) |                                                              | |
| Lenovo Thinkpad T450/T450s	|[链接](https://github.com/racka98/Lenovo-Thinkpad-T450-T450s-Hackintosh-Guide-Opencore)	|		|		|



## Minisforum 铭凡

| **台式（部分）** | 发布地址 | 教程地址 | 备注 |
| ---------------- | -------- | -------- | ---- |
| minisforum B550 | [链接](https://github.com/daliansky/minisforum-Elitemini-B550-Hackintosh) |  | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| **minisforum HX80G / HX90G** | [链接](https://github.com/daliansky/minisforum-HX90G-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| minisforum NAG6              | [链接](https://github.com/daliansky/minisforum-NAG6-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| minisforum U820              | [链接](https://github.com/daliansky/minisforum-u820-hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| minisforum UM480XT           | [链接](https://github.com/daliansky/minisforum-UM480XT-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| minisforum UM560XT           | [链接](https://github.com/daliansky/minisforum-UM560XT-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| minisforum UM580D/UM590      | 链接                                                         |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |

### MSI 微星

| **台式（部分）**                                  | 发布地址                                                     | 教程地址                                                     | 备注                                                         |
| ------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| MSI B250M-E                                       | [链接](https://github.com/rakiy/Hackintosh_MSI_B250M_EFI)    |                                                              |                                                              |
| MSI B250 GAMING PRO CARBON                        | [链接](https://github.com/AurelienAudero/i5-7400-EFI-by-Aure) |                                                              |                                                              |
| MSI B250M MORTAR                                  | [链接](https://github.com/SummerEmber/MSI-B250M-MORTAR)      |                                                              |                                                              |
| MSI B350M MORTAR                                  | [链接](https://github.com/VenenoSix24/MSI-B350M-MORTAR-Hackintosh-OpenCore-EFI) |                                                              | R5 5500 + RX 5700                                            |
| MSI B360                                          | [链接](https://github.com/SuperNG6/MSI-b360-10.14.4-EFI)     |                                                              | 也适用于<br />MAG Z390 TOMAHAWK <br />(MS-7B18)<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI B360M Bazooka                                 | [链接](https://github.com/ririxidev/B360-macOS)              |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI B360M MORTAR                                  | [链接](https://github.com/andot/MSI-B360M-MORTAR-IMACPRO-EFI) [链接](https://github.com/ZzzM/Hackintosh-MSI-B360M-MORTAR) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI B360M i3-8100/rx570                           | [链接](https://github.com/shm007g/hackintosh-msi-b360m-i3-8100-rx570) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI B360M MORTAR                                  | [链接](https://github.com/GeQ1an/MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI) [链接](https://github.com/CeuiLiSA/Opencore-EFI) | [链接](https://github.com/GeQ1an/MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI/blob/master/README.md) | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI B365M Pro-VDH                                 | [链接](https://github.com/suggested-username/MSI-B365M-PRO-VDH-OPENCORE-HACKINTOSH) |                                                              |                                                              |
| MSI B460I GAMING EDGE WIFI                        | [链接](https://github.com/zhaxingyu/MSI-B460i-Hackintosh)    |                                                              |                                                              |
| MSI B460M MORTAR                                  | [链接](https://github.com/fpfeng/Hackintosh-10400-B460M-MORTAR) <br/>[链接](https://github.com/josways/B460M-MORTAR) <br />[链接](https://github.com/cheneyxx/Hackintosh-10400-B460M-MORTAR) |                                                              | I5-10400 / RX560 <br/> I5-10400 / RX550<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI MAG B560M MORTAR WIF                          | [链接](https://github.com/sqlsec/MSI-MAG-B560M-MORTAR-i7-10700) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI MAG B660M MORTAR                              | [链接](https://github.com/yzchan/MSI-MAG-B660M-MORTAR-DDR4-12600K-EFI) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MAG B660M MORTAR WIFI DDR4                        | [链接](https://github.com/abc408880155/12490F-MSI-B660M-D4-WIFI-MORTAR-RX6600-EFI) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI PRO B660M-A WIFI                              | [链接](https://github.com/laggykiller/Hackintosh_MSI_B660M-A_WIFI_DDR4) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI H270 GAMING M3                                | [链接](https://github.com/basett1/OPENCORE-EFI-MSI-H270-GC-TITAN-RIDGE) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI H410M-A PRO                                   | [链接](https://github.com/goomadao/MSI-H410M-A-PRO-OpenCore-EFI) [链接](https://github.com/jkimieck/MSI440_CATALINA) |                                                              |                                                              |
| MSI H410M-PRO-VH                                  | [链接](https://github.com/Abhinavcs7/EFI-For-MSI-H41OM-PRO---VH-MacOS-big-sur-) |                                                              | i3-10100                                                     |
| MSI H410M BOMBER                                  | [链接](https://github.com/dakezi/i3-10100-MSI-H410M-BOOMER-UHD630-Hackintosh-EFI) |                                                              | i3-10100                                                     |
| MSI H61-P31/W8                                    | [链接](https://github.com/rahmanhadi/EFI-CLOVER_MSI-H61)     |                                                              |                                                              |
| MSI H81M-IE35                                     | [链接](https://github.com/MoeGuoH/EFI-MSI-H81M-IE35)         |                                                              |                                                              |
| MSI H270 GAMING M3 + Thunderbolt 3 GC Titan Ridge | [链接](https://github.com/basett1/OPENCORE-EFI-MSI-H270-GC-TITAN-RIDGE) |                                                              |                                                              |
| MSI X99A Sli Plus                                 | [链接](https://github.com/gemini64/opencore-msi-x99a)        |                                                              |                                                              |
| MSI Z270 PC-MATE                                  |                                                              |                                                              |                                                              |
| MSI Z370-A                                        | [链接](https://github.com/daliansky/Z370-Hackintosh)<br />[链接](https://github.com/FrostMiKu/msi-z370-hackintosh) | [链接](https://github.com/daliansky/Z370-Hackintosh)         | 小兵自用，长期维护<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z370 OC Gaming                                | [链接](https://github.com/FrostMiKu/msi-z370-hackintosh)     |                                                              | LTS                                                          |
| MSI Z370m mortar                                  | [链接](https://github.com/JackyCZJ/Z370M-MORTAR-I7-9700K-M9PEG-CLOVER) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI Z370-TOMAHAWK                                 | [链接](https://github.com/luffythink/Hackintosh-EFI)         | [链接](https://github.com/luffythink/Hackintosh-EFI/blob/master/README.md) | clover 稳定版 and oc 版<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z390-A PRO                                    | [链接](https://github.com/filipac/Working-EFI-OpenCore-0.6.5-MSI-Z390PRO) |                                                              |                                                              |
| MSI Z390-Gaming-EDGE-AC                           | [链接](https://github.com/fnoopv/MSI-Z390-Gaming-Edge-AC_OC) |                                                              | 微星 MPG-Z390-Gaming-Edge-ac OpenCore EFI<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z390i Gaming EDGE AC                          | [链接](https://github.com/mojo2012/hackintosh-efi)           |                                                              |                                                              |
| MSI Z390i                                         | [链接](https://github.com/GaryOAO/MSI-Z390i-hackintosh-clover) |                                                              |                                                              |
| MSI Z390 gaming pro carbon                        | [链接](https://github.com/cangzhang/efi-for-9700k-msi-z390-gaming-pro-carbon) [链接](https://github.com/XXCoreRangerX/Hackintosh-Z390-9700K) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI MAG Z390 TOMAHAWK                             | [链接](https://github.com/xushuduo/MSI_Z390_TOMAHAWK_I5-9600K_HACKINTOSH_OPENCORE_EFI) [链接](https://github.com/eamonzzz/EFI-Z390-TOMAHAWK-RX590) |                                                              | MSI MAG Z390 TOMAHAWK + i5-9600K + RX590 HACKINTOSH OPENCORE EFI<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI MEG Z490 ACE                                  | [链接](https://github.com/kreactnative/z490-ace-10700k-catalina) [链接](https://github.com/kreactnative/EFI-z490-ace-10700k-bigSur) |                                                              | 链接 1 为 catalina，链接 2 为 Big Sur<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI MAG Z490 TOMAHAWK                             | [链接](https://github.com/Dir3Rav3n/MSI-MAG-Z490-TOMAHAWK-i7-10700-OpenCore-) [链接](https://github.com/Baio1977/MSI-MAG-Z490-Tomahawk-UHD630) |                                                              | i7-10700 / RX580<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z490-A PRO                                    | [链接](https://github.com/evling2020/OpenCore) [链接](https://github.com/ianchb/Hackintosh_EFI_OpenCore_MSI_Z490A_PRO_MS7C75) | [链接](https://github.com/ianchb/Hackintosh_EFI_OpenCore_MSI_Z490A_PRO_MS7C75/blob/main/README.md) | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)<br />显卡：蓝宝石 RX 6600XT<br />链接 2：5500XT+10600KF，核显未作测试 支持了 Ventura Beta |
| MSI Z490M Gaming Edge                             | [链接](https://github.com/redcweed/z490)                     |                                                              | Intel i7-10700 / XFX RX590<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z490 Gaming Plus                              | [链接](https://github.com/Flop88/opencore) [链接](https://github.com/ianchb/Hackintosh_EFI_OpenCore_MSI_Z490A_PRO_MS7C75) |                                                              | i5-10400f / RX550<br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z490i Unify                                   | [链接](https://github.com/kingwood77/MSI-Z490i-Unify-Hackintosh) [链接](https://github.com/wjz304/Hackintosh-EFI-MSI-Z490i-Unify)<br />[链接](https://github.com/diskerror/EFI) |                                                              | i5-10400 / RX580                                             |
| MSI Z490 S01                                      | [链接](https://github.com/jdjxk/Hackintosh_OpenCore_Z490_i9_10850K_RX5500XT) |                                                              | 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)      |
| MSI Z490 GODLIKE                                  | [链接](https://github.com/cuihairu/MEG-Z490-GODLIKE-i910900K-RX6900XT-Hackintosh) |                                                              | i9-10900k + RX6900XT <br />网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| MSI Z590i Unify                                   | [链接](https://github.com/malibio/msi-z590i-unify-opencore)  |                                                              |                                                              |                                                                                 |                 
| MSI PRO H610M-E                                   | [链接](https://github.com/cuihairu/MSI-PRO-H610M-E-i3-12100F-RX580-Hackintosh) |                                            | Intel i3-12100F RX580  网卡推荐：[BCM94360CD](https://hackintosher.taobao.com)    ||                
| MSI MPG Z690 EDGE TI                              | [链接](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT) |                                                              |                                                              |
| MSI Z790i EDGE                                    | [链接](https://github.com/conversun/Hackintosh-MSI-Z790i-EDGE-13900K-6900XT-OpenCore) |                                                              |                                                              |
| MSI Z97 Gaming 5                                  | [链接](https://github.com/plcharriere/Hackintosh/blob/master/Z97G5/) |                                                              | i5-4690K                                                     |
| MSI H81M P33                                      | [链接](https://github.com/inokoe/MSI-H81M-P33-Hackintosh-EFI) |                                                              | E3 1246 V3                                                   |

### Mini 迷你系列

| **台式（部分）**             | 发布地址                                                     | 教程地址                                                 | 备注                                                         |
| ---------------------------- | ------------------------------------------------------------ | -------------------------------------------------------- | ------------------------------------------------------------ |
| Asus PN62                    | [链接](https://github.com/cuteribs/hackintosh/tree/master/ASUS_PN62) |                                                          |                                                              |
| **Beelink EQR5**             | [链接](https://github.com/daliansky/Beelink-EQR5-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](                |
| Beelink SEi8                 | [链接](https://github.com/daliansky/Beelink-SEI8-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| Beelink SER5                 | [链接](https://github.com/daliansky/Beelink-SER5-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| Cloud Hin H170               | [链接](https://github.com/kdwycz/cloud-hin-h170-stx-hackintosh) [链接](https://github.com/matri/hipda-h170-opencore) |                                                          | 云轩 H170                                                    |
| FEVM FN60G & V2 & WE 水冷    | [链接](https://github.com/daliansky/FEVM-FN60G-Hackintosh)   |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| Deskmini-310                 | [链接](https://github.com/yuqi/Deskmini-310-Hackintosh)      |                                                          | Deskmini-310                                                 |
| **GEEKOM miniFun9**          | [链接](https://github.com/daliansky/Geekom-miniFun9-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| **GEEKOM miniFun11**         | [链接](https://github.com/daliansky/Geekom-miniFun11-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| GMKTEC NucBox2               | [链接](https://github.com/laggykiller/hackintosh-gmk-nucbox2) |                                                          | 网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com)      |
| Soarsea mini PC              | [链接](https://github.com/EngLearnsh/Soarsea-i9-8950HK-Hackintosh) |                                                          | S200H                                                        |
| **Soarsea S210H**            | [链接](https://github.com/daliansky/SoarSea-S210H-Hackintosh) | [链接](https://item.taobao.com/item.htm?id=693991506304) | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| **Soarsea P310S**            | [链接](https://github.com/daliansky/SoarSea-P310S-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| CM238 i7-8950H UHD630 ALC269 | [链接](https://github.com/kkzzhizhou/S200H_I7-8750H_Hackintosh) |                                                          | S200H_I7-8750H 小主机                                        |
| I7-8850H 迷你主机            | [链接](https://github.com/n0jack/i78850h-minipc-hackintosh)  |                                                          |                                                              |
| DQ77KB                       | [链接](https://github.com/siwilizhao/DQ77KB-I7-3770S-Hackintosh) |                                                          |                                                              |
| morefine S500                | [链接](https://github.com/daliansky/morefine-S500-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| **morefine M600s**           | [链接](https://github.com/daliansky/morefine-M600s-Hackintosh) | [链接](https://item.taobao.com/item.htm?id=659725057885) | 小兵长期维护机型<br />网卡推荐：[BCM94360Z3](https://hackintosher.taobao.com) |
| TinyMonster ECO              | [链接](https://github.com/daliansky/TinyMonsterECO-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |
| TinyMonster PRO              | [链接](https://github.com/daliansky/TinyMonsterPro-Hackintosh) |                                                          | 小兵长期维护机型<br />网卡推荐：[BCM94360Z4](https://hackintosher.taobao.com) |

### 台式机其它机型

| 机型名称                         | 发布地址                                                     | 教程地址                                                     | 备注             |
| -------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------- |
| ACER Veriton D430                | [链接](https://github.com/SummerEmber/ACER-Veriton-D430)     |                                                              |                  |
| 华南金牌 B75                     | [链接](https://github.com/ic005k/HUANAN-B75) [链接](https://github.com/LeUKi/Hackintosh-EFI-huanan_B75) |                                                              | e3-1230-v2 RX460 |
| Huanan X79 E5-2670, GTX650       | [链接](https://github.com/cheneyveron/clover-x79-e5-2670-gtx650) | [链接](https://github.com/cheneyveron/clover-x79-e5-2670-gtx650/blob/master/README.md) | 华南 x79 V2      |
| Huananzhi x99 f8                 | [链接](https://github.com/oscaroum/huananzhi_x99_f8)         |                                                              |                  |
| 华南X99TF | [链接](https://github.com/KGDJudy/HUANNA-X99TF-OC-9.1-EFI) | | |
| 华南B85-ITX 黑苹果                 | [链接](https://github.com/Mustang-Sun/HUANANZHI-B85-ITX-Hackintosh) |                                                              | i5-4690+16G、无独显、未安装wifi，声卡正常  |
| Ant Country X79 Basic            | [链接](https://github.com/m1qnet/X79-Hackintosh-Catalina)    |                                                              |                  |
| Supermicro x8dai                 |                                                              |                                                              | Xeon x5680       |
| X79 E5-2696-v2                   | [链接](https://github.com/cmd2001/X79-E5-2696-v2-R9-Nano-Clover-EFI) |                                                              | R9 Nano          |
| X79 X99                          | [链接](https://github.com/nguyenphucdev/OpenCore_X79_X99_Xeon_E5_2650v2) |                                                              |                  |
| X99                              | [链接](https://github.com/Cclown98/X99-OPENCORE-EFI-CATALINA-BIGSUR) |                                                              |                  |
| X99 K9 v2 Machinist | [链接](https://github.com/Andrej-Antipov/X99-K9-Machinist-Hackintosh) | | |
| PANSHI X99D4                     | [链接](https://github.com/Andywyh/PANSHI-X99-D4-OC-EFI)      |                                                              |                  |
| 七彩虹 Battle_Axe_C.B250M-HD     | [链接](https://github.com/liuoneping/Battle_Axe_C.B250M-HD-I5-7400-HD630-EFI) |                                                              |                  |
| 七彩虹 战斧C.B360M-HD 魔音版 V20 | [链接](https://github.com/swjtuhyq/colorful-b360m-efi)       |                                                              |                  |
| 七彩虹 CVN B460i                 | [链接](https://github.com/AlphaGHX/Hackintosh-CVN-b460i-efi) [链接](https://github.com/Coceki/CVN-B460i-EFI-Opencore) |                                                              |                  |
| 七彩虹 C.H110M-K D3 PRO | [链接](https://github.com/wecy-chen/C.H110M-K_D3_PRO) | | |
| Colorful CVN B760I FROZEN | [链接](https://github.com/Heming-Zhong/Colorful_CVN_B760I_FROZEN_WIFI_V20_hackintosh) | | |
| ONDA B460 SD4 | [链接](https://github.com/it1580/Hackintosh-ONDA-B460SD4-EFI) | | |
| ONDA H410 SD4                    | [链接](https://github.com/yinxianwei/ONDA-H410SD4-Hackintosh) |                                                              |                  |
| Onda P75U                        | [链接](https://github.com/hunanhjx/E3-1230v2_GTX760_OpenCore) |                                                              | E3-1230 v2       |
| Asrock Z390M ITX AC	|[1链接](https://github.com/Good0007/Asrock-Z390M-ITX-AC-Hackintosh-OC)	|		|		|
| Asus ROG STRIX B460-G GAMING	|[链接](https://github.com/JhonsonT/ROG-B460G-10400-UHD630-OPENCORE-BIGSUR)	|		|		|
| Gigabyte B460M Aorus Pro	|[链接](https://github.com/hendraanggrian/OpenCore-Gigabyte-B460M-Aorus-Pro)	|		|		|
| Gigabyte Z390 Aorus Pro	|[链接](https://github.com/blacklizard/gigabyte-z390-aorus-pro-wifi-hackintosh-opencore)	|		|		|
| ASRock B460 PG4	|[链接](https://github.com/Forne/oc-ASRock-B460-PG4)	|		|		|
| Gigabyte Z390M	|[链接](https://github.com/revunix/GIGABYTE-Z390M)	|		|		|
| MSI Pro VDH Max	|[链接](https://github.com/sileshn/Ryzentosh)	|		|		|
| Asus Strix X570-I	|[链接](https://github.com/aluveitie/RyzenMacPro)	|		|		|
| Gigabytes Z390i Pro Wifi	|[链接](https://github.com/k0Iry/opencore_z390i-pro-wifi_i7-9700k_rx580)	|		|		|
| MSI MAG B460M MORTAR|[链接](https://github.com/maemual/MSI-B460M-10700-5500XT)	|		|		|
| Gigabyte Z170X-Gaming	|[链接](https://github.com/barijaona/OpenCore_GA-Z170X-Gaming5)	|		|		|
| Asus Prime Z390A	|[链接](https://github.com/m4ary/OpenCore-Big-Sur-Asus-Prime-Z390A_i7-9700K_RX580)	|		|		|
| Gigabyte Z390 GAMING X	|[链接](https://github.com/extric99/Hackintosh-Gigabyte-Z390-GAMING-X-i9-9900k-5700XT)	|		|		|
| Asus PRIME B460I-PLUS 	|[链接](https://github.com/vulgo/prime-b460i-plus-hackintosh)	|		|		|
| MSI Prestige 15 A10SC		|[链接](https://github.com/wgjas2/MSI-Prestige-15-Hackintosh)	|		|		|
| Gigabyte B360M D3H	|[链接](https://github.com/samuelcarreira/Hackintosh-Big-Sur-Gigabyte-B360M-D3H-i3-8100-RX580-BCM943602CS-4K-monitor-OpenCore)	|		|		|
| MSI-B250M PRO-VDH-i5-7500	|[链接](https://gitee.com/akwangl/msi-b250-m-pro-vdh-i5-7500)	|		|		|
| 铭瑄B760M 终结者 D4	|[链接](https://github.com/nsinm/13400F-B760M-EFI) 	[链接](https://github.com/xiecang/Hackintosh-B760M-12490F-6600xt)	|	| 网卡推荐：[BCM94360CD](https://hackintosher.taobao.com) |
| 铭瑄 MS-B760ITX	|[链接](https://github.com/rbongIO/rbongIO-MaxSun-B760ITX-EFI)	|	|  |
| 铭瑄z790m	|[链接](https://github.com/xxy6910/13700k_z790m_EFI)	|	|	|
| MAXSUN Terminator-Z790M-D5	|[链接](https://github.com/sonojo/Terminator-Z790M-D5)	|	|	|
| 精粤B760i Snow Dream	|[链接](https://github.com/zhongjiachao/JingyueB760i-hackintosh-Opentcore-EFI)	|	|	|

## 硬件兼容列表

| 机型名称         | 发布地址                                                                         | 教程地址                                                                                        | 备注                                                       |
| ---------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **硬件兼容列表** | [链接](https://github.com/CrazyPegAsus/macOS-Mojave-Compatibility-hardware-list) |                                                                                                 | 感谢: [CrazyPegAsus](https://github.com/CrazyPegAsus)      |
| 黑苹果购买指南   | [链接](https://github.com/khronokernel/Anti-Hackintosh-Buyers-Guide)             |                                                                                                 | Hackintosh Buyers Guide                                    |
| 黑苹果安装学院   | [链接](https://github.com/huangyz0918/Hackintosh-Installer-University)           | [链接](https://github.com/huangyz0918/Hackintosh-Installer-University/blob/master/README-CN.md) | 这个和本 repo 功能类似，既然作者开放了，我们也可以收录补充 |
| 黑苹果互助项目   |                                                                                  |                                                                                                 | 和本 repo 类似                                             |

## 其它机型请提交到[这里](https://github.com/daliansky/Hackintosh)

## 感谢名单

- [Apple](https://www.apple.com/) 的 macOS
- [RehabMan](https://github.com/rehabman)维护的项目：[OS-X-Clover-Laptop-Config](https://github.com/RehabMan/OS-X-Clover-Laptop-Config) [Laptop-DSDT-Patch](https://github.com/RehabMan/Laptop-DSDT-Patch) [OS-X-USB-Inject-All](https://github.com/RehabMan/OS-X-USB-Inject-All)等
- [Acidanthera](https://github.com/acidanthera) 维护的项目：[OpenCorePkg](https://github.com/acidanthera/OpenCorePkg) [lilu](https://github.com/acidanthera/Lilu) [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup) [WhateverGreen](https://github.com/acidanthera/WhateverGreen) [VirtualSMC](https://github.com/acidanthera/VirtualSMC) [AppleALC](https://github.com/acidanthera/AppleALC) [BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM) [MaciASL](https://github.com/acidanthera/MaciASL) 等
- [headkaze](https://www.insanelymac.com/forum/profile/1364628-headkaze/) 提供的工具：[hackintool](https://github.com/headkaze/Hackintool) [PinConfigurator](https://github.com/headkaze/PinConfigurator) [BrcmPatchRAM](https://www.insanelymac.com/forum/topic/339175-brcmpatchram2-for-1015-catalina-broadcom-bluetooth-firmware-upload/)
- [CloverHackyColor](https://github.com/CloverHackyColor)维护的项目：[CloverBootloader](https://github.com/CloverHackyColor/CloverBootloader) [CloverThemes](https://github.com/CloverHackyColor/CloverThemes)
- [ic005k](https://github.com/ic005k/)维护的项目：[OpenCore Auxiliary Tools OpenCore Configurator OCAT](https://github.com/ic005k/QtOpenCoreConfig)
- 宪武整理的：[P-little](https://github.com/daliansky/P-little) [OC-little](https://github.com/daliansky/OC-little)
- [chris1111](https://github.com/chris1111)维护的项目：[VoodooHDA](https://github.com/chris1111/VoodooHDA-2.9.2-Clover-V15) [Wireless USB Adapter Clover](https://github.com/chris1111/Wireless-USB-Adapter-Clover)
- [zxystd](https://github.com/zxystd)开发的[itlwm](https://github.com/zxystd/itlwm) [IntelBluetoothFirmware](https://github.com/zxystd/IntelBluetoothFirmware)
- [lihaoyun6](https://github.com/lihaoyun6)提供的工具：[CPU-S](https://github.com/lihaoyun6/CPU-S) [macOS-Displays-icon](https://github.com/lihaoyun6/macOS-Displays-icon) [SidecarPatcher](https://github.com/lihaoyun6/SidecarPatcher)
- [xzhih](https://github.com/xzhih)提供的工具：[one-key-hidpi](https://github.com/xzhih/one-key-hidpi)
- [Bat.bat](https://github.com/williambj1)更新维护的[精解 OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)
- [athlonreg](https://github.com/athlonreg)更新维护的[OpenCore 0.5+ 部件补丁](https://blog.cloudops.ml/ocbook/) [Common-patches-for-hackintosh](https://github.com/athlonreg/Common-patches-for-hackintosh)
- [stevezhengshiqi](https://github.com/stevezhengshiqi) 更新维护的 [XiaoMi NoteBook Pro Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh) 和 [one-key-cpufriend](https://github.com/stevezhengshiqi/one-key-cpufriend)
- [Miracle-Sakuno](https://github.com/Miracle-Sakuno) 整理的各平台配置文件
- [github.com](github.com)
- [码云 gitee.io](gitee.io)
- [扣钉 coding.net](coding.net)

## 参考及引用

- https://deviwiki.com/wiki/Dell
- https://deviwiki.com/wiki/Dell_Wireless_1820A_(DW1820A)
- [Hervé](<[https://osxlatitude.com/profile/4953-herv%C3%A9/](https://osxlatitude.com/profile/4953-hervé/)>) 更新的 Broadcom 4350:https://osxlatitude.com/forums/topic/12169-bcm4350-cards-registry-of-cardslaptops-interop/
- [Hervé](<[https://osxlatitude.com/profile/4953-herv%C3%A9/](https://osxlatitude.com/profile/4953-hervé/)>) 更新的 DW1820A 支持机型列表:https://osxlatitude.com/forums/topic/11322-broadcom-bcm4350-cards-under-high-sierramojave/
- [nickhx](https://osxlatitude.com/profile/129953-nickhx/) 提供的蓝牙驱动：https://osxlatitude.com/forums/topic/11540-dw1820a-for-7490-help/?do=findComment&comment=92833
- [xjn819](https://blog.xjn819.com/)： [使用 OpenCore 引导黑苹果](https://blog.xjn819.com/?p=543) [300 系列主板正确使用 AptioMemoryFix.efi 的姿势(重写版）](https://blog.xjn819.com/?p=317)
- [insanelymac.com](https://www.insanelymac.com/)
- [tonymacx86.com](https://www.tonymacx86.com/)
- [远景论坛](http://bbs.pcbeta.com)
- [applelife.ru](https://applelife.ru/)
- [olarila.com](https://www.olarila.com/)
- [Hackintoshlifeit](https://github.com/Hackintoshlifeit)

## QQ 群列表

553283949 [黑果小兵黑苹果技术群 6](https://qm.qq.com/cgi-bin/qm/qr?k=kr_hZc5pKK4TCDRaFPwRlfAiB4528InP&jump_from=webapi) 2000 人群

630724380 [黑果小兵黑苹果技术群 7](https://qm.qq.com/cgi-bin/qm/qr?k=JyGkfKK7U3Xq3TDtpqKOTq_gW7SBg4Uh&jump_from=webapi) 2000 人群

713810838 [黑果小兵黑苹果技术群 8](https://qm.qq.com/cgi-bin/qm/qr?k=e8E-1Ge2lCoBSTlj8Y4zMxX7l7-V63Iv&jump_from=webapi) 2000 人群

688324116 [一起黑苹果](https://qm.qq.com/cgi-bin/qm/qr?k=Fp4HZ5e8A61oCu0GMS5YUqP6COc43-AO&jump_from=webapi) 2000 人群

331686786 [一起吃苹果](https://qm.qq.com/cgi-bin/qm/qr?k=No8zvDfvDicT-GfSApw1RMBI-3MQ7zM3&jump_from=webapi) 2000 人 群

257995340 [一起啃苹果](https://qm.qq.com/cgi-bin/qm/qr?k=acztqL9efoqAOoptc_3moZ9b3Sgczu9_&jump_from=webapi) 2000 人群 远景报备群

875482673 [黑果小兵黑苹果技术群](https://qm.qq.com/cgi-bin/qm/qr?k=aZNyoRum_er2mruqmnbX_93ncHNgsyak&jump_from=webapi) 2000 人群 已满员

1058822256 [黑果小兵黑苹果技术群 2](https://qm.qq.com/cgi-bin/qm/qr?k=1sIT0BDaejgr9t1Hlw16cMnw_Z96zleV&jump_from=webapi) 2000 人群 已满员

819662911 [黑果小兵黑苹果技术群 3](https://qm.qq.com/cgi-bin/qm/qr?k=aJx9xO7vAmyslCuOdK0bRMmDLpvOCeRw&jump_from=webapi) 2000 人群

954098809 [黑果小兵黑苹果技术群 4](https://qm.qq.com/cgi-bin/qm/qr?k=iu042k0X5snr--dzAxOzcsvD9Zft9yx7&jump_from=webapi) 2000 人群

1161377948 [黑果小兵黑苹果技术群 5](https://qm.qq.com/cgi-bin/qm/qr?k=kBV9vCnz-NqtXXJiwnUhaLyJN1D7G0n6&jump_from=webapi) 2000 人群

701278330 [黑苹果无线网卡交流群](https://qm.qq.com/cgi-bin/qm/qr?k=x57TlUmxz88oXGDWjMOOsWokYi8klE11&jump_from=webapi) 1000 人群 DW1820A 技术支持群

891434070 [Catalina 黑苹果交流群](https://qm.qq.com/cgi-bin/qm/qr?k=TUAxSUUtw_T1N62V0kF1sWvMcDr_eoxc&jump_from=webapi) 2000 人群 远景报备群

939122730 [Catalina 黑苹果交流 II 群](https://qm.qq.com/cgi-bin/qm/qr?k=g_rpf7m0LJllE6WHY9c0gVvCTBm1MtuN&jump_from=webapi) 2000 人群

891677227 [黑果小兵高级群](https://qm.qq.com/cgi-bin/qm/qr?k=xsuIOzF7RXYaRTTbJ5o_UjzohRDUx5UY&jump_from=webapi) 2000 人群

943307869 [黑果小兵高级群 II](https://qm.qq.com/cgi-bin/qm/qr?k=aoSvqrbysdjPo0Wa_XvvPuMG9NMEtOie&jump_from=webapi) 2000 人群

275356796 [morefine 黑苹果交流群](https://qm.qq.com/cgi-bin/qm/qr?k=H7hFwiVkZq71L7se6rz3hE9QcacqL-dV&jump_from=webapi) 500 人群 非专用机型请勿加入

869792897 [minisforum U820黑苹果交流群](https://qm.qq.com/cgi-bin/qm/qr?k=TdIS59sEdBCjbz8NbdrQ2IyPG6bMza3_&jump_from=webapi) 500 人群 非专用机型请勿加入

942112153 [天逸 510s Mini 黑苹果交流群](https://qm.qq.com/cgi-bin/qm/qr?k=N5cjw5ksrnmk-RMQ4fPCOo5D_Dxiu47B&jump_from=webapi) 1000 人群 非专用机型请勿加入

673294583 [小新 Pro 黑苹果技术群](https://qm.qq.com/cgi-bin/qm/qr?k=GgcMJM5-98yB-fc6zyGcTI3OuesrSBRk&jump_from=webapi) 2000 人群 非专用机型请勿加入

946132482 [小新 Pro 黑苹果](https://qm.qq.com/cgi-bin/qm/qr?k=r-m99xC-BPIRdVkEjU6duvqXMJ-1FOwA&jump_from=webapi) 500 人群 非专用机型请勿加入

943181023 [联想小新 Air 黑苹果交流群](https://qm.qq.com/cgi-bin/qm/qr?k=OGO_GSX9ZhtbQ_HNns57Vdxm5pR1wH6V&jump_from=webapi) 500 人群 非专用机型请勿加入

247451054 [小米 PRO 黑苹果高级群](https://qm.qq.com/cgi-bin/qm/qr?k=mnawqS-p0Djpx-B1sgjJPtMfUtVpn-2-&jump_from=webapi) 2000 人群，限小米机型

## Telegram 群

黑果小兵的部落阁 [http://t.me/daliansky](https://t.me/daliansky)
黑果小兵的部落阁 #安装问题讨论 [https://t.me/macos_installer](https://t.me/macos_installer)

其他推荐 :
安装和安装后支持小组 [https://t.me/HackintoshLife_it](https://t.me/HackintoshLife_it)

## 微信扫一扫，订阅/直达【黑果小兵的部落阁】

![WeChat](https://blog.daliansky.net/uploads/WeChatandShop.png)

## 关于打赏

如果您认可我的工作，请通过打赏支持我后续的更新

| paypal                                                                                                                             | 微信                                                                                        | 支付宝                                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| [![paypal_daliansky](https://pics.daliansky.net/d/xD0Ar91B/blog/paypal_daliansky.png?download=1)](https://www.paypal.me/daliansky) | ![wechatpay_160](https://pics.daliansky.net/d/xD0Ar91B/blog/wechatpay_160.jpg?download=1) | ![alipay_160](https://pics.daliansky.net/d/xD0Ar91B/blog/alipay_160.jpg?download=1) |

## 项目 Star 数增长趋势

[![Stargazers over time](https://starchart.cc/daliansky/Hackintosh.svg)](https://starchart.cc/daliansky/Hackintosh) 

[![img](https://img.shields.io/github/stars/daliansky/Hackintosh.svg?color=ff69b4&label=%E7%82%B9%E8%B5%9E&logoColor=ff69b4&style=social)](https://github.com/daliansky/Hackintosh) [![img](https://img.shields.io/github/followers/daliansky.svg?label=%E7%B2%89%E4%B8%9D&logoColor=success&style=social)](https://github.com/daliansky/Hackintosh) ![img](https://img.shields.io/github/contributors/daliansky/Hackintosh.svg?color=red&label=%E8%B4%A1%E7%8C%AE%E4%BA%BA%E6%95%B0) [![img](https://img.shields.io/github/last-commit/daliansky/Hackintosh.svg?color=orange&label=%E6%9C%80%E8%BF%91%E6%8F%90%E4%BA%A4)](https://github.com/daliansky/Hackintosh)
