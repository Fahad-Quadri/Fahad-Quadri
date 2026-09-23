<!-- Header -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0f3d3e,100:00c896&height=190&section=header&text=Syed%20Fahad%20Quadri&fontSize=46&fontColor=e6edf3&fontAlignY=36&desc=Security%20Analyst%20%7C%20SOC%20%7C%20Detection%20and%20Response&descSize=17&descAlignY=58&descColor=9be9d8" alt="Syed Fahad Quadri — Security Analyst" />
</p>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&duration=2800&pause=900&color=00C896&center=true&vCenter=true&width=640&lines=%24+whoami+%E2%86%92+SOC+%2F+Blue+Team+Analyst;Triaging+40-50%2B+Splunk+SIEM+alerts+a+day;Phishing+%26+BEC+investigation+%7C+IR+documentation;Nessus+%E2%80%A2+OpenVAS+%E2%80%A2+Wireshark+%E2%80%A2+Nmap+%E2%80%A2+pfSense;Building+labs%3A+pfSense+%2B+Kali+%2B+Active+Directory" alt="Typing intro" />
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/syed-fahad-quadri-8a796a3a8/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://fahad-quadri.github.io/"><img src="https://img.shields.io/badge/Portfolio-00C896?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio" /></a>
  <a href="mailto:syedfahadquadri09@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://img.shields.io/badge/Kansas%20City%2C%20MO-Open%20to%20Relocation-30363d?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location" />
</p>

---

### `> cat about.txt`

```yaml
analyst:
  name:      Syed Fahad Quadri
  role:      Security Analyst — SOC / Incident Response / Vulnerability Management
  based_in:  Kansas City, MO (open to relocation)
  focus:     [alert triage, phishing & BEC investigation, vuln assessment, packet analysis]
  sectors:   [healthcare (HIPAA), multi-tenant client environments]
  education: M.S. Cybersecurity Management — Lindsey Wilson University
  certs:
    - Google Cybersecurity Professional Certificate  # completed
    - CompTIA Security+                              # exam scheduled Sep 2026
  status:    open to SOC Analyst / Security Analyst roles
```

---

### 📈 Impact at a Glance

<table align="center">
  <tr>
    <td align="center" width="25%"><h2>50+</h2><sub>Splunk SIEM alerts<br/>triaged daily</sub></td>
    <td align="center" width="25%"><h2>150+</h2><sub>Windows &amp; Linux systems<br/>scanned (Nessus / OpenVAS)</sub></td>
    <td align="center" width="25%"><h2>25+</h2><sub>critical &amp; high-risk<br/>findings prioritized</sub></td>
    <td align="center" width="25%"><h2>8+</h2><sub>confirmed compromises<br/>escalated</sub></td>
  </tr>
</table>

---

### 🛡️ Experience & Education

| Role | Organization | Dates | Highlights |
|---|---|---|---|
| **SOC Analyst Intern** | Unify Decoders LLC | Jan 2026 – Aug 2026 | 40+ daily Splunk alerts with SOP-based triage · 60+ systems evaluated, 25+ critical/high findings prioritized · Wireshark/Nmap validation of IDS/IPS indicators, 8+ compromises escalated |
| 🎓 **M.S. Cybersecurity Management** | Lindsey Wilson University | Jan 2024 – Dec 2025 | Graduate study in cybersecurity management between the HHC Clinic role and the Unify Decoders internship |
| **Security Analyst** | HHC Clinic | Aug 2022 – Nov 2023 | 50+ daily SIEM alerts in healthcare · phishing & BEC investigation with audit-ready evidence · 150+ systems scanned for HIPAA readiness · PCI DSS / ISO policy documentation |
| **Cybersecurity Intern** | AICTE | Jan 2022 – Jun 2022 | Hybrid Azure / AWS / GCP configuration · segmentation, identity controls & logging · change-control docs with Terraform & PowerShell |

---

### 🔬 Featured Lab — [Home-lab-network-security](https://github.com/Fahad-Quadri/Home-lab-network-security)

> A virtualized enterprise-in-a-box: firewall, attacker, Linux client and an Active Directory domain — every build step, failure, and root cause documented with screenshots.

```mermaid
flowchart LR
    NET((Internet)) ---|WAN / NAT| FW
    subgraph LAB["labnet · 192.168.1.0/24"]
        FW["🧱 pfSense CE 2.7.2<br/>Router / Firewall · .1<br/>ICMP block rule · Suricata IDS"]
        KALI["🐉 Kali Linux 2026.2<br/>Attacker / Recon · .101"]
        UBU["🐧 Ubuntu Server<br/>Domain-joined client · .100"]
        DC["🪟 Windows Server 2025 Core<br/>AD DS + DNS · fahadlab.local · .102"]
    end
    FW --- UBU
    FW --- KALI
    FW --- DC
    KALI -. "nmap -sn / -sV" .-> UBU
    UBU == "realmd / SSSD / Kerberos" ==> DC
```

| What I built | What I troubleshot |
|---|---|
| pfSense router/firewall with isolated LAN segment and verified NAT routing | VT-x capture by Windows VBS/Memory Integrity, APIC panic, ZFS pager-read boot loop |
| LAN ICMP-block rule, verified with before/after ping tests | Suricata `ipfw` divert-socket failure — 4 start paths tested, root-caused to the VM NIC |
| Kali recon: host discovery + service/version scans | `.local` DNS resolution quirk in `systemd-resolved` blocking `realm discover` |
| Windows Server 2025 DC via PowerShell (`Install-ADDSForest`) | Kerberos preauthentication failure during the Linux domain join |

---

### 🗂️ More Projects

<table>
  <tr>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/Fahad-Quadri/ioc-extractor">🔎 ioc-extractor</a></h4>
      Python CLI that pulls IPs, domains, URLs, emails, hashes and CVEs out of phishing emails and SIEM alerts, refangs/defangs, exports CSV/JSON for Splunk lookups.<br/><br/>
      <code>Python</code> <code>unit-tested</code> <code>GitHub Actions</code>
    </td>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/Fahad-Quadri/splunk-detection-library">📡 splunk-detection-library</a></h4>
      8 SPL detections (brute force, password spraying, encoded PowerShell, log clearing, DNS tunneling…) mapped to MITRE ATT&amp;CK, each with tuning and triage steps.<br/><br/>
      <code>Splunk SPL</code> <code>Sysmon</code> <code>ATT&amp;CK</code>
    </td>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/Fahad-Quadri/phishing-analysis-playbook">🎣 phishing-analysis-playbook</a></h4>
      End-to-end phishing &amp; BEC investigation method: evidence handling, SPF/DKIM/DMARC header analysis, scoping, containment, and an incident report template.<br/><br/>
      <code>IR</code> <code>BEC</code> <code>HIPAA-aware</code>
    </td>
  </tr>
</table>

---

### 🧰 Toolkit

**SIEM · EDR · Detection**
<p>
  <img src="https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white" />
  <img src="https://img.shields.io/badge/Microsoft%20Sentinel-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/CrowdStrike-E01F3D?style=flat-square&logo=crowdstrike&logoColor=white" />
  <img src="https://img.shields.io/badge/SentinelOne-6B2FBA?style=flat-square&logo=sentinelone&logoColor=white" />
  <img src="https://img.shields.io/badge/Elastic-005571?style=flat-square&logo=elastic&logoColor=white" />
  <img src="https://img.shields.io/badge/Cortex%20XDR-FA582D?style=flat-square&logo=paloaltonetworks&logoColor=white" />
  <img src="https://img.shields.io/badge/MITRE%20ATT%26CK-C0392B?style=flat-square&logoColor=white" />
</p>

**Network & Vulnerability**
<p>
  <img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
  <img src="https://img.shields.io/badge/Nmap-4682B4?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Nessus-00C176?style=flat-square&logo=tenable&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenVAS-66C430?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/pfSense-212121?style=flat-square&logo=pfsense&logoColor=white" />
  <img src="https://img.shields.io/badge/Suricata-EF8B00?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Hack%20The%20Box-111927?style=flat-square&logo=hackthebox&logoColor=9FEF00" />
</p>

**Cloud · Systems · Identity**
<p>
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Active%20Directory-0078D4?style=flat-square&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Windows%20Server-0078D6?style=flat-square&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white" />
</p>

**Scripting**
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white" />
</p>

**Governance & Compliance** &nbsp;·&nbsp; `HIPAA` `PCI DSS` `ISO` `CIS Controls` `Security Policy` `Incident Documentation`

---

### 🎯 Currently

- 📘 Preparing for **CompTIA Security+** (exam scheduled September 2026)
- 🧪 Extending the home lab — next up: getting an IDS sensor running on a different virtual NIC / hypervisor, and alternatives like Snort
- 🔎 Practicing attacker TTPs mapped to **MITRE ATT&CK** on Hack The Box
- 💼 Open to **SOC Analyst / Security Analyst** roles — happy to relocate

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00c896,50:0f3d3e,100:0d1117&height=110&section=footer" alt="" />
</p>
