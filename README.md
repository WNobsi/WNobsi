<div align="center">

# Nobex Wahengbam

### Offensive Security · Active Directory · Internal Network Penetration Testing

[![PJPT](https://img.shields.io/badge/PJPT-TCM%20Security-CC0000?style=for-the-badge&logo=checkmarx&logoColor=white)](https://certifications.tcm-sec.com/pjpt/)
[![Active Directory](https://img.shields.io/badge/Active%20Directory-Windows%20Server-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/WNobsi/Active-Directory-Home-Lab-VAPT)
[![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)](https://www.kali.org/)
[![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-Aligned-FF6B00?style=for-the-badge&logoColor=white)](https://attack.mitre.org/)

*Building enterprise Active Directory labs · Simulating realistic attack chains · Documenting offensive security methodology*

</div>

---

## 👤 About Me

Offensive Security practitioner with a background in **IT Support**, transitioning into **Internal Network Penetration Testing**. I focus on building and attacking realistic enterprise Active Directory environments, understanding attacks from both red and blue team perspectives, and producing professional-grade security documentation.

**Current Focus:**
- 🔴 Active Directory Red Team Operations
- 🏗️ Realistic Internal Network Lab Construction
- 🔑 Credential Access & Lateral Movement Chains
- 📋 Professional Penetration Test Reporting
- 🛡️ Defensive Mitigations & Hardening Guidance

---

## 🏅 Certifications

| Certification | Issuer | Domain |
|---|---|---|
| ✅ **PJPT** — Practical Junior Penetration Tester | [TCM Security](https://certifications.tcm-sec.com/pjpt/) | Internal Network / Active Directory Pentesting |

> The PJPT exam involves performing a full internal network penetration test against an enterprise Active Directory environment and producing a professional pentest report — the skills demonstrated directly in this profile's lab work.

---

## 🏗️ Featured Project — Active Directory Home Lab (VAPT)

[![AD Lab](https://img.shields.io/badge/View%20Lab-Active%20Directory%20Home%20Lab%20VAPT-0078D4?style=for-the-badge&logo=github&logoColor=white)](https://github.com/WNobsi/Active-Directory-Home-Lab-VAPT)

A complete, end-to-end penetration test of a self-built Windows Active Directory environment. The lab simulates a realistic enterprise domain (`BATMAN.local`) with a Domain Controller, two Windows workstations, and an isolated Kali Linux attacker — executing a full attack chain from unauthenticated network access to Domain Admin and Golden Ticket persistence.

**Lab Architecture:**
```
╔══════════════════════════════════════════════════════╗
║                  BATMAN.local Domain                 ║
║                                                      ║
║  ┌──────────────────┐     ┌──────────────────┐       ║
║  │  Domain Controller│     │  Windows Client  │       ║
║  │  192.168.126.139  │     │  192.168.126.140 │       ║
║  │  BATMAN-DC        │     │  THEFLASH        │       ║
║  └──────────────────┘     └──────────────────┘       ║
║                                                      ║
║  ┌──────────────────┐                                ║
║  │  Windows Client  │                                ║
║  │  192.168.126.141 │                                ║
║  │  SUPERMAN        │                                ║
║  └──────────────────┘                                ║
╚══════════════════════════════════════════════════════╝
                    │
          (Isolated NAT Network)
                    │
     ┌─────────────────────┐
     │   Attacker Machine  │
     │   192.168.126.128   │
     │   Kali Linux        │
     └─────────────────────┘
```

**Attack Coverage — 17 Techniques across the full kill chain:**

| # | Technique | MITRE ID | Tactic |
|---|---|---|---|
| 1 | LLMNR Poisoning | T1557.001 | Credential Access |
| 2 | SMB Relay Attack | T1557.001 | Credential Access |
| 3 | IPv6 / mitm6 Attack | T1557 · T1136.002 | Credential Access · Persistence |
| 4 | Gaining Shell Access | T1569.002 · T1550.002 | Execution · Lateral Movement |
| 5 | Initial Internal Attack Strategy | T1590 · T1046 | Reconnaissance · Discovery |
| 6 | Post-Compromise Enumeration | T1087.002 · T1069.002 · T1482 | Discovery |
| 7 | Pass the Password / Pass the Hash | T1550.002 · T1021.002 | Lateral Movement |
| 8 | Dumping & Cracking Hashes | T1003.002 · T1003.004 · T1110.002 | Credential Access |
| 9 | Kerberoasting | T1558.003 | Credential Access |
| 10 | Token Impersonation | T1134.001 | Privilege Escalation |
| 11 | LNK File Attacks | T1187 | Credential Access |
| 12 | GPP / cPassword Attacks | T1552.006 | Credential Access |
| 13 | Mimikatz & Credential Dumping | T1003.001 · T1555.004 | Credential Access |
| 14 | Dumping NTDS.dit | T1003.003 | Credential Access |
| 15 | Golden Ticket Attacks | T1558.001 · T1550.003 | Persistence · Lateral Movement |
| 16 | ZeroLogon — CVE-2020-1472 | T1210 · T1068 | Lateral Movement · Privilege Escalation |
| 17 | PrintNightmare — CVE-2021-1675 | T1210 · T1068 | Lateral Movement · Privilege Escalation |

---

## 🔴 Red Team — Tools

### Network & Protocol Attacks
| Tool | Purpose |
|---|---|
| [Responder](https://github.com/SpiderLabs/Responder) | LLMNR / NBT-NS / MDNS poisoning — passive NTLMv2 hash capture |
| [mitm6](https://github.com/dirkjanm/mitm6) | IPv6 / DHCPv6 man-in-the-middle — rogue IPv6 DNS server |
| [Nmap](https://nmap.org/) | Network scanning, SMB signing detection, service enumeration |

### Credential Access & Hash Cracking
| Tool | Purpose |
|---|---|
| [Hashcat](https://hashcat.net/) | GPU-accelerated offline hash cracking (NTLMv2 `5600`, NTLM `1000`, Kerberos TGS `13100`) |
| [Impacket](https://github.com/fortra/impacket) | `ntlmrelayx`, `secretsdump`, `psexec.py`, `GetUserSPNs` — full AD attack suite |
| [Mimikatz](https://github.com/gentilkiwi/mimikatz) | LSASS memory credential extraction, Golden Ticket forging (`sekurlsa::logonPasswords`, `kerberos::golden`) |

### Post-Compromise & Lateral Movement
| Tool | Purpose |
|---|---|
| [NetExec](https://github.com/Pennyw0rth/NetExec) | Credential spraying, PTH, SAM/LSA/LSASS remote dumping across subnets (successor to CrackMapExec) |
| [Metasploit Framework](https://www.metasploit.com/) | PSExec exploitation, Meterpreter sessions, token impersonation via `incognito` |

### Active Directory Enumeration & Reporting
| Tool | Purpose |
|---|---|
| [Bloodhound](https://github.com/SpecterOps/BloodHound) | Graph-based AD attack path analysis — visualise shortest paths to Domain Admin |
| [bloodhound-python](https://github.com/dirkjanm/BloodHound.py) | Python-based Bloodhound data collector (`-c all`) |
| [PlumHound](https://github.com/PlumHound/PlumHound) | Automated HTML report generation from Bloodhound Neo4j data |
| [ldapdomaindump](https://github.com/dirkjanm/ldapdomaindump) | LDAP domain enumeration — users, groups, computers, GPOs |
| [PingCastle](https://www.pingcastle.com/) | Active Directory domain risk scoring and client-deliverable security reporting |

---

## 🧠 Red Team — Concepts & Techniques

### Credential Access
- **LLMNR / NBT-NS Poisoning** — passive NTLMv2 hash capture via Windows multicast name resolution fallback
- **SMB Relay** — relay captured hashes in real-time to authenticate as the victim, bypassing the need to crack
- **Kerberoasting** — request TGS-REP tickets for SPNs and crack offline with any domain user account
- **Pass-the-Hash (PTH)** — authenticate with NTLM hash directly, no plaintext password required
- **Pass-the-Password** — spray valid credentials across subnets to identify lateral movement targets
- **LSASS Memory Dumping** — extract cached credentials, NTLM hashes, and Kerberos tickets from LSASS
- **SAM / LSA Secrets Dumping** — extract local account hashes and service account credentials
- **NTDS.dit Extraction** — dump the entire domain credential database via DRSUAPI replication protocol
- **GPP / cPassword** — decrypt GPO-stored passwords using the publicly-leaked Microsoft AES encryption key

### Lateral Movement & Execution
- **PSExec (Impacket & Metasploit)** — remote SYSTEM shell via SMB service execution
- **WMIExec / SMBExec** — stealthy remote execution alternatives leaving minimal disk artefacts
- **SMB Relay Shell** — interactive shells and remote command execution via ntlmrelayx relay chain
- **LNK File Attacks** — force hash capture by embedding UNC paths in Windows shortcut files placed on shares

### Privilege Escalation & Persistence
- **Token Impersonation** — steal Domain Admin delegation tokens from memory using Meterpreter `incognito`
- **Golden Ticket** — forge Kerberos TGTs signed with the `krbtgt` hash for permanent, persistent domain access
- **IPv6 / LDAP Relay** — relay high-privilege authentication to LDAPS to create new domain admin accounts passively
- **Domain Account Backdoor** — add DA persistence accounts (`net user /add ... /domain`) via impersonated token context

### CVE Exploitation
- **ZeroLogon (CVE-2020-1472)** — CVSS 10.0, unauthenticated Domain Controller takeover via Netlogon AES-CFB8 flaw
- **PrintNightmare (CVE-2021-1675 / CVE-2021-34527)** — domain user to SYSTEM via Print Spooler RCE (tested against hardened Server 2022)

---

## 🛡️ CDIR — Cyber Defence & Incident Response

Every attack in the lab is documented alongside its corresponding detection and mitigation strategy — building both offensive and defensive understanding.

### Detection & Mitigation Coverage

| Attack Vector | Key Detection | Mitigation |
|---|---|---|
| LLMNR Poisoning | LLMNR/NBT-NS traffic spikes; Event ID 4625 | Disable LLMNR & NBT-NS via GPO |
| SMB Relay | Unexpected cross-host SMB auth; lateral movement | Enable SMB Signing on ALL endpoints |
| IPv6 / mitm6 | Rogue DHCPv6 traffic; unexpected DNS server changes | Block DHCPv6 via Windows Firewall GPO |
| Pass-the-Hash | Event ID 4624 Type 3 anomalies; LAPS violations | LAPS; unique local admin passwords; account tiering |
| Kerberoasting | Bulk TGS-REQ from single account; Event ID 4769 | gMSA; service account passwords >25 characters |
| Token Impersonation | Admin logons to workstations; privilege escalation events | Account Tiering; Privileged Access Workstations (PAW) |
| LSASS Dumping | Process access to lsass.exe; Event ID 4656 | Credential Guard; LSASS PPL; EDR |
| Golden Ticket | Anomalous Kerberos ticket lifetimes; Event ID 4769/4770 | Rotate `krbtgt` TWICE; Microsoft Defender for Identity |
| NTDS.dit Dump | DRSUAPI replication from non-DC source; Event ID 4662 | Limit DCSync rights; monitor replication events |
| ZeroLogon | Netlogon auth with empty credentials; Event ID 5829 | Apply August 2020 patch; enforce Netlogon secure channel |
| GPP/cPassword | SYSVOL XML files containing `cPassword` attribute | Delete GPP XML files; apply KB2962486 |

### Hardening Principles Documented
- **Account Tiering (Tier 0/1/2)** — prevent Domain Admin credentials from being exposed on workstations
- **Privileged Access Workstations (PAW)** — dedicated hardened machines for all privileged administrative tasks
- **Protected Users Security Group** — prevents delegation token creation for sensitive high-privilege accounts
- **LSASS as Protected Process Light (PPL)** — block LSASS memory reads even with local admin rights
- **Credential Guard (VBS)** — virtualization-based security isolating LSASS from the OS
- **SMB Signing** — prevent relay attacks across the entire domain
- **gMSA (Group Managed Service Accounts)** — eliminate Kerberoastable service accounts with 120-char auto-rotated passwords
- **LDAP Signing & Channel Binding** — prevent LDAP relay attacks targeting Domain Controllers

### Defensive Tools Explored
| Tool | Defensive Use |
|---|---|
| PingCastle | Domain risk scoring; finds stale accounts, over-privileged DAs, trust issues |
| Bloodhound | Identify and remediate attack paths *before* attackers do |
| PlumHound | Generate audit-ready HTML security reports from AD data |
| Windows Event Log | Correlated Event IDs mapped to each attack for SOC-level detection |

---

## 📚 Training & Resources

| Resource | Focus |
|---|---|
| [TCM Security — Practical Ethical Hacking](https://academy.tcm-sec.com) | Internal network pentesting, AD attacks — core PJPT curriculum |
| [MITRE ATT&CK for Enterprise](https://attack.mitre.org) | Threat modelling, technique IDs, tactic categorisation |
| [Impacket Documentation](https://github.com/fortra/impacket) | Core AD attack tooling reference |
| [SpecterOps Bloodhound Docs](https://support.bloodhoundenterprise.io) | Attack path analysis methodology |
| [Hashcat Wiki — Example Hashes](https://hashcat.net/wiki/doku.php?id=example_hashes) | Hash mode reference for all credential types |

---

## 🎯 Goals (2026)

- ✅ Earn PJPT
- 🔄 Continue expanding the Active Directory Attack Series
- ⏳ Secure first Offensive Security role
- ⏳ Build reusable offensive security tooling
- ⏳ Publish high-quality penetration testing documentation

---

<div align="center">

*"Understanding why an attack works, how defenders detect it, and how to document findings in a professional consulting style."*

[![GitHub](https://img.shields.io/badge/GitHub-WNobsi-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/WNobsi)

</div>
