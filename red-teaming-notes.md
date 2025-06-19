# 🛡️ Red Teaming Notes

## 📌 What Is Red Teaming?
Red Teaming is a **full-scope simulated cyberattack** on an organization, designed to **test defenses** under realistic conditions. It includes **social engineering**, **physical breaches**, and **strategic deception**.

> ✅ **Goal**: Emulate real-world attackers (APT, insiders, hacktivists) to identify **detection and response gaps** — not just vulnerabilities.

---

## 🧠 Key Concepts

| Term | Description |
|------|-------------|
| **Red Team** | Simulates real-world adversaries and advanced threat actors. |
| **Blue Team** | Defenders responsible for monitoring, detection, and response. |
| **Purple Team** | Collaboration of Red + Blue to improve defenses. |
| **TTPs** | Tactics, Techniques, and Procedures — adversary behavior. |
| **OPSEC** | Operational Security — hide your tracks, avoid detection. |
| **C2 (Command and Control)** | Communication between attacker and compromised host. |

---

## 🧰 Tools Cheat Sheet

| Category | Tools | Why They're Used |
|---------|-------|------------------|
| Reconnaissance | Nmap, Shodan, Amass, Maltego | Discover attack surface and metadata |
| Initial Access | Metasploit, Evilginx, GoPhish | Deliver payloads, bypass MFA |
| Priv Esc | LinPEAS, WinPEAS, Seatbelt | Find ways to escalate to admin |
| Lateral Movement | BloodHound, PsExec, Rubeus | Move across the network |
| Persistence | Registry keys, WMI, DLL hijack | Stay hidden and maintain access |
| Exfiltration | DNS tunneling, Rclone, Stego | Exfil data covertly |

---

## 📜 Red Team Engagement Phases

1. **Planning & Scoping**
   - Define ROE, objectives, and legal permissions
2. **Reconnaissance**
   - Passive (OSINT) & active (port scans, fingerprinting)
3. **Weaponization**
   - Payload crafting, C2 setup
4. **Delivery & Exploitation**
   - Phishing, CVE exploitation, USB drops
5. **Post-Exploitation**
   - Credential dumping, lateral movement
6. **Persistence & Evasion**
   - Backdoors, obfuscation, log cleaning
7. **Reporting**
   - Technical + executive reports with remediation advice

---

## ⚔️ Red Team Frameworks & Standards

- **MITRE ATT&CK**: Adversary TTP matrix
- **Cyber Kill Chain**: Lockheed Martin's 7-stage attack model
- **PTES**: Penetration Testing Execution Standard
- **NIST 800-115**: Official technical security testing guide
- **TIBER-EU**: Threat Intelligence-Based Ethical Red Teaming

---

## 🕵️‍♀️ OSINT Tips

- Google Dorking: `site:linkedin.com "Company"`  
- Subdomain enum: `Amass`, `Sublist3r`  
- Credential leaks: HaveIBeenPwned, GitHub search  
- Email formats: Hunter.io  
- Auto-recon: Spiderfoot

---

## 🎭 Social Engineering Scenarios

| Method | Description | Example |
|--------|-------------|---------|
| Pretexting | Impersonate a role | "I'm IT support, need VPN creds." |
| Phishing | Email with malicious payload | Macro Excel file |
| Vishing | Phone-based phishing | Call to reset password |
| Baiting | Drop infected USBs | "HR Salary Report" USB in hallway |

---

## 🧪 Practical Labs

| Category | Platform | Purpose |
|---------|----------|---------|
| Vuln Machines | TryHackMe, HTB, VulnHub | Realistic targets |
| AD Labs | DetectionLab, HTB Enterprise | Learn AD attacks |
| C2 Practice | Mythic, Sliver, Brute Ratel | Learn evasion & control |
| AMSI Bypass | Invoke-Obfuscation, Nim | Craft stealthy payloads |

---

## 📚 Resources to Learn Like a Beast

### Books
- *Red Team Field Manual*
- *The Hacker Playbook 3*
- *Advanced Red Teaming* – Joe Vest

### YouTube
- IppSec – HTB walkthroughs
- TCM Security – Training
- InsiderPhD – OSCP prep

### GitHub Repos
- `lolbas-project` – Living off the Land Windows binaries
- `GTFOBins` – Linux privesc tools
- `PayloadsAllTheThings` – Post-exploit arsenal

---

## 🎯 Certifications Path

| Certification | Focus | Cost |
|---------------|-------|------|
| **RTO1** | C2, AD, red ops | 💸 Paid |
| **CRTO** | Cobalt Strike ops | 💸 Paid |
| **PNPT** | Full-scope pentesting | 💸 Paid |
| **TryHackMe Red Team Room** | Intro | ✅ Free |
| **HTB Intro to Offensive Sec** | Basics | ✅ Free |
| **TCM Practical Ethical Hacking** | Beginner | ✅ Often Free |

---

## 📑 Personal Red Team Diary

Use this space to track:
- ✅ Labs completed
- ✅ Payloads crafted
- ✅ TTPs learned
- ✅ Mistakes made & how you improved
- ✅ C2 profiles tested
- ✅ Detection logs observed

---

> 💬 **Pro Tip**: A loud Red Teamer is a failed Red Teamer. Stealth, logs, and OPSEC are everything.
