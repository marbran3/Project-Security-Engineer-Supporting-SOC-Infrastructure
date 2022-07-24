# Red Team: Summary of Operations

## Table of Contents
- Exposed Services
- Critical Vulnerabilities
- Exploitation

### Exposed Services  

Nmap scan results for each machine reveal the below services and OS details:  

*$ nmap -sV -sC 192.168.1.110*  

*Additional nmap scan showed 1 more open port. This scan search in stealth mode for any open port  
in a “very verbose” mode. Port 54294 (according to Wikipedia’s list of all TCP & UDP port numbers) is  
unofficially used for Certificate Management over CMS. CMS Is Cryptographic Message Syntax. It’s the  
standard for messages protected cryptographically, to “digitally sign, digest, authenticate or encrypt  
any form of digital data”. (Wikipedia, Cryptographic Message Syntax)  
   nmap -sS -n -p- -vv -O 192.168.1.110*
  
These scans identify the services below as potential points of entry:  
- Target 1
  - Port 22 - ssh
  - Port 80 – http
  - Port 111 – rpcbind
  - Port 139 – netbios-ssn Samba smbd 3.X – 4.X
  - Port 445 – netbios-ssn Samba smbd 4.2.14-Debian
  - Port 54294 - TCP  

The following vulnerabilities were identified on each target:
- Target 1 – IP 192.168.1.110
  - Based on the wpscan, several vulnerabilities were found:
    - CVE-2013-0235
      - Severity is not listed – indicated as maintenance and security update since  version 3.5.1
      - Has many names
      - For any version older than 3.5.1
      - Allows remote attackers to send HTTP request to intranet servers, and conduct port-scanning attacks, also allows for DDOS attacks, also attackers to execute arbitrary code
      - This version was 3.7.8, so may not be as vulnerable
      - The known vulnerabilities have been patched, another solution indicated was to remove pingback.ping
    - CVE-2018-6389 – DoS attacks
      - Severity is 7.5 (high)
      - Through version 4.9.2, attackers can cause a denial of service attack.
      - While not giving unauthorized access to a hacker, it could cripple the availability of a website
      - Simple solution is to block unauthorized users from loading .php scripts.
    - CVE-2022-1299 
      - While numbered, it is still awaiting analysis according to National Vulnerability Database
      - Affects the slideshow plugin for WordPress.
      - High-privileged users could perform Cross-Site Scripting attacks
        - If a hacker was able to elevate to root, a hacker may be able to exploit this.

