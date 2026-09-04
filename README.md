# Active-Directory-Gap-Analysis

Summary

	This repository contains a comprehensive NIST SP 800-53 Rev. 5 Security Assessment and Plan of Action and Milestones (POA&M) for a newly deployed Active 		Directory Domain Controller baseline. Utilizing PingCastle: an open-source auditing tool, and Microsoft Policy Analyzer: a group policy evaluation app, the 	goal of this project is to identify configuration gaps, evaluate system risk against compliance baselines, and deliver an actionable, operational remediation 	roadmap.






Deliverables

	Executive Summary.pdf --> Project overview

	AD_Assessment_Workbook.xlsx
  		Dashboard --> High-level visuals, legends
  		Gap Analysis Matrix --> Current vs. desired state, framework mapping, risk scores
  		POA&M --> Chronological Remediation
  		Policy Analyzer Scan --> Raw GPO Comparison Data
  
	artifacts/ --> Sanitized visual artifacts
  		PingCastle_LAB-ENV.html
  		Wauh_agent_endpoints.png
  		TaskSchedule_PingCastle.png
  		TaskSchedule_LifecycleAutomation.png
  





Scope and Gap Mapping

	The target system for this project was a Windows Server Active Directory Domain Controller (LAB-ENV.LOCAL), within the fake organization Lab-Env Inc. 			Configuration gaps were assessed against the NIST 800-53 Rev. 5.
  





Tools Used for Assessment and Evidence Collection

	PingCastle was used for the initial security posture assessment. Along with overall risk, the tool isolated key misconfigurations, the risks associated with       them, supporting documentation, and remediation recommendations. Microsoft Policy Analyzer was used to directly compare the domain Group Policy Objects   		(GPOs) with an established baseline (downloaded via Microsoft Security Compliance Toolkit 1.0).






Scoring the Risk

	The risk of each control was qualitatively scored based on a standard 3x3 Risk Assessment Matrix, with risk scores ranging from Low to Critical. Each 			likelihood and impact level were scored as follows:

	Likelihood:
	Low – Rare conditions needed to exploit the vulnerability
	Medium – Requires a compromised account, elevated access, or complex conditions to exploit the vulnerability
	High – Known scripts/documentation are available and/or standard domain users are vulnerable
	
	Impact:
	Low – Minimal privilege escalation, minor data/information disclosure
	Medium – Partial network access, lateral movement, etc.
	High – Domain takeover, sensitive data exposed, system downtime






Remediation

	The POA&M was separated into two sections: Immediate Fixes and Continuous Monitoring/Management. Immediate Fixes will be fully deployed in 1 week, while the 	long-term changes will be fully deployed in 5-6 weeks. By implementing both immediate and continuous security posture improvements, we will drastically reduce 	system risk, establish a truly secure baseline, and maintain a NIST 800-53 Rev. 5 compliant identity environment.



  
  
  

