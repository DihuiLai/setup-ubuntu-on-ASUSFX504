# Setup-ubuntu-on-ASUSFX504



## resolve reboot problem
The reboot problem will be resolved by installling nvidia driver and change the grub file

first get the PPA repository driver

``` sudo add-apt-repository ppa:graphics-drivers/ppa```

# install nvidia driver 

``` sudo apt install nvidia-384 nvidia-384-dev```

```sudo nano /etc/default/grub```

Edit 

```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash reboot=pci"```

Update grub 

``` sudo update-grub```

Restart ubuntu and sudo reboot should run normal now. 

## mount disk space automatically 
` ls -al /dev/disk/by-uuid/`

`sudo nano /etc/fstab`

adding the following lines to the fstab

` #data drive`

`UUID=27d4988e-250c-428f-9a80-f25e2f1cec39 /media/dihui/data ext4 defaults       0       0`

## GPU-support tensorflow
https://gist.github.com/Mahedi-61/2a2f1579d4271717d421065168ce6a73

## resovlve touchpad and kernal update
kernal update causes other issues
https://linuxhint.com/upgrade-kernel-ubuntu-1804/
