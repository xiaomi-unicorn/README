### 内核相关信息收集
1. GKI KMI 更方便刷机,也更麻烦

### 小米开源代码
1. https://github.com/MiCode/Xiaomi_Kernel_OpenSource 分支 mayfly-s-oss,分支说明是12S的,但里面有12SPRO的配置vendor/unicorn_GKI.config
2. https://github.com/Mandi-Sa/micode-mayfly-s-oss 两个仓库代码不一样,这个仓库代码时间更早，代码也相对多一点

### 高通开源代码分支
1. https://git.codelinaro.org/clo/la/kernel/msm-5.10 提交记录 154370a6e15b39c564691e60c08c7f698457c2ab 比小米开源代码少一个提交记录
2. 对应tags是KERNEL.PLATFORM.1.0.r1-09000-WAIPIO.0
3. 对应分支猜测曾经是 kernel.lnx.5.10.r1-rel 已经多了很多提交记录了

### 谷歌代码 5.10.81
1. https://android.googlesource.com/kernel/common 分支deprecated/android12-5.10-2022-03
2. 镜像地址 https://mirrors.tuna.tsinghua.edu.cn/git/AOSP/kernel/common

### KernelSU
1. https://github.com/tiann/KernelSU
2. 使用谷歌代码分支(deprecated/android12-5.10-2022-03)编译,仅加入KernelSU部分代码,无其他修改
3. 当前最新版: https://github.com/tiann/KernelSU/releases/download/v0.6.7/AnyKernel3-android12-5.10.81_2022-03.zip
4. twrp下刷入即可,已测试可用,即验证可以直接用谷歌的代码分支启动MIUI,暂时没有发现功能问题
5. KernelSU需配合其管理程序一起使用 https://github.com/tiann/KernelSU/releases/download/v0.6.7/KernelSU_v0.6.7_11210-release.apk

### 猜想
1. 谷歌原版分支可以启动MIUI,可否直接用谷歌的分支做第三方系统适配
2. 可否拿谷歌的分支直接做Halium适配