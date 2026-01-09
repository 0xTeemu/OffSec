# Nmap commands

## First quick scan to check open TCP ports 
```
sudo nmap -p- --min-rate 10000 -oA $ip $ip
```

## Second scan to check services of open ports. NOTE! Uses xclip for adding final command to clipboard.
```
echo "sudo nmap -vvv -Pn -sCV -T4 -p $(grep -oP '^\d+/tcp' $ip.nmap | awk -F/ '{print $1}' | paste -sd, -) --reason -oA specific_$ip \$ip" | xclip -selection clipboard
```
