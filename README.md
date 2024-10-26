# JW LTG Themes

[简体中文版]("./README - zh_CN.md")

### 🎊Chuh Koi! 1st RELEASE Today🎊

(Chuh Koi: "Congratulations" in [Lenda Sarieh](https://lendasarieh.github.io))

New **GRUB** & **Plymouth** theme for Linux users, created by JW!

---

### GRUB Theme

##### Ubuntu

First, you'd better download, unzip and copy the related files to the directory called `/boot/grub/themes`.

```shell
$ tar -zxvf jw-grub-theme.tar.gz	# Unzip the file (In "Releases")
$ sudo mkdir /boot/grub/themes		# If there DOESN'T exist this directory
$ sudo cp -r jw-grub-theme /boot/grub/themes	# Copy the unzipped folder to this directory
```

Then, find and open the file `/etc/default/grub` via your editor

```shell
$ sudo nano /etc/default/grub
```

Add these lines to the file `/etc/default/grub`, then save the file:

```shell
[...]
# If there exist these lines, modify them like THESE
GRUB_THEME=/boot/grub/themes/jw-grub-theme
GRUB_GFXMODE=1920x1080
[...]
```

Afterwards, apply the change to the GRUB using command:

```shell
$ sudo update-grub
```

Normally, you should see the following output:

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

Reboot the system and you'll see the **updated** GRUB Menu like this:

![](D:\Git_2\jw-ltg-themes\Updated GRUB Menu (Sample).png)

Like it?😊

---

### Plymouth Theme

##### Ubuntu

First, you'd better download, unzip and copy the related files to the directory called `/usr/share/plymouth`

```shell
$ tar -zxvf jw-plymouth-theme.tar.gz			# Unzip the file (In "Releases")
$ cd jw-plymouth-theme
# Copy these directories here (Copy the BOTH!!!)
$ sudo cp -r jw-ltg /usr/share/plymouth/themes && sudo cp -r jw_spinner /usr/share/plymouth/themes
```

Then, enable the theme using the following commands:

```Shell
$ sudo ln -sf /usr/share/plymouth/themes/jw-ltg/jw-ltg.plymouth /usr/share/plymouth/themes/default.plymouth
$ sudo update-initramfs -u	# Update the initramfs to apply the change
```

Normally, reboot the system and you'll see the **updated** Plymouth animation like this:

###### Normal (e.g. VirtualBox)

![](D:\Git_2\jw-ltg-themes\Updated Plymouth Animation (Sample).png)

###### Fallback (e.g VMware Workstation Pro)

![](D:\Git_2\jw-ltg-themes\Updated Plymouth Animation (Sample Fallback).png)

Like it?😊

---

### Custom

Change to your style? No problem!

###### Text (GRUB Menu)

jw-ltg-themes/**theme.txt**

```shell
# Main options
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

# Boot menu
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


# Countdown label
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

###### Images (GRUB/Plymouth)

Just copy certain images to the relative directories, and rename to the **BOLDER** filenames.

jw-ltg-themes/**background.png** (1920x1080 resolution images are recommended)

![](D:\Git_2\jw-ltg-themes\jw-grub-theme\background.png)

jw_spinner/**bgrt-fallback.png**

<img src="D:\Git_2\jw-ltg-themes\jw-plymouth-theme\jw_spinner\bgrt-fallback.png"  style="float:left" />

jw_spinner/**watermark.png**

<img src="D:\Git_2\jw-ltg-themes\jw-plymouth-theme\jw_spinner\watermark.png" style="float:left" />

---

### Contact Me

If there's any problem with the content above, just send a feedback!

E-mail: jack201806@outlook.com

QQ (Personal): 1625351963

QQ Group: [518075828](https://qm.qq.com/q/ZRfSu4nwMo )

Weixin: srhskah

