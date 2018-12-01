# Ping-scan

## rules
```
alert icmp any any -> any any (msg:"ICMP PING NMAP"; dsize:0; itype:8; reference:arachnids,162; classtype:attempted-recon; sid:469; rev:3;)
alert tcp any any -> any any (msg:"Nmap NULL Scan"; flags:0; sid:1000009; rev:1; )
alert icmp any any -> 192.168.1.105 any (msg: "NMAP ping sweep Scan"; dsize:0;sid:10000004; rev: 1; )
```
## kali 
```
nmap -sp 192.168.1.1
```

## 介紹
```
https://www.hackingarticles.in/detect-nmap-scan-using-snort/
```
