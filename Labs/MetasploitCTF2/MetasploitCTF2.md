# Host and Network Penetration Testing - The Metasploit Framework CTF 2 (eJPT / INE)

## Objective
Use the Metasploit Framework to enumerate, exploit, and escalate privileges on the target machine.

---

## Reconnaissance
- Ran `nmap -sC -sV` scan to identify services.
- Found open ports including SMB (port 445) and HTTP (port 80).
- Identified potential vulnerabilities and service versions.

## Exploitation
- Used Metasploit modules to exploit discovered services:
  - `exploit/windows/smb/ms08_067_netapi` or similar (based on vulnerability)
- Established a Meterpreter session on the target.

## Post-Exploitation
- Collected system information: `sysinfo`, `ipconfig`, etc.
- Listed and searched for user documents.
- Dumped credentials using `hashdump` and token impersonation.

## Privilege Escalation
- Enumerated using `getsystem` and local exploit suggester modules.
- Achieved SYSTEM-level access through known privilege escalation paths.

## Flags Captured
- Located and exfiltrated user and system flags from `C:\Users\...\Desktop`.

---

## Tools Used
- Nmap
- Metasploit Framework
- Meterpreter

---

## Conclusion
This CTF reinforced the workflow of using Metasploit for efficient enumeration, exploitation, and escalation within a Windows environment.
