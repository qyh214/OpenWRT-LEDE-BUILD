## 路由器固件[lede](https://github.com/coolsnowwolf/lede)(openwrt)自动编译（小秦自用版）

固件源码：[github](https://github.com/coolsnowwolf/lede)

--------------
* [编译状态](#编译状态)
* [更新建议](#更新建议)
* [特别功能](#特别功能)
* [固件下载](#固件下载)
--------------

### 编译状态
| Github Action | Gitlab CI/CD |
| ----- | ----- |
| [![github pipeline status](https://github.com/qyh214/OpenWRT-LEDE-BUILD/actions/workflows/openwrt-ci.yml/badge.svg)](https://github.com/qyh214/OpenWRT-LEDE-BUILD/actions/workflows/openwrt-ci.yml) | [![gitlab pipeline status](http://git.qyh.name/shihuang/routerbuild/badges/master/pipeline.svg)](http://git.qyh.name/shihuang/routerbuild/commits/master) |

目前仅编译自用友善R4S的软路由固件，请注意路由器固件分区大小，不同分区大小请勿混合使用或混合升级。

- 当前内核分区：32MB
- 当前系统分区：1024MB

Gitlab：编译的固件最多保存2周，如有需要请自行备份历次固件。

Github：暂时保留全部历史编译版本。

### 更新建议
重大版本或重大改动时，建议不保留配置全新更新。如有需要建议使用烧录工具重新制作。

### 特别功能

#### cpu跑分
自动完成跑分并显示在首页。

#### 温度监控
已整合温度监控，自动显示在首页。

### 固件下载
[百度网盘下载](https://pan.baidu.com/s/1J7tX4Qsu2hF_cmXrhqsogQ)(提取码：r6ds)(请注意型号，可能更新不及时)

[gitlab release页面下载](http://git.qyh.name/shihuang/routerbuild/-/releases)（请注意型号以及外链说明）

[github release页面下载](https://github.com/qyh214/OpenWRT-LEDE-BUILD/releases)（请注意型号以及外链说明）
