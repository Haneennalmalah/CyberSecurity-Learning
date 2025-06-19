# 🛡️ Red Teaming Notes

## 📌 What Is Red Teaming?
Red Teaming is a **full-scope simulated cyberattack** on an organization, designed to **test defenses** under realistic conditions. It goes beyond technical exploitation to include **social engineering**, **physical breaches**, and **strategic deception**.

> ✅ **Goal**: Emulate real-world attackers (APT, insider threat, hacktivists) to identify **gaps in detection and response** — not just vulnerabilities.

---

## 🧠 Key Concepts (With Real-World Flavor)

| Term | Description |
|------|-------------|
| **Red Team** | Offensive security experts simulating adversaries (e.g. APTs, ransomware gangs). Their job is to think like attackers. |
| **Blue Team** | Defenders (SOC analysts, incident responders, threat hunters) monitoring systems to detect and stop threats. |
| **Purple Team** | A collaborative team where Red & Blue work together to improve detection and response. |
| **TTPs** | **Tactics, Techniques, and Procedures** — the real behavior of adversaries (documented in MITRE ATT&CK). |
| **OPSEC** | Operational Security — Red Team must remain stealthy to avoid being caught. Logs, network noise, and artifacts must be minimized. |
| **C2 (Command and Control)** | The communication channel between compromised hosts and the attacker. |

---

## 🧰 Tools Cheat Sheet (with Purpose)

| Category | Top Tools | Why They're Used |
|---------|-----------|------------------|
| **Reconnaissance** | Nmap, Shodan, Amass, Maltego, theHarvester | Discover external attack surface, exposed services, and metadata. |
| **Initial Access** | Metasploit, Evilginx, Phishing Frameworks (GoPhish), Cobalt Strike | Exploit CVEs, deliver payloads, or bypass MFA. |
| **Privilege Escalation** | LinPEAS, WinPEAS, PowerUp, Seatbelt | Find misconfigs or vulnerable services to gain SYSTEM/admin. |
| **Lateral Movement** | BloodHound, CrackMapExec, PsExec, Rubeus | Move inside networks by abusing protocols like SMB, LDAP. |
| **Persistence** | Scheduled Tasks, Run Keys, DLL Hijacking, WMI, Registry | Maintain stealthy access even after reboots. |
| **Exfiltration** | Rclone, DNSCat2, ICMP tunneling, Stego | Extract sensitive data without triggering alarms. |

> 🧠 Always pair tools with **OPSEC** techniques like encryption, port forwarding, traffic obfuscation, and log evasion.

---

## 📜 Engagement Phases (With Examples)

### 1. **Planning & Rules of Engagement**
- Define:
  - Scope (IP ranges, allowed attack vectors)
  - Success criteria (domain admin? data exfil?)
  - Legal approvals
  - Reporting timelines

> Example: Can we phish the CEO? Can we break into the building?

---

### 2. **Reconnaissance**
- **Passive**: Google Dorking, LinkedIn, WHOIS, Pastebin, GitHub scraping
- **Active**: Port scanning, subdomain bruteforce, ASN enumeration

> Goal: Map targets and identify entry points.

---

### 3. **Weaponization**
- Craft payloads (e.g., `msfvenom`, `donut`, `SharpLoader`)
- Set up **C2 infrastructure** (Cobalt Strike, Sliver, Mythic)

> Use domain fronting, redirectors (e.g., Apache mod_rewrite) for stealth

---

### 4. **Delivery & Exploitation**
- **Phishing emails**, browser exploits, USB drops
- Exploit web apps (RCE, SQLi, SSRF)
- MFA Bypass (e.g., Evilginx, AitM)

---

### 5. **Post-Exploitation**
- **Credential Dumping**: Mimikatz, LSASS memory
- **Privilege Escalation**: Kernel exploits, misconfigured services
- **Enumeration**: Find shares, trust paths, access tokens

---

### 6. **Lateral Movement**
- Pass-the-Hash / Pass-the-Ticket
- Overpass-the-Hash with Rubeus
- Abuse AD misconfigurations

---

### 7. **Persistence & Evasion**
- Hidden scheduled tasks
- DLL side-loading
- Registry keys
- Userland rootkits

---

### 8. **Reporting**
- Technical report + Executive summary
- Include detection gaps, attacker timeline, and **defense recommendations**

---

## ⚔️ Red Team Frameworks & Methodologies

- **MITRE ATT&CK**: Public TTP knowledge base (crucial for mapping behavior)
- **Cyber Kill Chain**: 7-stage intrusion model by Lockheed Martin
- **PTES**: Penetration Testing Execution Standard
- **NIST 800-115**: Security testing guide
- **TIBER-EU**: Threat Intelligence-Based Ethical Red Teaming (used in EU banks)

---

## 🕵️‍♀️ OSINT Pro Tips

- `site:linkedin.com "company name"` to find employees
- Use **Hunter.io** for email formats
- Search GitHub for leaked creds:  
  `password filename:.env`
- Check breaches with **HaveIBeenPwned**
- Use **Spiderfoot** for automated recon

---

## 🎭 Social Engineering (With Scenarios)

| Method | Description | Example |
|--------|-------------|---------|
| Pretexting | Impersonate trusted role | “Hi, I’m from IT, I need your password to fix your VPN.” |
| Phishing | Malicious email with link or attachment | Fake invoice with macro payload |
| Vishing | Voice-based phishing | Calling helpdesk for password reset |
| Baiting | Leave infected USB labeled “HR Salaries” | Triggers payload once inserted |

---

## 🧪 Practical Labs & Where to Train

| Category | Platform | Notes |
|---------|----------|-------|
| Basics | TryHackMe, Hack The Box | Start with Red Team Path (THM) or HTB Starting Point |
| Advanced C2 | Sliver, Mythic, Brute Ratel | Cobalt Strike trial is limited, but others are FOSS |
| AD & Lateral Movement | HTB Enterprise, DetectionLab | Practice BloodHound, Rubeus, PowerView |
| Payloads | Obfuscation, AMSI Bypass labs | Use `Invoke-Obfuscation`, `Nim`, `Donut` |

---

## 📚 Learn Like a Beast

### 📘 Must-Read Books:
- *Red Team Field Manual*
- *The Hacker Playbook 3*
- *Advanced Red Teaming* – Joe Vest
- *Adversarial Tradecraft in Cybersecurity* – Dan Borges

### 🎥 YouTube Channels:
- **IppSec** – Best walkthroughs (HTB)
- **TCM Security** – Practical explanations
- **InsiderPhD** – For OSCP + beyond

### 📦 GitHub Repos:
- `lolbas-project` – Living off the land binaries
- `GTFOBins` – Unix equivalent
- `PayloadsAllTheThings` – God-tier resource

---

## 🥷 Top Red Team Certifications (with 💸 status)

| Certification | Focus | Cost | Notes |
|---------------|-------|------|-------|
| **Red Team Ops I (RTO1)** | C2, AD, evasion | 💸 Paid | Pure red team skill |
| **CRTO** | Cobalt Strike & ops | 💸 Paid | Widely respected |
| **PNPT** | Full pentest + report | 💸 Paid | Includes social engineering |
| **THM Red Team Room** | Intro | ✅ Free | Great start |
| **HTB Intro to Offensive Sec** | Basics | ✅ Free | Good warmup |
| **Practical Ethical Hacking** | Full beginner course | ✅ Often Free | TCM Security |

---

## 📑 Personal Red Team Diary

> Use this space to document your growth:
- 🔹 Tools mastered
- 🔹 Labs completed
- 🔹 TTPs learned
- 🔹 Bypasses found
- 🔹 What you’d do differently next time
- 🔹 Detection logs you generated

---

> 💬 **Pro Tip:** Always approach Red Teaming with discipline, stealth, and documentation. A loud Red Teamer is a failed Red Teamer.
