open tryhackme on Ubuntu VM 

download vpn file

sudo opevpn <file>

now should be conneceted hehehe

````md
# Tools Required for Web Pentesting

## 1. Update System
```bash
sudo apt update && sudo apt upgrade -y
````

## 2. Install Main Tools

```bash
sudo apt install -y nikto gobuster john wget openssh-client nmap git curl
```

## 3. Install RustScan

```bash
sudo snap install rustscan
```

## 4. Install Wordlists (SecLists)

```bash
git clone https://github.com/danielmiessler/SecLists.git
```

## 5. Install Extra Tools

```bash
sudo apt install -y ffuf dirsearch
```

## 6. Install Nuclei

```bash
sudo apt install -y nuclei
```

### If not available:

```bash
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
```

## 7. Install Subdomain Enumeration Tool

```bash
sudo apt install -y amass
```

## 8. Install Technology Detection Tool

```bash
sudo apt install -y whatweb
```

## 9. Install Burp Suite (Community Edition)

```bash
sudo apt install -y burpsuite
```

## 10. Install Optional Cracking Tool

```bash
sudo apt install -y hashcat
```

## 11. Install Privilege Escalation Script (linPEAS)

```bash
wget https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh
chmod +x linpeas.sh
```

## 12. Fix Common Wordlist Path

### Your Notes:

```
/opt/directory-list-2.3-medium.txt
```

### Correct Path on Ubuntu:

```
SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt
```

## 13. Final Verification

```bash
rustscan --version
nikto -Version
gobuster version
john --list=build-info
nmap --version
```

```
```
