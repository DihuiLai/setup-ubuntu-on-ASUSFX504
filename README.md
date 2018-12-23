# Setup-ubuntu-on-ASUSFX504
## resolve reboot problem

`sudo nano /etc/default/grub`

` sudo update-grub

## mount disk space automatically 
` ls -al /dev/disk/by-uuid/`

`sudo nano /etc/fstab`

adding the following lines to the fstab

` #data drive`

`UUID=27d4988e-250c-428f-9a80-f25e2f1cec39 /media/dihui/data ext4 defaults       0       0`
