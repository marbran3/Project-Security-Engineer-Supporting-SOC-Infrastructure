# Network Forensic Analysis Report

## Time Thieves

You must inspect your traffic capture to answer the following questions:

  1. What is the domain name of the users' custom site? frank-n-ted.com
  2. What is the IP address of the Domain Controller (DC) of the AD network? 10.6.12.12
  3. What is the name of the malware downloaded to the 10.6.12.203 machine? june11.dll 
      - Once you have found the file, export it to your Kali machine's desktop.
  4. Upload the file to VirusTotal.com.
  5. What kind of malware is this classified as? This is classified as a Trojan.

## Vulnerable Windows Machine

1. Find the following information about the infected Windows machine:
    - Host name Rotterdam-PC
    - IP address 172.16.4.205
    - MAC address 00:59:07:b0:63:a4
2. What is the username of the Windows user whose computer is infected? The username is matthijs.devries
3. What are the IP addresses used in the actual infection traffic?  
   *Based on filtering for IP 172.16.4.205 and the conversations statistics, the IP’s that had the most traffic  
   were from 166.62.111.64 (mysocalledchaos.com) and to 185.243.115.84 (b5689023.green.mattingsolutions.co)   
   filters:  
   ip.src == 172.16.4.205  
   Statistics > Conversations > IPv4 > Packets sorted high to low*  
4. As a bonus, retrieve the desktop background of the Windows host. Desktop image has a bird on it.
   
## Illegal Downloads
1. Find the following information about the machine with IP address 10.0.0.201:  
    - MAC address 00:16:17:18:66:c8
    - Windows username elmer.blanco
    - OS version appears to be Windows 10, based on the User-Agent
    - Computer host name BLANCO-DESKTOP or DOGOFTHEYEAR. Both use the same MAC address  
2. Which torrent file did the user download? The movie was: Betty Boop – Rhythm on the Reservation.  


