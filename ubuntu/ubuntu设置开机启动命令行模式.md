sudo gedit /etc/default/grub

找到这一行

GRUB_CMDLINE_LINUX_DEFAULT="quiet splash" （ubuntu 12版本）或GRUB_CMDLINE_LINUX_DEFAULT="quiet "
改成

GRUB_CMDLINE_LINUX_DEFAULT="quiet splash text"  或 GRUB_CMDLINE_LINUX_DEFAULT="quiet text "

保存再输入命令：sudo update-grub  开机后就自动进入tty1了。