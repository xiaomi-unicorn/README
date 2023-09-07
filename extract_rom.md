### 官方包解包提取
1. 有多个工具可以解包

### 线刷包解包工具,解 super.img
1. simg2img + lpunpack ,simg2img直接安装，lpunpack 是安装源码里的，[网友编译好的](https://blog.csdn.net/u012045061/article/details/119383397)
2. xda帖子里提到的imjtool，[源贴地址](https://forum.xda-developers.com/t/editing-system-img-inside-super-img-and-flashing-our-modifications.4196625/)，[工具说明页](https://newandroidbook.com/tools/imjtool.html)，[下载地址](http://newandroidbook.com/tools/imjtool.tgz)

### 卡刷包解包工具,解 payload.bin
1. 卡刷包解包工具用LineageOS的 https://github.com/LineageOS/scripts/tree/master/update-payload-extractor
2. https://github.com/kholia/payload_dumper

### 接线刷包建议用imjtool
```
# 这步用simg2img  也一样，都是 simg -> img
./imjtool.ELF64 super.img extract
# 在extracted里面下得到一堆img
./imjtool.ELF64 extracted/image.img extract
```

### 挂载
```
# ext4或者不指定文件系统格式将得到一个错误信息
sudo mount -t ext4 -o ro,loop system_a.img /mnt/
mount: /mnt: wrong fs type, bad option, bad superblock on /dev/loop0, missing codepage or helper program, or other error.
# 这个才是正确的，imjtool工具会提示文件系统格式，lpunpack暂时不提示
sudo mount -t erofs -o ro,loop system_a.img /mnt/
```