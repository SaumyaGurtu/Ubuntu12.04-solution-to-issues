## lan connection ethernet

> cd Desktop/compat-wireless-2012-03-10-p/ <br/>
> scripts/driver-select alx <br/>
> sudo su <br/>
> make <br/>
> make install <br/>
> modprobe alx <br/>
> rfkill list <br/>

You can find 'compact-wireless-2012-03-10-p' folder in the repository.
Specifications - 32 bit, Ubuntu 12.04, Lenovo G580

## wifi connection

> lspci -nnk | grep -iA2 net <br/>
> echo "blacklist brcmwl" | sudo tee -a <br/>
> sudo apt-get install --reinstall bcmwl-kernel-source <br/>
or, <br/>
> sudo dpkg -i bcmwl-kernel-source_6.30.223.248+bdcom-0ubuntu0.0.2_i386.deb <br/>
> iwlist scan <br/>
> rfkill list <br/>

You can find 'bcmwl-kernel-source_6.30.223.248+bdcom-0ubuntu0.0.2_i386.deb' in the repository.

## grub boot repair

> sudo add-apt-repository ppa:yannubuntu/boot-repair <br/>
> ls <br/>
> vim boot.sh <br/>
> sh boot.sh <br/>
> reboot

## network configurations check

> vim /etc/network/interfaces <br/>
> /etc/init.d/networking restart <br/>
> ifconfig <br/>
> ifup eth0 <br/>
> cat /etc/issue <br/>
> /etc/init.d/network-manager restart


