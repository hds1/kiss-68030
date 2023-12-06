# kiss-68030
Debian trixie/sid with kernel 6.6 fpor the retrobrew kiss-68030

1) create 3 partitions on CF-Card 1st=150M vfat, 2nd=nnnGB ext4, 3rd=50M swap
2) mount -o loop trixie_partition1.dd dir_of_your_choice
3) cp dir_of_your_choice/* to 1st partition of CF-Card
4) umount dir_of_your_choice
5) mount trixie_partition2.dd dir_of_your_choice
6) sudo cp -rav dir_of_your_choice to 2nd partition of CF-Card
7) umount dir_of_your_choice
8) Boot kiss68030 with new CF Card
9) login: root pswd: root

   Note: /sbin/init; /sbin/shutdown are taken from the old Linux image, cause debian boots and shuts down via systemctl.
   This is way too slow for the 68030 kiss system.

Download:
https://www.iup.uni-bremen.de/~schroete/trixie_partition1.dd
https://www.iup.uni-bremen.de/~schroete/trixie_partition2.dd
