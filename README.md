## 路由器固件[lede](https://github.com/coolsnowwolf/lede)(openwrt)自动编译
固件来源：[github](https://github.com/coolsnowwolf/lede)

### 编译状态
[![pipeline status](http://dev.qyh.name:800/shihuang/routerbuild/badges/master/pipeline.svg)](http://dev.qyh.name:800/shihuang/routerbuild/commits/master)

仅编译网件r7800、华硕rt-ac58u、rt-acrh17、斐讯k3的路由器固件，不接受个性化定制。

编译的固件永久保存以供挑选使用。

### 更新建议
建议不保留配置全新更新。

### 特别功能
#### 不服来跑个分？cpu跑分
使用SSH连接路由器终端，输入`/etc/coremark.sh` 稍等片刻后，访问路由器主页，概况里将显示分数，例如网件R7800的主页主机型号末尾将会显示路由器跑分` Netgear Nighthawk X4S R7800 (CpuMark : 12654.587288 Scores) ` 。

#### 隐藏功能
如果你无法看到某个神秘功能，你需要使用SSH连接输入 `echo  0xDEADBEEF > /etc/config/google_fu_mode` 回车命令后即可重新访问神秘功能，如果显示错误请清除配置信息后再试，设备无需重启。

#### 电信天翼云盘
中国电信天翼云盘提速脚本，有关token的获取可参考[这里](http://koolshare.cn/thread-159179-1-2.html)。某些地区
可能需要设置定时脚本（1小时重启）`0  */1  *  *  * /etc/init.d/familycloud restart`。

### 固件下载
#### 最新固件下载
华硕rt-ac58u：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_ac58u)

华硕rt-acrh17：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_acrh17)

网件r7800：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_r7800)

斐讯k3：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_k3)

#### 本地下载
[点此访问](http://dev.qyh.name:800/shihuang/routerbuild/pipelines)

- 请注意：你需要点击右侧的`download`按钮进行下载，或者点击`passed`状态按钮，然后在右侧点击`browse`按钮选择你需要的文件进行下载。

### 固件首次安装方式/刷机/救砖介绍
斐讯K3：https://post.smzdm.com/p/607853/

### 固件特殊命令
#### R7800
修改cpu调节器（仅限openwrt18.x）：

https://forum.openwrt.org/t/r7800-performance/15780/ 

```
echo 35 > /sys/devices/system/cpu/cpufreq/ondemand/up_threshold
echo 10 > /sys/devices/system/cpu/cpufreq/ondemand/sampling_down_factor
```

