# Filters in Wireshark
Wireshark Provides two type of Filtering 
 
 1.Filtering while Capturing
 
 2.Filtering while Displaying

### Capture Filters
Some of the example 

1.Capture only traffic to or from IP address
```
host 192.168.56.101
```
2.Capture traffic to or from a range of IP addresses:
```
net 192.168.0.0/24
or
net 192.168.0.0 mask 255.255.255.0
```
3.Capture traffic from a range of IP addresses:
```
src net 192.168.0.0/24
or
src net 192.168.0.0 mask 255.255.255.0
```
4.Capture traffic to a range of IP addresses:
```
dst net 192.168.0.0/24
or
dst net 192.168.0.0 mask 255.255.255.0
```
5.Capture only DNS (port 53) traffic:
```
port 53
```
6.Capture traffic within a range of ports
```
(tcp[0:2] > 1500 and tcp[0:2] < 1550) or (tcp[2:2] > 1500 and tcp[2:2] < 1550)
```
7.Capture HTTP GET requests. This looks for the bytes 'G', 'E', 'T', and ' ' (hex values 47, 45, 54, and 20) just after the TCP header. "tcp[12:1] & 0xf0) >> 2".
```
port 80 and tcp[((tcp[12:1] & 0xf0) >> 2):4] = 0x47455420
```

### Display Filters
**Some Display filters commands**
```
Equal to              "==" or "eq"
Not equal to          "!=" or "ne"
Less than             "<" or "lt"
Greater or equal      ">" or "gt"
Contains              "Contains"
Slicing               "[]"
```

1. Search for traffic from specific IP
```
ip.addr == 192.168.56.101
```
2. Show only traffic in the LAN (192.168.x.x), between workstations and servers -- no Internet:
```
ip.src==192.168.0.0/16 and ip.dst==192.168.0.0/16
```
3. Show only specific traffic
```
tcp.port eq 25 or icmp
```
4. Tcp flags
```
tcp.flags.syn == 1
```
5. Match HTTP requests where the last characters in the uri are the characters "id=1":
```
  http.request.uri matches "id="
```
6. Check the contents of DNS Response
```
dns.resp.name contains "google"
```

[Capturing of Packets](capack.md)   | [Advanced Wireshark](advwire.md)
