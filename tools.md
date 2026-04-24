# Tools Functionalities for Web Pentesting

---

## 1. Recon / Information Gathering

### Goal
Identify target, tech stack, and entry points

### Tools & Functions

**nslookup, dig**
- Resolve domain → IP address
- Query DNS records (A, MX, TXT)
- Identify:
  - server IP
  - mail servers
  - DNS misconfigurations

**subfinder, amass**
- Discover subdomains
- Methods:
  - public datasets (certificates, DNS logs)
  - brute force (wordlists)
- Finds hidden assets:
  - admin panels
  - dev environments

**whatweb, wappalyzer**
- Detect technologies
- Analyze:
  - HTTP headers
  - HTML structure
  - scripts/libraries
- Identify:
  - server (Apache, Nginx)
  - backend (PHP, Node)
  - frameworks (WordPress, Laravel)

**curl -I**
- Fetch HTTP headers only
- Reveals:
  - server type
  - cookies
  - redirects
  - security headers

### Output
- Domain → IP
- Tech stack
- Initial attack surface

---

## 2. Scanning (Network Level)

### Goal
Find open ports and services

### Tools & Functions

**nmap**
- Port scanning
- Service/version detection
- Features:
  - OS detection
  - NSE scripts for vulnerability checks

**rustscan**
- Fast port scanning (all 65k ports)
- Passes results to Nmap
- Optimized for speed

### Purpose
- Identify exposed services (HTTP, SSH, FTP)
- Build attack surface

---

## 3. Enumeration (Web Mapping)

### Goal
Discover hidden endpoints and files

### Tools & Functions

**gobuster, ffuf, dirsearch**
- Brute-force directories/files
- Use wordlists:
  - /admin
  - /login
  - /uploads
- Detect valid responses (200, 403)

**nikto**
- Scan for:
  - outdated software
  - dangerous files
  - insecure configurations

**browser (manual)**
- Inspect:
  - HTML source
  - comments
  - hidden inputs
  - JavaScript files
- Reveals:
  - endpoints
  - credentials
  - clues

### Purpose
- Map application structure
- Find hidden files, APIs, upload points

---

## 4. Traffic Interception

### Goal
Inspect and modify HTTP requests

### Tools

**Burp Suite, OWASP ZAP**

### Functions
- Act as proxy between browser and server
- Intercept and modify requests
- Replay requests
- Test authentication logic

### Purpose
- Understand backend behavior
- Manipulate parameters
- Identify vulnerabilities

---

## 5. Vulnerability Discovery

### Goal
Identify weaknesses

### Automated Tools

**nikto**
- Detect server misconfigurations

**nuclei**
- Scan for known vulnerabilities (CVEs)
- Template-based, high-speed scanning

**OWASP ZAP**
- Automated vulnerability scanning:
  - XSS
  - SQLi
  - insecure headers

### Manual Tools

**ffuf, wfuzz**
- Fuzz parameters with payloads
- Detect:
  - file inclusion
  - command injection

**Burp Intruder**
- Automate request variations
- Used for:
  - brute-force
  - parameter discovery

### Purpose
- Identify:
  - SQL injection
  - XSS
  - auth bypass
  - file upload flaws

---

## 6. Exploitation

### Goal
Gain access

### Tools & Functions

**sqlmap**
- Automates SQL injection exploitation
- Can:
  - dump databases
  - extract credentials

**Metasploit**
- Exploit known vulnerabilities (CVEs)
- Prebuilt exploit modules

**Burp Suite**
- Manual exploitation
- Craft custom payloads
- Modify requests

### Purpose
- Gain shell access
- Extract sensitive data
- Bypass authentication

---

## 7. Post-Exploitation

### Goal
Escalate privileges and expand access

### Tools & Functions

**ssh**
- Access remote system with credentials/keys

**linpeas, pspy**
- Privilege escalation enumeration
- Identify:
  - SUID binaries
  - cron jobs
  - misconfigurations

**john, hashcat**
- Password cracking
- Brute-force hashes or keys

### Purpose
- Escalate privileges
- Extract sensitive data
- Move laterally

---

## 8. Reporting

### Goal
Document findings

### Tools

**notes, screenshots, reporting tools (e.g. Dradis)**

### Purpose
- Explain vulnerabilities
- Provide remediation steps
- Deliver professional report

---