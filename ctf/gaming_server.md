10.145.188.158
rust-scan: look for open ports

nikto -h "http://IP" | tee nikto.log

gobuster dir -u http://IP -w /opt/directory-list-2.3-medium.txt

Now go to web poke around