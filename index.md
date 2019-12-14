## Manifold配置ROS开发环境（妙算试坑笔记）

妙算[Manifold](https://www.dji.com/cn/manifold)是大疆无人机上的机载miniPC，其中的核心板是NVIDIA的嵌入式视觉板Jetson Tegra K1。不过于2019年已经停产。由于安装妙算过程中试过很多坑，所以笔者在此记录一下安装和配环境的过程。



### （0）系统重装
1. 制作系统前需要准备:

- 系统镜像（可以使用[DJI官网上的镜像](https://dl.djicdn.com/downloads/manifold/manifold_image_v1.0.tar.gz)）
- Ubuntu 14.04 的计算机一台（可以用虚拟机但是笔者试了有些慢不推荐），一定是14.04的系统，笔者用过16.04的来制作会产生显示闪烁的问题。一定是14.04!一定是14.04!一定是14.04!重要的事情说三遍。

2.  


```markdown
Syntax highlighted code block



Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/SkyEagle8352/Manifold_ROS_Setup.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
