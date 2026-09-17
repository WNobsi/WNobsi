<div align="center">

# Nobex Wahengbam

### PJPT-Certified Penetration Tester | Active Directory & Web Application Security

[![PJPT Certified](https://img.shields.io/badge/PJPT-Certified-00d4ff?style=for-the-badge&logo=security&logoColor=white)](https://certified.tcm-sec.com/6bd6e2e8-01d5-43f8-b508-d0544b58e4af)
[![Active Directory](https://img.shields.io/badge/Active%20Directory-17%20Techniques-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/WNobsi/Active-Directory-Home-Lab-VAPT)
[![OWASP Top 10](https://img.shields.io/badge/OWASP%20Top%2010-32%20Findings-FF6B00?style=for-the-badge&logoColor=white)](https://github.com/WNobsi/web-application-vapt-lab)
[![Portfolio](https://img.shields.io/badge/Portfolio-Live-00d4ff?style=for-the-badge&logo=github&logoColor=white)](https://wnobsi.github.io/portfolio/)

**📍 Mumbai, India** · **🎯 Open to Penetration Testing & Red Team Roles**

</div>

---

## 💼 Professional Summary

PJPT-certified penetration tester with hands-on experience in **Active Directory exploitation** (17 documented attack techniques) and **web application security testing** (32 OWASP Top 10 findings). Proven ability to build realistic enterprise attack scenarios, document complete kill chains, and provide actionable remediation recommendations.

**What I Bring to Your Team:**
- ✅ Real-world penetration testing methodology (PTES, OWASP Testing Guide)
- ✅ Complete attack documentation from reconnaissance to post-exploitation
- ✅ MITRE ATT&CK framework mapping for threat intelligence alignment
- ✅ Professional-grade security reports with CVSS scoring and business impact analysis
- ✅ Defensive mindset — every attack paired with detection and mitigation strategies

---

## 🎓 Certifications

| Certification | Issuer | Year | Verification |
|---|---|---|---|
| **✅ PJPT** (Practical Junior Penetration Tester) | TCM Security | 2026 | [Verify Certificate](https://certified.tcm-sec.com/6bd6e2e8-01d5-43f8-b508-d0544b58e4af?key=afa14ac35bc9e12f22ad1096cf67d455a3e978cc8477123f8d62cf1d428c135e) |

---

## 🏗️ Featured Projects

### 🏰 Active Directory Home Lab — Complete VAPT

[![View Project](https://img.shields.io/badge/View%20on%20GitHub-Active%20Directory%20VAPT-0078D4?style=for-the-badge&logo=github&logoColor=white)](https://github.com/WNobsi/Active-Directory-Home-Lab-VAPT)

**Enterprise-grade AD penetration testing lab** simulating realistic attack chains from initial access to Domain Admin compromise.

**Key Achievements:**
- 🎯 **17 documented attack techniques** across full kill chain
- 🏢 **3-machine Windows domain** (BATMAN.local) — DC + 2 workstations
- 🔑 **Complete credential access chain** — LLMNR poisoning → Kerberoasting → Golden Ticket
- 🛡️ **Defense-aware** — every attack paired with Event ID detection and GPO hardening
- 📊 **MITRE ATT&CK mapped** — 15+ TTP IDs documented

**Attack Coverage:**
| Technique | MITRE ID | Impact |
|---|---|---|
| LLMNR/NBT-NS Poisoning | T1557.001 | NTLMv2 hash capture |
| SMB Relay | T1557.001 | SAM/LSA dumping |
| Kerberoasting | T1558.003 | Service account compromise |
| Pass-the-Hash | T1550.002 | Lateral movement |
| Mimikatz / LSASS Dumping | T1003.001 | Credential extraction |
| Golden Ticket | T1558.001 | Persistent DA access |
| ZeroLogon (CVE-2020-1472) | CVE-2020-1472 | DC takeover |
| PrintNightmare (CVE-2021-1675) | CVE-2021-1675 | SYSTEM escalation |

**Tools Used:** Responder, Impacket Suite, Bloodhound, Mimikatz, Hashcat, NetExec, mitm6

---

### 🌐 Web Application VAPT Lab — OWASP Top 10

[![View Project](https://img.shields.io/badge/View%20on%20GitHub-Web%20Application%20VAPT-FF6B00?style=for-the-badge&logo=github&logoColor=white)](https://github.com/WNobsi/web-application-vapt-lab)

**Comprehensive web security testing** across DVWA and PortSwigger Web Security Academy with professional pentest reporting.

**Key Achievements:**
- 🎯 **32 documented vulnerabilities** with full exploitation walkthroughs
- 🔴 **9 Critical findings** — SQL injection, command injection, unrestricted file upload → RCE
- 🟠 **19 High severity** — XSS (reflected, stored, DOM), authentication bypass, CSRF, IDOR
- 📋 **Enterprise report** — CVSS v3.1 scoring, remediation recommendations, Burp Suite evidence
- ✅ **100% OWASP Top 10 (2021) coverage**

**Vulnerability Classes:**
| Category | Findings | Severity |
|---|---|---|
| **A03: Injection** | SQL Injection (6), XSS (6), Command Injection (2) | Critical/High |
| **A01: Broken Access Control** | CSRF, IDOR, Unprotected Admin (4) | Critical/High |
| **A07: Authentication Failures** | 2FA bypass, Brute-force, Session fixation (5) | Critical/High |
| **A04: Insecure Design** | File Upload RCE, API flaws (5) | Critical/High |
| **A05: Security Misconfiguration** | LFI, Info disclosure (2) | High/Medium |

**Tools Used:** Burp Suite, sqlmap, Nmap, Hydra, netcat, msfvenom

---

## 🖥️ CTF & Machine Writeups

### Recent Completions:

| Platform | Machine/Challenge | Type | Key Techniques |
|---|---|---|---|
| **HTB** | [Cyber Apocalypse 2026: Gatery](https://github.com/WNobsi/HTB-Cyber-Apocalypse-2026-Gatery) | Web CTF | Session management bypass, broken authorization |
| **TCM** | [BlackPearl](https://github.com/WNobsi/TCM-BlackPearl-Machine-Walkthrough) | Linux | Web exploitation, privilege escalation |
| **TCM** | [Butler](https://github.com/WNobsi/TCM-Butler-Machine-Walkthrough-) | Windows | Jenkins RCE, unquoted service path → SYSTEM |
| **TCM** | [Dev](https://github.com/WNobsi/TCM-Dev-Machine-Walkthrough) | Linux | Boltwire LFI, NFS enumeration, sudo abuse |
| **TCM** | [Academy](https://github.com/WNobsi/TCM-Academy-Machine-Walkthrough) | Linux | FTP disclosure, file upload, cron job abuse → root |
| **VulnHub** | [Kioptrix Level 1](https://github.com/WNobsi/kioptrix.level1-using-Metaploit) | Linux | Samba trans2open exploit, mod_ssl buffer overflow |

---

## 🛠️ Technical Skills

### Active Directory & Internal Network
- **Credential Access:** LLMNR poisoning, SMB relay, Kerberoasting, LSASS dumping, NTDS.dit extraction
- **Lateral Movement:** Pass-the-Hash, PSExec, WMIExec, SMBExec
- **Privilege Escalation:** Token impersonation, Golden Ticket, ZeroLogon, PrintNightmare
- **Enumeration:** Bloodhound, ldapdomaindump, NetExec, PingCastle
- **Tools:** Responder, Impacket, Mimikatz, Hashcat, mitm6, Metasploit

### Web Application Security
- **OWASP Top 10:** SQL injection (UNION, blind, auth bypass), XSS (reflected, stored, DOM), command injection
- **Access Control:** CSRF, IDOR, authentication bypass, session management flaws
- **File Security:** Unrestricted upload → RCE, LFI/RFI, path traversal
- **API Security:** Mass assignment, parameter pollution, SSRF, endpoint enumeration
- **Tools:** Burp Suite, sqlmap, Nmap, Hydra, ffuf, Nikto

### Exploitation & Post-Exploitation
- **Linux PrivEsc:** SUID abuse, sudo misconfiguration, cron jobs, kernel exploits
- **Windows PrivEsc:** Unquoted service paths, weak service ACLs, registry exploitation
- **CVE Research:** Exploit-DB, GitHub PoCs, Metasploit modules
- **Reverse Shells:** bash /dev/tcp, PHP, Groovy, netcat, msfvenom payloads
- **Tools:** LinPEAS, winPEAS, GTFOBins

### Scripting & Automation
- **Python 3:** pwntools, Paramiko, custom exploitation scripts
- **Bash:** Automation, enumeration scripts, reverse shell one-liners
- **PowerShell:** Windows post-exploitation, service manipulation

### Methodologies & Frameworks
- **MITRE ATT&CK:** 15+ techniques mapped with detection strategies
- **OWASP Testing Guide:** Web application testing methodology v4.2
- **PTES:** Penetration Testing Execution Standard
- **CVSS v3.1:** Vulnerability severity scoring and risk assessment

---

## 📊 Portfolio Statistics

```
🎯 Active Directory Attacks Documented:    17
🌐 Web Vulnerabilities Found:              32
🏆 Machines Compromised:                   6
📝 Technical Writeups Published:           9
🛠️ Tools Mastered:                        30+
📋 Professional Reports Generated:         2
🔴 Critical Findings:                      9
🟠 High Severity Findings:                 19
```

---

## 📞 Contact & Links

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-wnobsi.github.io-00d4ff?style=for-the-badge&logo=github)](https://wnobsi.github.io/portfolio/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-in%2Fwnobex-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/wnobex/)
[![Email](https://img.shields.io/badge/Email-wnobex%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:wnobex@gmail.com)

[![TryHackMe](https://img.shields.io/badge/TryHackMe-itsNobushi-212C42?style=for-the-badge&logo=tryhackme)](https://tryhackme.com/p/itsNobushi)
[![HackTheBox](https://img.shields.io/badge/HackTheBox-Profile-9FEF00?style=for-the-badge&logo=hackthebox&logoColor=black)](https://profile.hackthebox.com/profile/019d674b-e4f9-70d6-a8b8-f9012e6c5cf2)

</div>

---

## 🎯 What I'm Looking For

**Open to roles in:** Penetration Testing, Red Team Operations, Security Assessment, Application Security Testing

**Preferred location:** Mumbai, India (open to remote opportunities)

**Why hire me?**
- ✅ Production-ready penetration testing skills backed by 50+ documented vulnerabilities
- ✅ PJPT certification validating real-world AD and network pentesting ability
- ✅ Strong documentation skills — every attack includes methodology, evidence, and remediation
- ✅ Defensive mindset — understand both offensive techniques and detection/mitigation strategies
- ✅ Continuous learner — active on HTB, THM, and TCM platforms with ongoing CTF participation

---

<div align="center">

### 💡 "Understanding why an attack works, how defenders detect it, and how to document findings in a professional consulting style."

**⚠️ All techniques demonstrated in isolated, self-owned virtual labs for educational purposes only.**

</div>
