# CYBERSECURITY-INTERNSHIP-
Task 1: Scan Your Local Network for Open Ports
Cyber Security Internship – Task 1
Objective: Perform a local network scan to discover open ports and understand the exposure of network services.  


 Tools Used
-Nmap (for port scanning)

Steps Performed
1. Installed Nmap on my system.
2. Found my local IP range using `ipconfig` (Windows) / `ifconfig` (Linux/Mac).
3. Ran a SYN scan on the full subnet:
   
nmap -sS  10.68.147.127 -oN scan_results.txt

-Identified live hosts and noted their open ports.
nmap -sS  10.68.147.127 -oN scan_results.txt

PORT    STATE SERVICE
135/tcp open  msrpc
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds

 Port  Service       Description                         Risk    Suggested Mitigation                            
 
 135   MSRPC         Remote procedure calls for Windows  Medium  Restrict via firewall; keep system patched      
 139   NetBIOS-SSN   Legacy file/printer sharing         Medium  Disable NetBIOS if unused; firewall restrict    
 445   Microsoft-DS  SMB file and printer sharing        High    Disable SMBv1; LAN-only access; patch regularly 
