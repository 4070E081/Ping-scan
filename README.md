# Ping-scan

## rules
```
alert icmp any any -> any any (msg: "NMAP ping Scan"; dsize:0;sid:10000004; rev: 1; )
```
## kali 
```
nmap -sp 192.168.1.1 --disable-arp-ping
將執行上面的命令而沒有參數加“disable arp-ping”那麼它默認的掃描，會arp數據包，儘管在目標網絡上發送ICMP，有可能snort無法讀取NMAP Ping掃描，因此我們在上面的命令中使用了參數“disable arp-ping”。
```

## 介紹
```
https://www.hackingarticles.in/detect-nmap-scan-using-snort/
```
