## lan connection ethernet

cd Desktop/compat-wireless-2012-03-10-p/
scripts/driver-select alx
sudo su
make
make install
modprobe alx
rfkill list

## wifi connection

lspci -nnk | grep -iA2 net
echo "blacklist brcmwl" | sudo tee -a
sudo apt-get install --reinstall bcmwl-kernel-source
or, sudo dpkg -i bcmwl-kernel-source_6.30.223.248+bdcom-0ubuntu0.0.2_i386.deb
iwlist scan
rfkill list

## grub boot repair

sudo add-apt-repository ppa:yannubuntu/boot-repair
ls
vim boot.sh
sh boot.sh 
reboot

## network configurations check

vim /etc/network/interfaces 
/etc/init.d/networking restart
ifconfig 
ifup eth0
cat /etc/issue
/etc/init.d/network-manager restart

