# Active-Directory-Gap-Analysis

## Summary

This repository contains a comprehensive NIST SP 800-53 Rev. 5 Security Assessment and Plan of Action and Milestones (POA&M) for a newly deployed Active Directory Domain Controller baseline. Utilizing PingCastle: an open-source auditing tool, and Microsoft Policy Analyzer: a group policy evaluation app, the goal of this project is to identify configuration gaps, evaluate system risk against compliance baselines, and deliver an actionable, operational remediation roadmap.






## Deliverables
- [Executive Summary (PDF)](https://github.com/DLegit03/Active-Directory-Gap-Analysis/raw/main/Executive_Summary.pdf) — Project overview
- [AD Assessment Workbook (XLSX)](https://github.com/DLegit03/Active-Directory-Gap-Analysis/raw/main/AD_Assessment_Workbook.xlsx)
  - **Dashboard** — High-level visuals, legends
  - **Gap Analysis Matrix** — Current vs. desired state, framework mapping, risk scores
  - **POA&M** — Granular, chronological remediation
  - **Policy Analyzer Scan** — Raw GPO Comparison Data



<img width="900" height="650" alt="Sample_Matrix" src="https://github.com/user-attachments/assets/4432d355-21f2-4414-b7a1-b30f3bdce8a3" />

*Sample data from Gap Analysis Matrix*


## Artifacts
- [PingCastle Assessment (HTML)](./evidence/PingCastle_LAB-ENV.html)
- [Wazuh Agent Endpoints (PNG)](./evidence/Wazuh_agent_endpoints.png)
- [Task Schedule (PNG)](./evidence/TaskSchedule.png)


  <img width="900" height="650" alt="Screenshot 2026-09-05 150748" src="https://github.com/user-attachments/assets/c101122f-5edb-4f46-9602-cc9695d8270d" />

*Sample data from PingCastle scan*


## Scope

The target system for this project is a Windows Server Active Directory Domain Controller (LAB-ENV.LOCAL), within the fake organization Lab-Env Inc. The server is being ran within a ProxMox virtual environment on-premises.

<img width="600" height="450" alt="Screenshot 2026-09-05 151507" src="https://github.com/user-attachments/assets/ceb31741-eac8-4109-b69b-834d26da2cb9" />

*Home Lab topology*  

## Key Findings
- NTLMv1 authentication protocol left enabled
- Lack of user lifecycle automation/governance
- Lack of domain audit visibility
- Several Group Policy Objects contain conflicting policy



## Tools Used for Assessment and Evidence Collection

PingCastle was used for the initial security posture assessment. Along with overall risk, the tool isolated key misconfigurations, the risks associated with them, supporting documentation, and remediation recommendations. Microsoft Policy Analyzer was used to directly compare the domain Group Policy Objects (GPOs) with an established baseline (downloaded via Microsoft Security Compliance Toolkit 1.0). Active Directory Domain Services, Group Policy Management, and Wazuh were also used. 

#### Frameworks
- NIST CSF 2.0
- NIST SP 800-53 Rev. 5








## Scoring the Risk

The risk of each control is qualitatively scored based on a standard 3x3 Risk Assessment Matrix, with risk scores ranging from Low to Critical. Each likelihood and impact level were scored as follows:

#### Likelihood:
Low – Rare conditions needed to exploit the vulnerability
Medium – Requires a compromised account, elevated access, or complex conditions to exploit the vulnerability
High – Known scripts/documentation are available and/or standard domain users are vulnerable
	
#### Impact:
Low – Minimal privilege escalation, minor data/information disclosure
Medium – Partial network access, lateral movement, etc.
High – Domain takeover, sensitive data exposed, system downtime






## Remediation

The POA&M is separated into two sections: Immediate Fixes and Continuous Monitoring/Management. Immediate Fixes will be fully deployed in 1 week, while the long-term changes will be fully deployed in 5-6 weeks. By implementing both immediate and continuous security posture improvements, we will drastically reduce system risk, establish a truly secure baseline, and maintain a NIST 800-53 Rev. 5 compliant identity environment.

  
  
  

