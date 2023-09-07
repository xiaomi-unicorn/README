### TWRP相关信息
1. 原帖地址: https://forum.xda-developers.com/t/shared-twrp-by-skkk.4479573/
2. 下载地址1: https://sourceforge.net/projects/recovery-for-xiaomi-devices/files/unicorn/ 
3. 下载地址2: https://mega.nz/folder/7g0EUAxK#HYD-Wl65HCYKa8PiwSsLKQ

### 注意事项
1. skkk大佬给的包分两种,可以直接启动的、需刷入分区再启动的
2. 不能直接刷'recovery'分区,别问为什么,变过砖.正确分区名'recovery_a'、'recovery_b'、'recovery_ab',分别对应第一个recovery分区、第二个recovery分区、两个recovery分区都刷
```
# 直接启动，要用可以直接启动的才可以，否则会失败，但不会砖
fastboot boot twrp.img

# 直接变砖，正在的分区名不是recovery
fastboot flash recovery twrp.img

# 刷到第一个recovery分区
fastboot flash recovery_a twrp.img

# 刷到第二个recovery分区
fastboot flash recovery_b twrp.img

# 两个recovery分区都刷，最直接，建议这样
fastboot flash recovery_ab twrp.img
```