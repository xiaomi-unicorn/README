### Dynamic System Updates (DSU) 动态系统更新
1. DSU 可以刷很多GSI包
2. 不影响原系统就可以玩其他系统
3. 谷歌介绍页面 https://source.android.google.cn/docs/core/ota/dynamic-system-updates?hl=zh-cn

### 推荐使用 DSU-Sideloader
1. https://github.com/VegaBobo/DSU-Sideloader
2. 当前版本下载 https://github.com/VegaBobo/DSU-Sideloader/releases/download/2.03/app-release.apk
3. 推荐使用KernelSU给DSU-Sideloader分root权限操作

### GSI资源
1. DSU-Sideloader 项目页有给出相关资源地址
2. 第三方GSI包 https://github.com/phhusson/treble_experimentations/wiki/Generic-System-Image-%28GSI%29-list
3. 谷歌GSI包,可能访问不了 https://developer.android.com/topic/generic-system-image/releases

### Generic System Images (GSI) 通用系统映像
1. 谷歌介绍页面 https://developer.android.google.cn/topic/generic-system-image?hl=zh_cn
2. 包含 GMS 的 Android GSI https://developer.android.google.cn/topic/generic-system-image/releases?hl=zh-cn
3. 不含 GMS 的 https://ci.android.com/builds/branches/aosp-android12-gsi/grid?hl=zh-cn

### 测试记录，欢迎补充

#### LineageOS 19.1
  1. 下载地址： https://sourceforge.net/projects/andyyan-gsi/files/lineage-19.x/
  2. 使用包 lineage-19.1-20230715-UNOFFICIAL-arm64_bvS.img.xz
  3. 第一次进系统 状态栏和下方虚拟按键显示不全，状态栏不响应下拉事件
  4. 第二次进系统 状态栏和下方虚拟按键显示正常，操作事件响应正常
  5. 扬声器破音，消息提示音破音
  6. 通话、短信、照相 应用正常

#### AlphaDroid Android 13
  1. 第一次进系统 界面显示和操作有问题
  2. 第二次进系统 界面显示和操作正常
  3. 扬声器破音，消息提示音破音