## Wireshark
- Wireshark is the world’s foremost and widely-used network protocol analyzer. 
- It lets you see what’s happening on your network at a microscopic level.
- A network packet analyzer will try to capture network packets and tries to display that packet data as detailed as possible.

## How Wireshark works?

- Wireshark leverages **libpcap** on unix platforms and  **WinPcap** on Windows. This library provides an API to capture         packets.
- Wireshark put your interface in **promiscus mode**,the network interface card is configured to be in promiscuous mode which   suppresses the HW comparison of destination MAC address to the NIC's own MAC address when receiving Ethernet frames. With     this setting, the PC can see all Ethernet frames going past the NIC even if they aren't addressed to it.
  
  But this will work only in broadcast networks. In offices mostly the switch is configured

