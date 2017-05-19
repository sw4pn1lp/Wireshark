## [Wireshark](https://www.wireshark.org/)
- Wireshark is the world’s foremost and widely-used network protocol analyzer. 
- It lets you see what’s happening on your network at a microscopic level.
- A network packet analyzer will try to capture network packets and tries to display that packet data as detailed as possible.

## How Wireshark works?

- Wireshark leverages **libpcap** on unix platforms and  **WinPcap** on Windows. This library provides an API to capture packets.
- Wireshark put your interface in **promiscuous mode**, the network interface card (NIC) is configured to be in promiscuous mode which         suppresses the HW comparison of destination MAC address to the NIC's own MAC address when receiving Ethernet frames. With this setting,   the PC can see all Ethernet frames going past the NIC even if they aren't addressed to it.
  But this will work only in broadcast networks. In offices mostly the switch is configured in way that they only allow the packets         intended for the mentioned MAC address.
  
## Installation of Wireshark.
You an Download wireshark at free of cost for [Mac](https://2.na.dl.wireshark.org/osx/Wireshark%202.2.6%20Intel%2064.dmg), [Windows](https://2.na.dl.wireshark.org/win32/Wireshark-win32-2.2.6.exe), Linux.
Download Wireshark setup and Install it on your system.
Lets start Wireshark 101.



