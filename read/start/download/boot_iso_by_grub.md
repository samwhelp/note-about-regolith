---
title: Boot ISO By GRUB
nav_order: 7040
has_children: false
parent: 下載
grand_parent: 入門
---


# Boot ISO By GRUB

## 範例

| GRUB Boot ISO 範例 | 設定檔路徑 | 是否需要執行 update-grub |
| --- | --- | --- |
| demo_40_custom / latest | /etc/grub.d/40_custom | 修改後，需要執行 `sudo update-grub` |
| demo_41_custom / [latest](https://github.com/samwhelp/note-about-grub/tree/gh-pages/_demo/prototype/boot_iso/demo_41_custom/RegolithLinux/latest) | [/boot/grub/custom.cfg](https://github.com/samwhelp/note-about-grub/blob/gh-pages/_demo/prototype/boot_iso/demo_41_custom/RegolithLinux/latest/custom.cfg) | 修改後，**不需要**執行 `sudo update-grub` |


## GRUB Menu Entry / Boot ISO 樣板

``` sh
menuentry "Regolith 1.6.0_focal ISO" --class Ubuntu {
	set iso_file="/opt/iso/regolith/latest/Regolith_1.6.0_focal"
	search --set=iso_partition --no-floppy --file $iso_file
	probe --set=iso_partition_uuid --fs-uuid $iso_partition
	set img_dev="/dev/disk/by-uuid/$iso_partition_uuid"
	loopback loop ($iso_partition)$iso_file
	set boot_option=""
	#set boot_option="locale=zh_TW"
	#set boot_option="quiet splash"
	linux (loop)/casper/vmlinuz boot=casper iso-scan/filename=$iso_file $boot_option
	initrd (loop)/casper/initrd
}
```


## See Also

* Grub 探索筆記 / [GRUB Boot ISO 範例](https://samwhelp.github.io/note-about-grub/read/howto/boot_iso.html)
