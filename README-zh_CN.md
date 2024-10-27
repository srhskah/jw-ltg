# JW LTG主题

[English ver.](./README.md)

### 🎊Chuh Koi! 今日首次RELEASE🎊

（Chuh Koi：[白菜语](https://lendasarieh.github.io)的“祝贺，恭喜”）

JW制作，为Linux用户打造的全新的**GRUB**和**Plymouth**主题，正！式！上！线！啦！

----

### GRUB主题

##### Ubuntu

首先，下载、解压并复制有关文件到`/boot/grub/themes`目录。

```shell
$ tar -zxvf jw-grub-theme.tar.gz	# 解压这个文件（在“Releases”里）
$ sudo mkdir /boot/grub/themes		# 如果不存在该目录，创建它
$ sudo cp -r jw-grub-theme /boot/grub/themes	# 将解压后的文件夹复制到该目录
```

然后，找到并用文本编辑器打开这个文件`/etc/default/grub`。

```shell
$ sudo nano /etc/default/grub
```

在`/etc/default/grub`里添加以下几行，并保存文件：

```shell
[...]
# 如果已有这几行，改成这样
GRUB_THEME=/boot/grub/themes/jw-grub-theme/theme.txt
GRUB_GFXMODE=1920x1080
[...]
```

接下来，执行这条命令，使更改生效：

```shell
$ sudo update-grub
```

正常情况下，您将会看到以下输出：

```shell
Sourcing file `/etc/default/grub'
Sourcing file `/etc/default/grub.d/init-select.cfg'
Generating grub configuration file ...
Found theme: /boot/grub/themes/descent/theme.txt
Found linux image: /boot/vmlinuz-5.15.0-41-generic
Found initrd image: /boot/initrd.img-5.15.0-41-generic
Found linux image: /boot/vmlinuz-5.15.0-39-generic
Found initrd image: /boot/initrd.img-5.15.0-39-generic
Found memtest86+ image: /boot/memtest86+.elf
Found memtest86+ image: /boot/memtest86+.bin
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
done
```

重启电脑后，您将看到**更新后**的GRUB菜单（如下图）：

<img src=".\Updated GRUB Menu (Sample).png" />

喜欢吗？😊

---

### Plymouth主题

##### Ubuntu

首先，下载、解压并复制有关文件到`/boot/grub/themes`目录。

```shell
$ tar -zxvf jw-plymouth-theme.tar.gz			# 解压这个文件（在“Releases”里）
$ cd jw-plymouth-theme
# 将这些文件夹复制到/boot/grub/themes目录（两个都要复制哦）
$ sudo cp -r jw-ltg /usr/share/plymouth/themes && sudo cp -r jw_spinner /usr/share/plymouth/themes
```

然后，执行以下命令以启用该主题：

```Shell
$ sudo ln -sf /usr/share/plymouth/themes/jw-ltg/jw-ltg.plymouth /usr/share/plymouth/themes/default.plymouth
$ sudo update-initramfs -u	# 更新initramfs以使更改生效
```

正常情况下，重启电脑，您将看到**更新后**的Plymouth动画（如下图）：

###### 正常（以VirtualBox为例）

<img src=".\Updated Plymouth Animation (Sample).png" />

###### Fallback（以VMware Workstation Pro为例）

<img src=".\Updated Plymouth Animation (Sample Fallback).png" />

喜欢吗？😊

---

### 自定义

想换成自己喜欢的样式？没问题！

###### 文字（GRUB菜单）

jw-ltg-themes/**theme.txt**

```shell
# 主要选项
title-text: ""
desktop-image: "background.png"
desktop-color: "#000000"
#terminal-font: "Terminus Regular 14"
terminal-font: "Ubuntu Regular 14"
terminal-box: "terminal_box_*.png"
terminal-left: "0"
terminal-top: "0"
terminal-width: "100%"
terminal-height: "100%"
terminal-border: "0"

# 启动菜单
+ boot_menu {
  left = 15%
  top = 40%
  width = 55%
  height = 65%
  item_font = "Ubuntu Regular 20"
  item_color = "#2c90c0"
  selected_item_color = "#90c02c"
  icon_width = 36
  icon_height = 36
  item_icon_space = 20
  item_height = 40
  item_padding = 2
  item_spacing = 10
  selected_item_pixmap_style = "select_*.png"
}

# 倒计时标签
# You can change the name of default starting OS here
+ label {
  left = 15%
  top = 31%
  align = "center"
  id = "__timeout__"
  text = "Selected OS will start in %d seconds"
  color = "#2c90c0"
  font = "Ubuntu Regular 17"
}
```

###### 图片（GRUB/Plymouth）

将指定的图片复制到相应的目录，重命名为**加粗的**文件名即可

jw-ltg-themes/**background.png**（推荐使用分辨率1920x1080的图片）

<img src=".\jw-grub-theme\background.png" />

jw_spinner/**bgrt-fallback.png**

<img src=".\jw-plymouth-theme\jw_spinner\bgrt-fallback.png"  style="float:left" />

jw_spinner/**watermark.png**

<img src=".\jw-plymouth-theme\jw_spinner\watermark.png" style="float:left" />

---

### 联系我

如果就上述内容有任何问题，请速向本人反馈！

电子邮箱: jack201806@outlook.com

本人QQ号: 1625351963

QQ群: [518075828](https://qm.qq.com/q/ZRfSu4nwMo )

本人微信号: srhskah

