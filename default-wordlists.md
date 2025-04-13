# 📂 Default Wordlists in Kali Linux

This document provides a curated list of pre-installed wordlists typically found in Kali Linux and similar pentesting distributions. These wordlists are used for tasks such as brute-force attacks, directory discovery, fuzzing, password auditing, and subdomain enumeration.

---

## 📌 Wordlists Overview

| Wordlist       | Path                                                                 | Description                                                                 | Tools Used                        |
|----------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------|
| **amass**      | `/usr/share/amass/wordlists`                                         | Wordlists for DNS enumeration and subdomain discovery.                      | `amass`                          |
| **dirb**       | `/usr/share/dirb/wordlists`                                          | Classic directory brute-forcing wordlists.                                 | `dirb`                           |
| **dirbuster**  | `/usr/share/dirbuster/wordlists`                                     | Extensive wordlists for web directory brute-forcing (small, medium, big).  | `DirBuster`, `Gobuster`, `ffuf` |
| **dnsmap.txt** | `/usr/share/dnsmap/wordlist_TLAs.txt`                                | Common DNS subdomain names.                                                 | `dnsmap`                         |
| **fasttrack.txt** | `/usr/share/set/src/fasttrack/wordlist.txt`                       | Wordlist included in the Social-Engineer Toolkit (SET).                     | `SET`, `Hydra`                   |
| **fern-wifi**  | `/usr/share/fern-wifi-cracker/extras/wordlists`                     | Wi-Fi password brute-force dictionaries.                                    | `Fern Wifi Cracker`             |
| **john.lst**   | `/usr/share/john/password.lst`                                       | Default password list used by John the Ripper.                              | `John`                           |
| **legion**     | `/usr/share/legion/wordlists`                                        | Wordlists for usernames/passwords used by Legion.                           | `Legion`                         |
| **metasploit** | `/usr/share/metasploit-framework/data/wordlists`                    | Wordlists for various services (e.g., PostgreSQL, HTTP) within Metasploit.  | `Metasploit`                     |
| **nmap.lst**   | `/usr/share/nmap/nselib/data/passwords.lst`                          | Simple password list used in Nmap's NSE scripts.                            | `Nmap`                           |
| **rockyou.txt.gz** | `/usr/share/wordlists/rockyou.txt.gz`                            | Famous leaked password list (~14M), often used in brute-force scenarios.    | `Hydra`, `John`, `Hashcat`      |
| **sqlmap.txt** | `/usr/share/sqlmap/data/txt/wordlist.txt`                            | Used during SQL injection testing.                                          | `sqlmap`                         |
| **wfuzz**      | `/usr/share/wfuzz/wordlist`                                          | Fuzzing and param brute-force wordlists.                                    | `wfuzz`, `ffuf`, `Burp`         |
| **wifite.txt** | `/usr/share/dict/wordlist-probable.txt`                              | Common WiFi password wordlist.                                              | `wifite`                         |

---

> 🔍 Tip: To locate all available wordlists, use the following command:
> ```bash
> find /usr/share/wordlists/ -type l -o -type f
> ```


