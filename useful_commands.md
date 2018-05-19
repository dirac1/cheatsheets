Useful Commands & one liners for Unix systems
================================================

* $expac '%m\t%n' | sort -h	 Sort package size in Archlinux

* #pacman -R $(pacman -Qdtq) 	 Delete unneeded packages

* #ncdu /			 Check filesystem HDD storage status 

* $sudo systemd-analyze verify foobar.service	Check .service file syntax

* #dd bs=4M if=/path/to/archlinux.iso of=/dev/sdx status=progress oflag=sync usb flash installation	
