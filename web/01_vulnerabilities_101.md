| Vulnerability | Description |
| --- | --- |
| Operating System | These types of vulnerabilities are found within Operating Systems (OSs) and often result in privilege escalation. |
| (Mis)Configuration-based | These types of vulnerabilities stem from an incorrectly configured application or service. For example, a website exposing customer details. |
| Weak or Default Credentials | Applications and services that have an element of authentication will come with default credentials when installed. For example, an administrator dashboard may have the username and password of `admin`. These are easy to guess by an attacker. |
| Application Logic | These vulnerabilities are a result of poorly designed applications. For example, poorly implemented authentication mechanisms that may result in an attacker being able to impersonate a user. |
| Human-Factor | Human-Factor vulnerabilities are vulnerabilities that leverage human behaviour. For example, phishing emails are designed to trick humans into believing they are legitimate. |

### CVSS
popular framework for vulnerability scoring and has three major iterations. As it stands, the current version is CVSSv3.1 (with version 4.0 currently in draft) a score is essentially determined by some of the following factors (but many more):     
    1. How easy is it to exploit the vulnerability?
    2. Do exploits exist for this?
    3. How does this vulnerability interfere with the CIA triad?

### VPR
much more modern framework in vulnerability management - developed by Tenable, an industry solutions provider for vulnerability management. This framework is considered to be risk-driven; meaning that vulnerabilities are given a score with a heavy focus on the risk a vulnerability poses to the organisation itself, rather than factors such as impact (like with CVSS)

### NVD – National Vulnerability Database
The National Vulnerability Database is a website that lists all publically categorised vulnerabilities. In cybersecurity, vulnerabilities are classified under “Common Vulnerabilities and Exposures” (Or CVE for short).

### Exploit-DB
Exploit-DB(opens in new tab) is a resource that we, as hackers, will find much more helpful during an assessment. Exploit-DB retains exploits for software and applications stored under the name, author and version of the software or application.