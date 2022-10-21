# MTK core temperature unlocking service

## Changelog  

### 增强模块 微型版v7更新：
1.新增，新增一个温度检测阈值控制，到达135触发powersave模式。

2.新增，一些温控阈值的分uperf版本的调整，比如v3版本在温度高于120度时会调整为fast模式v2版本则会调整为performance模式。

3.新增，支持在magisk里在线更新。

4.新增，在系统启动后60秒内重启会自动禁用模块。

5.调整，默认配置调整，将原来的高温保护阈值从原来的115℃触发balance模式提高到120℃触发v2版本的performance模式；v3版本的fast模式，将原来的120℃触发powersave模式提高到130℃触发balance模式。

6.调整，将不再对module.prop注入，会单独创建一个module.prop，但核心服务程序仍然在uperf文件夹内部，所以禁用uperf那么核心服务不会启用，如果在magisk里禁用“增强模块”那么在uperf里的服务会检测magisk留下的flag，也不会启动。

7.修复，再次修复“有小概率会错误的检测到“系统不支持”然后服务暴毙的bug”。

## Historical Changelog

### 增强模块 微型版v6更新：
1.新增，用户温控检测配置调整文件，可以在/sdcard/Android/MTK-Enhance/cfg_enhance.prop调整温度检测的阈值。

2.新增，检测uperf或gpuadj启动后马上启动，而不是硬等待，加快启动速度。

3.新增，检测uperf是v2还是v3，如果是v2那么触发高温保护后回复到fast模式，如果是v3那么回复到performance模式。

4.调整，默认配置调整，将原来的高温保护阈值从原来的110℃触发balance模式提高到115℃触发balance模式，将原来的115℃触发powersave模式提高到120℃触发powersave模式。

5.调整，将log从/sdcard/Android/MTK-Enhance.log移动到/sdcard/Android/MTK-Enhance/MTK-Enhance.log。

6.修复，有小概率会错误的检测到“系统不支持”然后服务暴毙的bug。

### 增强模块 微型版v5更新：
1.新增实时检测CPU核心温度，到达115度会将uperf切换到balance模式，到达120度会将uperf切换到powersave模式，降温到105度切换到fast模式。

2.增加机型验证，阻止高通机型安装。

3.一大堆已知问题修复。

### 增强模块 微型版 v4更新：
1.解决新版hamjin调度注入后的异常耗电问题。

2.再次压缩压缩包体积。

3.许多已知问题修复。

### 增强模块 微型版 v3更新：
1.可以查看log是否在运行，位置在/storage/emulated/0/Android/MTK-Enhance.log。

2.可以在uperf升级(安装后未重启)时注入。

3.帮hamjin修复新版动态调频(gpu_adjustment)不生效。

4.压缩二进制文件，让整个模块压缩包更小！

5.已知问题修复。

### 增强模块 微型版 v2更新：
1.已知问题修复。
2.适配hamjin220926000版本。
