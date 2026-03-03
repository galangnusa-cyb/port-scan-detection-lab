# Nmap Commands Used

Target: 192.168.28.128 (Ubuntu)

## SYN scan
sudo nmap -sS -p 1-1000 192.168.28.128 -T4 -Pn

## TCP connect scan
nmap -sT -p 1-1000 192.168.28.128 -T4 -Pn

## Service/version detection
sudo nmap -sS -sV -p 1-1000 192.168.28.128 -T4 -Pn

## UDP scan (optional / slower)
sudo nmap -sU -p 1-200 192.168.28.128 -T3 -Pn
