# 🛡️ Red Teaming Notes

## 📌 Overview
Red Teaming is a simulated cyber attack designed to test and improve an organization's security by identifying vulnerabilities in systems, networks, or personnel.

> ✅ Goal: Think like an attacker to improve defenses.

---

## 🧠 Key Concepts

| Term | Definition |
|------|------------|
| **Red Team** | Offensive security professionals simulating attacks. |
| **Blue Team** | Defensive team responsible for detecting and stopping attacks. |
| **Purple Team** | A collaborative team combining Red and Blue teams. |
| **TTPs** | Tactics, Techniques, and Procedures used by adversaries. |
| **OPSEC** | Operational Security - Red teamers must hide their activities. |

---

## 🧰 Tools Cheat Sheet

| Category | Tools |
|---------|-------|
| Reconnaissance | Nmap, Shodan, Maltego, theHarvester |
| Exploitation | Metasploit, Cobalt Strike, SQLmap |
| Privilege Escalation | LinPEAS, WinPEAS, PowerUp |
| Lateral Movement | CrackMapExec, PsExec, BloodHound |
| Persistence | Scheduled Tasks, Registry Run Keys, WMI |
| Exfiltration | Rclone, DNS tunneling tools, custom scripts |

---

## 📜 Red Team Engagement Phases

1. **Planning and Scoping**
   - Define ROE (Rules of Engagement)
   - List authorized targets
   - Set timeline

2. **Reconnaissance**
   - Passive (OSINT)
   - Active (network scanning)

3. **Weaponization**
   - Create payloads
   - Prepare infrastructure (C2 servers)

4. **Exploitation**
   - Gain initial access (phishing, exploiting CVEs)

5. **Post-Exploitation**
   - Privilege escalation
   - Lateral movement
   - Data collection

6. **Persistence**
   - Maintain access without detection

7. **Reporting**
   - Document findings
   - Share remediation advice

---

## 📚 Must-Know Frameworks

- **MITRE ATT&CK** – Matrix of known adversary behaviors
- **Cyber Kill Chain** (Lockheed Martin)
- **NIST SP 800-115** – Technical Guide to Information Security Testing
- **PTES** – Penetration Testing Execution Standard

---

## 📓 OSINT Techniques

- Use **Google Dorking** for sensitive info
- Enumerate subdomains with `Sublist3r` or `Amass`
- Look up exposed credentials on **HaveIBeenPwned**
- Search employee info via LinkedIn (Maltego / recon-ng)

---

## 🕸️ Social Engineering Tips

- **Pretexting**: Impersonate IT staff
- **Phishing**: Malicious links or attachments
- **Vishing**: Voice phishing
- **Baiting**: Dropping infected USBs

> ⚠️ Always get explicit permission before attempting social engineering in engagements.

---

## 🧪 Lab Practice Ideas

| Lab Type | Platform |
|----------|----------|
| Vulnerable Machines | TryHackMe, Hack The Box, VulnHub |
| Windows Labs | DetectionLab, PurpleSharp |
| Active Directory | Hack The Box (Enterprise), AD labs |
| C2 Frameworks | Practice with Cobalt Strike (trial), Sliver, Mythic |

---

## 📖 Learning Resources

- **Books**:
  - *Red Team Field Manual*
  - *Advanced Penetration Testing* by Wil Allsopp
  - *The Hacker Playbook* series

- **YouTube**:
  - InsiderPhD
  - IppSec (HTB walkthroughs)
  - TCM Security

- **Courses**:
  - TCM Security’s *Practical Ethical Hacking*
  - Red Team Ops I & II by Zero-Point Security
  - Offensive Security’s OSCP / OSCE3 tracks

---

## 🎯 Certifications Path (Free + Paid)

| Cert | Type | Cost |
|------|------|------|
| **Red Team Ops I (RTO1)** | Red Teaming | Paid |
| **TCM PNPT** | Pentesting | Paid |
| **Hack The Box Red Teaming Path** | Red Teaming | Paid |
| **TryHackMe Red Team Room** | Intro Practice | Free |
| **Intro to Offensive Security – HTB** | Basics | Free |
| **Practical Ethical Hacking – TCM** | Pentesting | Sometimes Free |

---

## 📑 Personal Notes / Journal

> Use this section to document:
- Labs completed
- TTPs tested
- Payloads crafted
- Mistakes made & lessons learned
