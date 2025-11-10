# Implementing Risk-Management Strategies for a Call Center Security
<img width="2048" height="1127" alt="image" src="https://github.com/user-attachments/assets/73c4c696-52b4-4a11-8cf0-3ac62e46999b" />

# Introduction 
 This project focuses on implementing robust security protocols for a call center. This includes conducting a detailed risk assessment to identify potential threats to the center’s operations, data protection and customer interactions.

---
# Problem Statement
Call centers handle sensitive customer and business information, making them targets for security threats such as unauthorised access, data breaches and system failures. Currently, there is no comprehensive framework in place to safeguard data and ensure secure operations. This exposes the organisation to risks including data loss, reputational damage, operational downtime and regulatory non-compliance. Emerging threats, remote work setups and third-party integrations further increase the center’s vulnerability. A structured risk assessment is needed to identify, analyse and prioritise these risks effectively. The findings will guide the implementation of strong security protocols to protect customer data, ensure compliance and maintain business continuity.

# Objectives
The goal of this project is to help the client prioritise and implement strong security protocols for their organisation’s call center operation by identifying potential threats that may disrupt the call center’s operations, analysing identified risks and evaluating the approach to manage them methodically.

---
# Tasks
1. **Perform a Risk Assessment:**
- Identify potential threats that may disrupt the call center’s operations, such as unauthorised access to customer information, system failures, or regulatory compliance issues.
- Analyse the identified risks by assessing their likelihood and potential impact on business operations.
- Prioritise the risks by evaluating their severity to determine which require immediate attention.
- Identify the assets that need to be protected. This could include sensitive information, customer data, financial information or any other critical assets important to the client.

2. **Prepare a Risk Treatment Plan Request:**
- Based on the assessment, a formal request for risk treatment would be created and directed to the appropriate departments (e.g., IT, HR, Operations).
- Include clear recommendations for reducing or eliminating the identified risks, such as introducing new security measures, revising policies, or training staff.

3. **Prepare Risk Assessment Report**
 - Create a comprehensive document that details the identified risks, their likelihood and their potential impact on the call center.
- Create a formal request outlining proposed actions to mitigate the risks, tailored for the relevant departments to implement.

### 1.0 Assets Register
<img width="1786" height="693" alt="image" src="https://github.com/user-attachments/assets/697cbe14-cafb-45b3-988c-8d61a1c2af39" />
Asset ID	Asset Name	Category	Description	Asset Owner	Asset Location	Confidentiality Rating	Integrity Rating	Availability Rating
1	Workstations (Computers)	Hardware	Computers used by call center employees to handle calls.	Operations Dept.	Call Centre Floor	Medium	Medium	High
2	Telephony Systems (PBX, VoIP Phones)	Hardware	Phone systems used for handling customer calls and internal communications.	IT Department	Call Centre Floor	Medium	High	High
3	Servers (Database, Web, Application)	Hardware	Servers hosting databases, web services, and business applications.	IT Department	Data Center	High	High	High
4	Network Devices (Routers, Switches, Firewalls)	Hardware	Routers, switches and firewalls used in call center operations.	IT Department	Call Center Premises	High	High	High
5	Mobile Devices (Tablets, Smartphones)	Hardware	Mobile devices used by supervisors and field agents for remote operations.	IT Department	Office & Remote	Medium	Medium	Medium
6	Printers, Scanners, Fax Machines	Hardware	Office equipment used for document handling and information exchange.	Facilities Dept.	Office Floor	Low	Medium	Medium
7	Power Backup Systems (UPS, Generators)	Hardware	Systems providing backup power during outages.	Facilities Dept.	Building Utility Room	Low	High	High
8	Customer Relationship Management (CRM) Systems	System	Customer Relationship Management software used to track cases.	IT Department	Cloud	Critical	High	High
9	Call Management Systems(Call Centre Software)	System	Software used for handling customer calls and managing tickets.	IT Department	Data Center	High	High	High
10	Workforce Management Systems	System	Applications for scheduling, attendance, and performance monitoring.	HR Department	Cloud	Medium	Medium	High
11	Email Systems	System	Platforms for internal and external business communication.	IT Department	Cloud/Internal Network	High	High	High
12	Monitoring and Logging Systems	System	Tools for tracking system health, security events, and performance.	IT Security Dept.	Data Center	High	High	Medium
13	Operating Systems (Windows, Linux)	Software	Core software managing hardware and application execution.	IT Department	All Devices	High	High	High
14	Anti-virus and Anti-malware Software	Software	Software protecting systems from malicious threats.	IT Security Dept.	All Devices	High	High	High
15	Office Productivity Software	Software	Tools like MS Office or Google Workspace for daily tasks.	IT Department	All Devices	Medium	Medium	High
16	Call Recording System	Software	System for recording and storing customer calls for compliance.	IT Department	Internal Network	High	Medium	Medium
17	Custom Business Applications	Software	In-house developed tools tailored for specific business operations.	IT Department	Internal Network	High	High	Medium
18	Database Management Systems	Software	Systems used to manage, store, and retrieve data efficiently.	IT Department	Data Center	High	High	High
19	Call Handlers / Agents	People	Employees responsible for handling inbound/outbound customer calls.	Operations Dept.	Office Floor	Medium	Medium	High
20	Supervisors	People	Staff overseeing call agents and ensuring service quality.	Operations Dept.	Office Floor	Medium	Medium	High
21	IT Support Staff / System Administrators	People	Personnel responsible for managing and maintaining IT systems.	IT Department	Office & Remote	High	High	High
22	Physical Security System	Physical	CCTV and access control systems for securing the call center.	Security Dept.	Call Center Premises	Medium	Medium	High
23	Employee Credentials	Information	Employee usernames and passwords for accessing systems.	HR Department	Internal Network	Critical	High	High
24	Backup Systema	Hardware	Systems used to back up critical call center data and operations.	IT Department	Data Center	High	High	High
25	Compliance Documentation	Information	Documents ensuring regulatory compliance (e.g., GDPR, PCI DSS).	Legal Dept.	Cloud/Internal Network	Critical	High	Medium
26	Employee Training Records	Information	Records of employee training related to security and compliance.	HR Department	Internal Network	Medium	Medium	Medium
<img width="2238" height="883" alt="image" src="https://github.com/user-attachments/assets/b6c978b7-6eae-4ee4-bd35-6533c900a9d9" />


---
## 2. Colour Coding Legend
<img width="682" height="135" alt="Colour Coding Legend" src="https://github.com/user-attachments/assets/4b5a5e56-06c8-41a9-b163-cc41d73253ae" />

Risk Score (R) is calculated as $L \times I$. Risk tolerance dictates that scores of 15-25 (Red) are Intolerable and require immediate treatment.

### 3. Comprehensive Risk Register Summary
The following table summarises all identified risks, their scores, and their potential impact on call centre operations, regulatory compliance, and business continuity.
<img width="1828" height="776" alt="image" src="https://github.com/user-attachments/assets/4cc2f0d0-5966-492c-9b51-6cb5f9d4bbc8" />
<img width="1834" height="786" alt="image" src="https://github.com/user-attachments/assets/a574fb2a-c087-4601-9562-a869ba43605a" />
<img width="1830" height="606" alt="image" src="https://github.com/user-attachments/assets/55906fcc-5ac6-409c-ae09-d10559b1c717" />

### 4. Formal Request for High-Priority Risk Treatment (Score >=16)

**TO: Head of IT Infrastructure, Head of Human Resources (HR), Head of Call Centre Operations**

**FROM: [Your Name/GRC Department]**

**SUBJECT: URGENT ACTION REQUIRED: Treatment of Extreme Risks (Score>=16)**

This section formally communicates the two Extreme Risks that require immediate, prioritized, and funded treatment plans. The departments listed below are mandated to collaborate to reduce the residual risk score for these items to a score of 8 (High) or lower within the next 6 months.
<img width="1484" height="557" alt="image" src="https://github.com/user-attachments/assets/a004e03c-6148-4e07-ada5-0f05d3366c34" />
<img width="837" height="310" alt="image" src="https://github.com/user-attachments/assets/473c8245-1e02-4481-be86-dd832037bf35" />

**Next Steps:**

Departmental Heads are required to acknowledge receipt of this request and provide an initial progress update to the GRC function within 14 days. 

Thanks
