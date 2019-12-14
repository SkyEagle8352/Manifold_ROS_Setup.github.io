## Manifold配置ROS开发环境（妙算试坑笔记）

妙算[Manifold](https://www.dji.com/cn/manifold)是大疆无人机上的机载miniPC，其中的核心板是NVIDIA的嵌入式视觉板Jetson Tegra K1。不过于2019年已经停产。由于安装妙算过程中试过很多坑，所以笔者在此记录一下安装和配环境的过程。



# 系统重装
## 制作系统前需要准备:

- 系统镜像（可以使用[DJI官网上的镜像](https://dl.djicdn.com/downloads/manifold/manifold_image_v1.0.tar.gz)）
- Ubuntu 14.04 的计算机一台（可以用虚拟机但是笔者试了有些慢不推荐），一定是14.04的系统，笔者用过16.04的来制作会产生显示闪烁的问题。一定是14.04!一定是14.04!一定是14.04!重要的事情说三遍。

## 解压安装包 
 在终端下输入如下命令：

```markdown
mkdir  ~/manifold
cd ~/manifold
sudo tar -xvpzf  /manifold_image_v1.0.tar.gz
```

## 妙算进入恢复模式
参考[使用手册](https://dl.djicdn.com/downloads/manifold/20170918/Manifold_User_Manual_v1.2_CH.pdf),笔者使用的方法：
- 连接妙算和计算机 (Manifold)micro-B <-> USB(PC);
- 连接电源;
- 按住recover键不松开，再按下电源键，释放电源键后松开recover键。

在终端中输入
```markdown
lsusb
```
若出现信息中包含有如下所示的项则进入回复模式成功，否正重来。
在终端中输入
```markdown
Bus 001 Device 008: ID 0955:7740 Nvidia Corp.
```
## 制作系统镜像
同样参考[使用手册](https://dl.djicdn.com/downloads/manifold/20170918/Manifold_User_Manual_v1.2_CH.pdf)：

输入以下指令:
```markdown
cd ~/manifold/Linux_for_Tegra/bootloader
sudo ./nvflash --read APP system.img --bl ardbeg/fastboot.bin –go
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/SkyEagle8352/Manifold_ROS_Setup.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
