## Linux Concepts

#### Basis Networking Command:

#### 1️⃣ ping
Test network connectivity between your system and a remote host.
```
ping google.com
```

#### 2️⃣ netstat
Shows active network connections, ports, and routing tables, and shows listening ports with associated programs.
```
netstat -tulpn
```
#### 3️⃣ ifconfig
Displays or configures network interfaces. Deprecated → use ip
```
ifconfig eth0
```

#### 4️⃣ traceroute vs tracepath
Both trace the path packets take to a destination.
```
traceroute google.com
```
```
tracepath google.com
```

#### 5️⃣ mtr
Combines ping + traceroute into real-time network path monitoring.
```
mtr google.com
```

#### 6️⃣ nslookup
DNS lookup tool – queries domain → IP mapping and vice-versa.
```
nslookup google.com
```

#### 7️⃣ telnet
Connects to a remote host over the Telnet protocol / test open ports.
```
telnet smtp.gmail.com 25
```

#### 8️⃣ hostname
Displays or sets the system hostname.
```
sudo hostname myserver
```

#### 9️⃣ ip
Modern command to manage the network and routing.
```
ip a            # Show network interfaces & IPs
ip r            # Show routing table
```

##### 🔟 iwconfig
Configures wireless network interfaces (Wi-Fi).
```
iwconfig
```

#### 11️⃣ ss
Modern replacement for netstat — shows socket statistics.
```
ss -tuln
```

#### 12️⃣ arp
Shows/modifies ARP table (IP ↔ MAC mapping).
```
arp -a
```

#### 13️⃣ dig
Advanced DNS query tool.
```
dig google.com
```

#### 15️⃣ whois
Gets domain registration information.
```
whois example.com
```

#### 16️⃣ ifplugstatus
Checks the network cable status for interfaces.
```
ifplugstatus
```

#### 17️⃣ route 
View or modify the IP routing table.
```
route -n
```
Show the routing table with numeric output.

#### 18️⃣ nmap
Powerful network scanner for security auditing and host discovery.
```
nmap 192.168.1.0/24
```

#### 19️⃣ wget 
Downloads files via HTTP, HTTPS, and FTP.
```
wget https://example.com/file.zip
```

#### 20️⃣ curl 
Fetch from API request
```
curl https://api.github.com
```

#### 21️⃣ watch
Repeats a command continuously and updates output.
```
watch df -h
```


