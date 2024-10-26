# JW LTG Themes

### 🎊Chuh Koi! 1st RELEASE Today🎊

[^Chuh Koi]: "Congratulations" in Lenda Sarieh

New **GRUB** & **Plymouth** theme for Linux users, created by JW!

### GRUB Theme

##### Ubuntu

First, you'd better download, unzip and copy the file to the directory called `/boot/grub/themes`.

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

### Plymouth Theme

##### Ubuntu

First, you'd better download, unzip and copy the file to the directory called `/usr/share/plymouth`

```shell
$ tar -zxvf jw-plymouth-theme.tar.gz			# Unzip the file (In "Releases")
$ cd jw-plymouth-theme
# Copy these directories here 
$ sudo cp -r jw-ltg /usr/share/plymouth/themes && sudo cp -r jw_spinner /usr/share/plymouth/themes
```

Then, enable the theme using the following commands:

```Shell
$ sudo ln -sf /usr/share/plymouth/themes/jw-ltg/jw-ltg.plymouth /usr/share/plymouth/themes/default.plymouth
$ sudo update-initramfs -u	# Update the initramfs and enable this theme
```

Normally, reboot the system and you'll see the **updated** Plymouth animation like this:

###### Normal (e.g. VirtualBox)

![](D:\Git_2\jw-ltg-themes\Updated Plymouth Animation (Sample).png)

###### Fallback (e.g VMware Workstation Pro)

![](D:\Git_2\jw-ltg-themes\Updated Plymouth Animation (Sample Fallback).png)

Like it?😊

### Contact Me

E-mail: jack201806@outlook.com

QQ (Personal): 1625351963

QQ Group: [518075828](https://qm.qq.com/q/ZRfSu4nwMo )

Weixin: srhskah

