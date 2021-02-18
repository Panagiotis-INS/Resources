# How to work with Machines #

nmap -sV -sC <machine ip><br>
In order to see what services the machine runs<br>

# Enumeration: # 


- HTTP service:<br>
- - gobuster<br>
- - wfuuz<br>

- Samba:<br>
-- enum4linux -a <machine ip>

- Apache Tomcat:<br>
- - Bad/Default/Common credentials there is areally good chance that this type of app uses default creds found on 


# Figurring out What exploit to use #<br>

1st step:If it is allowed try to use Metasploit/or and try to set it  up yourself based on a ready exploit
2nd:Metasploit is not always allowed:<br>
  - Understand the srvices:If you can understand what services the machine runs you can start searching for the right exploit
  - HOW to search 
  - - We suppose that you know the exploit name and/or have run a nmap vuln scan with the right script
  - - - If the exploit is in the msfconsole the set it up from inside msf and/or find the files in the exploitdb (use search command on msf)
  - - - If the exploit is not in the framework then use <b>searchsploit</b> and set it up from files found on the web
