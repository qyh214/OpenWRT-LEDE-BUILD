## 路由器固件[lede](https://github.com/coolsnowwolf/lede)(openwrt)自动编译
固件来源：[github](https://github.com/coolsnowwolf/lede)

--------------
* [编译状态](#编译状态)
* [更新建议](#更新建议)
* [特别功能](#特别功能)
* [固件下载](#固件下载)
* [已知问题](#已知问题)
--------------

### 编译状态
[![pipeline status](http://dev.qyh.name:800/shihuang/routerbuild/badges/master/pipeline.svg)](http://dev.qyh.name:800/shihuang/routerbuild/commits/master)

仅编译网件r7800、华硕rt-ac58u、rt-acrh17、斐讯k3的路由器固件，原则上不接受个性化定制，下游仓库若需使用共享的CI定制化必须遵守相关约定，否则请使用独立的CI或者建议使用github的action功能。

编译的固件最多保存6个月，如有需要请自行备份历次固件。

### 更新建议
重大版本或重大改动时，建议不保留配置全新更新。

### 特别功能

#### 不服来跑个分？cpu跑分
目前大多数机型路由器已整合跑分，自动完成跑分并显示在首页。

#### 隐藏功能
如果你无法看到某个神秘功能，你需要使用SSH连接输入 `echo  0xDEADBEEF > /etc/config/google_fu_mode`，回车，稍等片刻后即可重新访问神秘功能，如果显示错误请清除配置信息后再试，设备无需重启。

#### 温度监控
目前大多数机型路由器已整合温度监控，自动显示在首页。

### 固件下载
#### 最新固件下载
##### 建议内网用户使用
华硕rt-ac58u：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_ac58u)

华硕rt-acrh17：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_acrh17)

网件r7800：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_r7800)

斐讯k3：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_k3)

##### 建议外网用户使用

[百度网盘下载](https://pan.baidu.com/s/1J7tX4Qsu2hF_cmXrhqsogQ)(提取码：r6ds)(请注意型号，可能更新不及时)

[release页面下载](http://dev.qyh.name:800/shihuang/routerbuild/-/releases)（请注意型号，链接有效期为1天，有下载次数限制）

#### 历次固件本地下载（建议内网用户使用，外网用户可以查看百度网盘）
[点此访问](http://dev.qyh.name:800/shihuang/routerbuild/pipelines)

- 请注意：你需要点击右侧的`download`按钮进行下载，或者点击`passed`状态按钮，然后在右侧点击`browse`按钮选择你需要的文件进行下载。

### 已知问题

#### https的强制转换（自shihuang/lede@87e3eb15569a8a52af806baa5fa420ed9f85fb3b起已解决）
- 路由器内所有http被指向https这个功能可能导致使用某些服务出现异常，例如aria2的rpc通信。

自shihuang/lede@87e3eb15569a8a52af806baa5fa420ed9f85fb3b起，取消了强制https转换，之前升级上来的可能依然是https访问，
可通过SSH连接，输入`cd /etc/config/`然后`vi uhttpd`将其中的`option redirect_https '1'`改为`option redirect_https '0'`
（vi编辑器的进入编辑方式，按`i`回车进入插入模式，修改内容后，`esc`退出，然后输入`:wq`保存，更多可查阅vi相关使用说明），修改完毕保存退出后，请重启路由器生效（通常浏览器也需要清除缓存）。

你也可以通过清除配置重新刷固件重置全部数据解决此问题（通常浏览器也需要清除缓存）。

#### aria2速度问题和transmission使用（自90bd7f0e33202ad74483f421087c91b45f87d7d5起，因核心移除编译，已解决）
- 目前aria2和transmission仅在网件R7800提供进行测试，自90bd7f0e33202ad74483f421087c91b45f87d7d5暂时移除了，
可在计算机上使用迅雷等工具下载。

aria2的bt速度问题可通过添加trackerslist解决，具体可查看[这里](https://github.com/ngosang/trackerslist)。

### 固件首次安装方式/刷机/救砖介绍
- 斐讯K3：https://post.smzdm.com/p/607853/
- 华硕acrh17：官方固件-更新固件-刷入trx格式-在openwrt里-更新固件-不保留配置-刷入更新固件即可
- 网件r7800：官方固件-更新固件-刷入img格式即可

### 固件特殊命令
#### R7800
修改cpu调节器（仅限openwrt18.x，自shihuang/lede@96ff77261f98b861374011ff149df02a46abd046固件已包含此更新，无需再次操作）：

现在包含cpu调节器，你可以任意超频等操作。

https://forum.openwrt.org/t/r7800-performance/15780/ 

```
echo 35 > /sys/devices/system/cpu/cpufreq/ondemand/up_threshold
echo 10 > /sys/devices/system/cpu/cpufreq/ondemand/sampling_down_factor
```

