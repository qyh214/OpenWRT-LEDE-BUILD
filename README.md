## 路由器固件[lede](https://github.com/coolsnowwolf/lede)(openwrt)自动编译
固件来源：[github](https://github.com/coolsnowwolf/lede)

### 编译状态
[![pipeline status](http://dev.qyh.name:800/shihuang/routerbuild/badges/master/pipeline.svg)](http://dev.qyh.name:800/shihuang/routerbuild/commits/master)

仅编译网件r7800、华硕rt-ac58u、rt-acrh17的路由器固件，不接受个性化定制。

编译的固件永久保存以供挑选使用。

### 更新建议
建议不保留配置全新更新。

### 特殊代码
如果你无法看到某个神秘功能，你需要使用SSH连接输入 `echo  0xDEADBEEF > /etc/config/google_fu_mode` 回车命令后即可重新访问神秘功能，如果显示错误请清除配置信息后再试，设备无需重启。

### 固件下载

#### 最新固件下载

华硕rt-ac58u：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_ac58u)

华硕rt-acrh17：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_acrh17)

网件r7800：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_r7800)

本地下载：[点此访问](http://dev.qyh.name:800/shihuang/routerbuild/pipelines)
- 请注意：你需要点击右侧的`download`按钮进行下载，或者点击`passed`状态按钮，然后在右侧点击`browse`按钮选择你需要的文件进行下载。
