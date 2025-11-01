# Implementing Risk-Management Strategies for a Call Center Security
<img width="2048" height="1127" alt="image" src="https://github.com/user-attachments/assets/73c4c696-52b4-4a11-8cf0-3ac62e46999b" />

# Introduction 
In this project, we simulate the implementation of strong security protocols for your organisation’s call center operations. This requires conducting a detailed risk assessment to identify potential threats to the center’s operations, data protection and customer interactions.

---
# Problem Statement
The client has a fence around the perimeter of its property and a padlock on its entrance gate to prevent unauthorised access. However, the leadership team is concerned about potential risks and vulnerabilities that could compromise the security of its information and systems. They require a comprehensive risk assessment to identify potential security threats and vulnerabilities in their system or network.

# Objectives
- Tenable (enterprise vulnerability management platform)
- Azure Virtual Machines (Nessus scan engine + scan targets)
- PowerShell & BASH (remediation scripts)

---
# Tasks

- Identify the assets that need to be protected. This could include sensitive information, customer data, financial information or any other critical assets that are important to the client.
- Define the likelihood, consequence and risk rating for each potential risk scenario (Define the risk matrix).
- Identify specific risks that the client needs to protect their assets from. i.e, cyberattack, natural disaster or employee negligence.
- Assess risk rating for each risk scenario – Calculate the inherent risk rating for each scenario, assuming there are no measures in place to reduce the risk (without fence and padlock in place).
- Assess risk levels for each risk scenario with additional measures:**
- Create a risk assessment report for the client that summarises the risk assessment findings**

---

### Identification of Critical Assets

This phase focuses on drafting a Vulnerability Management Policy as a starting point for stakeholder engagement and collaboration. The initial draft outlines scope, responsibilities and remediation timelines. It may be adjusted based on feedback from relevant departments to ensure practical implementation before final approval by upper management.  
[Draft Policy](https://docs.google.com/document/d/1j4WyDX3NXpOiAb-_8i-t_xvLJj5v0F6W/edit)
Based on the problem statement, the following critical assets were identified as requiring protection. The compromise of these assets could lead to significant operational, financial, and reputational damage to the organisation.
- **Confidential Customer Data: Personal and sensitive information belonging to customers.**
- Sensitive Information: Intellectual property, internal communications, and strategic plans.**
- **Proprietary Business Information: Internal data that provides a competitive advantage.**
- **Financial Information: Company financial records, transaction data, and banking details.**
- **Intellectual Property: Patents, trade secrets, designs, and proprietary software.**
- Customer Data: Personally Identifiable Information (PII) and financial records.** 
- ** Physical Infrastructure & Equipment: Servers, network hardware, and other critical physical assets.**

---

### Step 2.  Mock Meeting: Policy Buy-In (Stakeholders)

In this phase, a meeting with the server team introduces the draft Vulnerability Management Policy and assesses their capability to meet remediation timelines. Feedback leads to adjustments, like extending the critical remediation window from 48 hours to one week, ensuring collaborative implementation.

---

### Step 3) Policy Finalisation and Senior Leadership Sign-Off

After gathering feedback from the server team, the policy is revised, addressing aggressive remediation timelines. With final approval from upper management, the policy now guides the program, ensuring compliance and reference for pushback resolution.  
[Finalised Policy](https://docs.google.com/document/d/1AcleFsAXVoNLtxuIsXn5eVjoDGvG3-Zh/edit?usp=sharing&ouid=117796789656080684771&rtpof=true&sd=true)


---

### Step 4) Mock Meeting: Initial Scan Permission (Server Team)

The team collaborates with the server team to initiate scheduled credential scans. A compromise is reached to scan a single server first, monitoring resource impact and using just-in-time Active Directory credentials for secure, controlled access.  

---

### Step 5) Initial Scan of Server Team Assets

In this phase, an insecure Windows Server is provisioned to simulate the server team's environment. After creating vulnerabilities, an authenticated scan is performed and the results are exported for future remediation steps.  

<img width="635" alt="image" src="https://github.com/user-attachments/assets/937cccbd-36bb-4445-97b9-e915085cda81" style="border: 2px solid black;">

[Scan 1 - Initial Scan](https://drive.google.com/file/d/1RBPVj_azKJMwmRZ8QILlb4hxIjQU3wQ7/view?usp=drive_link)




---

### Step 6) Vulnerability Assessment and Prioritisation

We assessed vulnerabilities and established a remediation prioritisation strategy based on ease of remediation and impact. The following priorities were set:

1. Third Party Software Removal (Wireshark)
2. Windows OS Secure Configuration (Protocols & Ciphers)
3. Windows OS Secure Configuration (Guest Account Group Membership)
4. Windows OS Updates

---

### Step 7) Distributing Remediations to Remediation Teams

The server team received remediation scripts and scan reports to address key vulnerabilities. This streamlined their efforts and prepared them for a follow-up review.  

<img width="635" alt="image" src="https://github.com/user-attachments/assets/bbf9478f-e1d1-4898-846e-b510ec8c6f72">

[Remediation Email](https://github.com/joshmadakor1/lognpacific-public/blob/main/misc/remediation-email.md)

---

### Step 8) Mock Meeting: Post-Initial Discovery Scan (Server Team)

The server team reviewed vulnerability scan results, identifying outdated software, insecure accounts and deprecated protocols. The remediation packages were prepared for submission to the Change Control Board (CAB). 

---

### Step 9) Mock CAB Meeting: Implementing Remediations

The Change Control Board (CAB) reviewed and approved the plan to remove insecure protocols and cipher suites. The plan included a rollback script and a tiered deployment approach.  

---
### Step 10 ) Remediation Effort

#### Remediation Round 1: Outdated Wireshark Removal

The server team used a PowerShell script to remove outdated Wireshark. A follow-up scan confirmed successful remediation.  
[Wireshark Removal Script](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/remediation-wireshark-uninstall.ps1)  

<img width="634" alt="image" src="https://github.com/user-attachments/assets/7b4f9ab2-d230-4458-ac0f-c0ff070ae79a">

[Scan 2 - Third Party Software Removal](https://drive.google.com/file/d/1UiwPPTtuSZKk02hiMyXf31pXUIeC5EWt/view?usp=drive_link)


#### Remediation Round 2: Insecure Protocols & Ciphers

The server team used PowerShell scripts to remediate insecure protocols and cipher suites. A follow-up scan verified successful remediation and the results were saved for reference.  
[PowerShell: Insecure Protocols Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-protocols.ps1)
[PowerShell: Insecure Ciphers Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-cipher-suites.ps1)

<img width="630" alt="image" src="https://github.com/user-attachments/assets/0e96120d-8ec9-4f76-8e42-79c752200010">

[Scan 3 - Ciphersuites and Protocols](https://drive.google.com/file/d/1Qc6-ezQvwReCGUZNtnva0kCZo_-zW-Sm/view?usp=drive_link)


#### Remediation Round 3: Guest Account Group Membership

The server team removed the guest account from the administrator group. A new scan confirmed remediation and the results were exported for comparison.  
[PowerShell: Guest Account Group Membership Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-guest-local-administrators.ps1)  

<img width="627" alt="image" src="https://github.com/user-attachments/assets/870a3eac-3398-44fe-91c0-96f3c2578df4">

[Scan 4 - Guest Account Group Removal](https://drive.google.com/file/d/1jVgikjfrV1YjOcL3QRT_oUB0Y82w22V7/view?usp=drive_link)


#### Remediation Round 4: Windows OS Updates

Windows updates were re-enabled and applied until the system was fully up to date. A final scan verified the changes  

<img width="627" alt="image" src="https://github.com/user-attachments/assets/870a3eac-3398-44fe-91c0-96f3c2578df4">

[Scan 5 - Post Windows Updates](https://drive.google.com/file/d/1tmDjeHl5uiGitRwWy8kFRi33q-nGi1Zt/view?usp=drive_link)

---

### First Cycle Remediation Effort Summary

The remediation process reduced total vulnerabilities by 80%, from 30 to 6. Critical vulnerabilities were resolved by the second scan (100%) and high vulnerabilities dropped by 90%. Mediums were reduced by 76%. In an actual production environment, asset criticality would further guide future remediation efforts.  

<img width="1920" alt="image" src="https://github.com/user-attachments/assets/51f0aae8-7f36-4d90-b29f-5257e57155f9">

[Remediation Data](https://docs.google.com/spreadsheets/d/1FTtFfZYmFsNLU6pm8nTzsKyKE-d2ftXzX_DPwcnFNfA/edit?gid=0#gid=0)

---

### On-going Vulnerability Management (Maintenance Mode)

After completing the initial remediation cycle, the vulnerability management program transitions into **Maintenance Mode**. This phase ensures that vulnerabilities continue to be managed proactively, keeping systems secure over time. Regular scans, continuous monitoring and timely remediation are crucial components of this phase. (See [Finalised Policy](https://docs.google.com/document/d/1AcleFsAXVoNLtxuIsXn5eVjoDGvG3-Zh/edit?usp=sharing&ouid=117796789656080684771&rtpof=true&sd=true) for scanning and remediation cadence requirements.)

Key activities in Maintenance Mode include:
- **Scheduled Vulnerability Scans**: Perform regular scans (e.g, weekly or monthly) to detect new vulnerabilities as systems evolve.
- **Patch Management**: Continuously apply security patches and updates, ensuring no critical vulnerabilities remain unpatched.
- **Remediation Follow-ups**: Address newly identified vulnerabilities promptly, prioritising based on risk and impact.
- **Policy Review and Updates**: Periodically review the Vulnerability Management Policy to ensure it aligns with the latest security best practices and organisational needs.
- **Audit and Compliance**: Conduct internal audits to ensure compliance with the vulnerability management policy and external regulations.
- **Ongoing Communication with Stakeholders**: Maintain open communication with teams responsible for remediation, ensuring efficient coordination.

By maintaining an active vulnerability management process, organisations can stay ahead of emerging threats and ensure long-term security resilience.
