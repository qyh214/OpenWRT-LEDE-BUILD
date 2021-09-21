## 路由器固件[lede](https://github.com/coolsnowwolf/lede)(openwrt)自动编译
固件来源：[github](https://github.com/coolsnowwolf/lede)

--------------
* [编译状态](#编译状态)
* [更新建议](#更新建议)
* [特别功能](#特别功能)
* [固件下载](#固件下载)
--------------

### 编译状态
[![pipeline status](http://git.qyh.name/shihuang/routerbuild/badges/master/pipeline.svg)](http://git.qyh.name/shihuang/routerbuild/commits/master)

仅编译友善R4S的软路由固件，原则上不接受个性化定制，下游仓库若需使用共享的CI定制化必须遵守相关约定，否则请使用独立的CI或者建议使用github的action功能。

编译的固件最多保存6个月，如有需要请自行备份历次固件。

### 更新建议
重大版本或重大改动时，建议不保留配置全新更新。

### 特别功能

#### cpu跑分
自动完成跑分并显示在首页。

#### 隐藏功能
如果你无法看到某个神秘功能，你需要使用SSH连接输入 `echo  0xDEADBEEF > /etc/config/google_fu_mode`，回车，稍等片刻后即可重新访问神秘功能，如果显示错误请清除配置信息后再试，设备无需重启。

#### 温度监控
已整合温度监控，自动显示在首页。

### 固件下载
#### 最新固件下载
##### 建议内网用户使用
R4S：[点此下载](http://git.qyh.name/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_r4s)

##### 建议外网用户使用

[百度网盘下载](https://pan.baidu.com/s/1J7tX4Qsu2hF_cmXrhqsogQ)(提取码：r6ds)(请注意型号，可能更新不及时)

[release页面下载](http://git.qyh.name/shihuang/routerbuild/-/releases)（请注意型号，链接有效期为1天，有下载次数限制）

#### 历次固件本地下载（建议内网用户使用，外网用户可以查看百度网盘）
[点此访问](http://git.qyh.name/shihuang/routerbuild/pipelines)

- 请注意：你需要点击右侧的`download`按钮进行下载，或者点击`passed`状态按钮，然后在右侧点击`browse`按钮选择你需要的文件进行下载。
