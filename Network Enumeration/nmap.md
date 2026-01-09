# Nmap commands

## First quick scan to check open TCP ports 
```
sudo nmap -p- --min-rate 10000 -oA $ip $ip
```
