## 路由器固件[lede](https://github.com/coolsnowwolf/lede)(openwrt)自动编译
固件来源：[github](https://github.com/coolsnowwolf/lede)

### 编译状态
[![pipeline status](http://dev.qyh.name:800/shihuang/routerbuild/badges/master/pipeline.svg)](http://dev.qyh.name:800/shihuang/routerbuild/commits/master)

仅编译网件r7800、华硕rt-ac58u、rt-acrh17的路由器固件，不接受个性化定制。

由于[固件上游支持](https://github.com/coolsnowwolf/lede)关闭停止支持，之后版本无法保证可用，敬请谅解，此版本起
固件永久保存以供备用。

自动在每周周二0点（CST）进行编译打包。服务器上的构建文件保留2周（自该文件编译成功日起，有需要的请提前做好备份）。

### 更新建议
当内核大版本更新时（例如从R7.6升级到R7.7），建议不保留配置文件更新，大版本更新一般
伴随不稳定，CI可能因配置文件问题导致错误，需要等待一段时间改进配置文件进行CI测试。

小版本更新（git的sha更新，以及R7.6升级到R7.6.1）一般可保留配置文件更新。

### 提交bug
路由器固件的问题请在[github](https://github.com/coolsnowwolf/lede)的issue处提交。

因为CI、配置文件陈旧导致的问题请在这里的issue处提交。

### 固件下载

#### 最新固件下载

华硕rt-ac58u：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_ac58u)

华硕rt-acrh17：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_acrh17)

网件r7800：[点此下载](http://dev.qyh.name:800/shihuang/routerbuild/-/jobs/artifacts/master/download?job=job_r7800)

百度网盘（可能不是最新的）：[点此访问](https://pan.baidu.com/s/1qXLGhVA)  密码:tunc

本地下载：[点此访问](http://dev.qyh.name:800/shihuang/routerbuild/pipelines)
- 请注意：你需要点击右侧的`download`按钮进行下载，或者点击`passed`状态按钮，然后在右侧点击`browse`按钮选择你需要的文件进行下载。
