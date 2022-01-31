## Arguments :

Scan : 

- `-PE` : Scan using ICMP Echo
- `-PM` : Scan using ICMP Address Mask
- `-PP` : Scan using ICMP Timestamp
- `-PR` : Scan using ARP
- `-sn`
- `-PS` : Scan TCP port using SYN packet. Default : Port 80. Ex : `-PS21-25`, `-PS80,443,8080`
- `-PA` : Scan using TCP ACK Ping
- `-sU` : UDP Scan
- `-sN` : Null Scan
- `-sF` : FIN Flag Scan
- `-sX` : XMas Scan. Send FIN, PSH, and URG flags
- `-sI <ZOMBIE_IP>`  : make requests from an idl machine

Others : 

- `-n` : no DNS lookup
- `-R` : reverse-DNS lookup for all hosts
- `-sn` : host discovery only
- `-F` : Scan only 100 most used port
- `T<0-5>` : set the speed of the scan. T0 slowest
- `-S <SPOFFED_IP>`  : Spoof IP
- `-f` : fragment packet
- `--reason` : explication of the results
- `-v` : verbose output
- `-vv` : even more verbose
- `-d` and `-dd` : for debug
- `-oN` : save file, normal
- `-oG` : save file, grepable
- `-oX` : save file, XML

Vuln : 

- `-sV` : Service and version information
- `-O` : OS detection
- `-sC`
- `-script <SCRIPT-NAME>` : start a script

Other tools 

masscan