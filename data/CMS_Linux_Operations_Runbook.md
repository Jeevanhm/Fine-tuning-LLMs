

**.**

**Document Control**

**Cloud Managed Service: Linux Runbook**

| Version | Status | Date | Author | Summary of Change |
| --- | --- | --- | --- | --- |
| V 1.1 | Initial Draft | 15th March 2022 | Kishore | Initial Draft |
| V 1.2 | Update | 25th Apr 2022 | Kishore | Content Update |
| V 1.3 | Update | 14th May 2022 | Taha Rashidi | Content Update |
| V 2.0 | Update | 28th June 2022 | Meghana/ Subhash | * Updated with MSHS screen shots * Steps to check Qualys agent status – Sec – 16.2 * Yum issues on the server – Sec – 16.18 * Steps for IP forwarding   Enable or Disable IP forwarding, Troubleshooting steps. – Sec – 16.17 |
| V2.1 | Update | 5th Sep, 2022 | Meghana/Subhash | * Updated with MSHS screen shots * Steps to check crowdstrike agent status – Sec – 12.8 * Linux server domain joining process – Sec – 15 * NTP server details – Sec –16.6 * Steps to Linux server Patching with Tag values – Sec – 20.10 * Azure Primary region updated – Sec – 9.5 * Hardening checks – Sec – 12.9 |
| V2.2 | Update | 10th Jan,2023 | Linux Team | * Document Call Out’s – Sec – 5 * Updated sssd login issue – Sec –11.7.6 * Updated Hardening process – Sec – 10.6 * Host Reporting no data details – Sec – 11.7.9 * Crowdstrike agent issue – Sec – 11.7.7 * Satellite server details – Sec – 14.18 * Additional details on Monitoring – Sec –16.4 * Updated Patching process – Sec –18.7 |
| V2.3 | Update | 02th July, 2024 | Linux Team | * Updated patching |
| V2.4 | Update | 11th Feb 2025 | Linux Team | * Update decomm process |

**Document Approval Details**

| Date | Version | Approver | Comments |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

**Document Reviews**

| Date | Company | Reviewer | Notes |
| --- | --- | --- | --- |
| 1st April 2022 | Accenture | Taha and Vikram | Provided Review comments on the structure, formatting, and operational activities. |
| 15th May 2022 | Accenture | KJ | Provided Review comments on the structure, formatting, and operational activities. |
| 8th July 2022 | Accenture | Vikram/Taha | Provided review comments |

Table of Contents

[1. Introduction 7](#_Toc108221604)

[2. About Client 8](#_Toc108221605)

[3. About Accenture 9](#_Toc108221606)

[4. Acronyms, Terminology, Appendix 10](#_Toc108221607)

[5. Document Call Outs 12](#_Toc108221608)

[6. Common URLs](#_Toc108221610) 13

[7. Scope](#_Toc108221611) 14

[7.1 In Scope of services](#_Toc108221612) 14

[7.2 Out of Scope of Services](#_Toc108221613) 14

[7.3 Decisions, Important Notes and Recommendations Reference](#_Toc108221614) 14

[8. Environment Details](#_Toc108221615) 16

[8.1 Azure VM Naming Standard](#_Toc108221616) 16

[8.2 Azure Virtual Machine Tagging](#_Toc108221617) 16

[8.3 Azure Access](#_Toc108221618) 17

[8.4 Azure Policy](#_Toc108221619) 17

[8.5 Azure Regions](#_Toc108221620) 17

[9. Operations and Governance](#_Toc108221622) 19

[9.1 ITSM Functions](#_Toc108221623) 19

[10. Operating System Administration](#_Toc108221628) 20

[10.1 Compute Virtual Machines (VMs)](#_Toc108221629) 20

[10.2 Operating Systems for Virtual Machines (VMs)](#_Toc108221631) 20

[10.3 OS Licensing](#_Toc108221632) 21

[10.4 Encryption](#_Toc108221635) 21

[10.5 Antivirus](#_Toc108221636) 22

[10.6 OS Hardening](#_Toc108221637) 23

[11. Operational Support](#_Toc108221638) 24

[11.1 User and Group Management](#_Toc108221639) 24

[11.2 Disk Management](#_Toc108221640) 25

[11.3 Server Performance Management](#_Toc108221642) 39

[11.4 Mount Network Share](#_Toc108221643) 46

[11.5 Server Rebooting Policy](#_Toc108221644) 47

[11.6 Schedule Task Job](#_Toc108221646) 47

[11.7 Common Issues:](#_Toc108221647) 48

[12. Server Provisioning and Decommissioning](#_Toc108221648) 52

[13. Join Server to Domain](#_Toc108221649) 53

[14. Post Server Build Steps](#_Toc108221650) 54

[14.1 Steps to check whether the server is joined to Active Directory](#_Toc108221651) 54

[14.2 Steps to check Tenable IO agent status / Qualys agent status](#_Toc108221652) 54

[14.3 Steps to check/verify the Public IP in the Overview of the VM in the Azure Portal](#_Toc108221653) 55

[14.4 Steps to check/verify CrowdStrike agent](#_Toc108221654) 56

[14.5 Steps to check/verify Disk Encryption.](#_Toc108221655) 56

[14.6 Steps to check/verify NTP configuration](#_Toc108221656) 57

[14.7 Steps to verify the server is update in CMDB.](#_Toc108221657) 58

[14.8 Steps to verify the server is added to backup 58](#_Toc108221658)

[14.9 Steps to verify the server is added to monitoring](#_Toc108221659) 59

[14.10 Steps to validate the IP Address and number of NIC attached:](#_Toc108221660) 59

[14.11 Steps to Identify the OS Version:](#_Toc108221661) 60

[14.12 Steps to validate VM status:](#_Toc108221662) 61

[14.13 Steps to validate VM Lock to Prevent Deletion is enabled:](#_Toc108221663) 62

[14.14 Steps to validate SELinux status on Server:](#_Toc108221664) 62

[14.15 Steps to validate a disk exists at LUN 0:](#_Toc108221665) 62

[14.16 Steps to ensure Azure VM Guest Agent is started](#_Toc108221666) 63

[14.17 Steps for IP forwarding – How to Disable/Enable using net.ipv4.ip\_forward](#_Toc108221667) 63

[14.18 Steps for Repo issue](#_Toc108221668) 64

[15. Networking](#_Toc108221669) 68

[16. Monitoring](#_Toc108221670) 69

[16.1 Azure Monitor](#_Toc108221671) 69

[16.2 Creating Alert](#_Toc108221672) 72

[16.3 Log queries with Performance records](#_Toc108221673) 74

[16.4 Create custom query with below metrics for monitoring](#_Toc108221674) 75

[17. Backups & Restore](#_Toc108221675) 77

[18. Server Patching](#_Toc108221676) 78

[18.1 Patching Schedule](#_Toc108221677) 78

[18.2 Patching Approval Process](#_Toc108221678) 79

[18.3 Emergency or Adhoc Patching Process](#_Toc108221679) 79

[18.4 Rollback](#_Toc108221680) 79

[18.5 Patching Exception](#_Toc108221681) 79

[18.6 Patching Compliance Report](#_Toc108221682) 80

[18.7 Patching Communications](#_Toc108221683) 81

[18.8 Azure Update Management](#_Toc108221684) 81

[18.9 Enable Update Management](#_Toc108221685) 81

[18.10 Schedule an Update Deployment](#_Toc108221686) 83

[18.11 View Results of an Update Deployment](#_Toc108221687) 87

[19. Storage Management 88](#_Toc108221688)

[20. Vulnerability Management](#_Toc108221689) 89

[21. Tools](#_Toc108221694) 90

[22. Vendor Management & SLA](#_Toc108221695) 91

[22.1 Azure case logging](#_Toc108221696) 91

[22.2 Escalation Matrix](#_Toc108221697) 91

[23. Contacts](#_Toc108221698) 92

[23.1 CMS contacts](#_Toc108221699) 92

[23.2 Build and Migration contacts](#_Toc108221700) 92

[23.3 Escalation Matrix Internal CMS](#_Toc108221701) 93

[23.4 Escalation MSHS](#_Toc108221702) 93

[24. SOP](#_Toc108221703) 94

1. Introduction

This document will act as a handbook which consists of all the technical procedures and processes that are required to support the MSHS Azure Linux Infrastructure. The CMS Linux Operation team will leverage this document for all the processes, tools, procedures, and resources to perform day-to-day operations within the IT Infrastructure and provide world-class service to the business and end-users.

When an incident or problem occurs in the environment, an operations organization relies on its Standard Operating Procedures (SOP’s) or troubleshooting guidelines to resolve the problem. A proactive approach to documentation is needed to support Azure Infrastructure operations within an organization.

This Run Book will serve to define daily operations tasks to support the infrastructure deployed for MSHS and recommended troubleshooting tasks to revolve issues which may be encountered.

Any updates in the document should be reviewed & approved.

2. About Client

Mount Sinai Health System (MSHS) is New York City's largest academic medical system, encompassing eight hospitals, a leading medical school, and a network of ambulatory practices. Mount Sinai is an international source of unrivaled education, translational research and discovery, and clinical delivery outcomes.

MSHS is among the top research and clinical institutions providing response to COVID-19, leveraging numerous artificial intelligence algorithms and machine learning models developed in-house.  The current pandemic has accelerated the need and urgency for speed and innovation, including rapid access to data and collaboration. However, MSHS is constrained by a legacy technology environment that is costly to maintain, and in some instances, with components beyond end of life. The culmination of technical debt has created an environment that is costly to maintain and prohibitive to research advancement and clinical outcomes.

Given the demands placed on the clinical and research teams; there exists an enterprise imperative to enable a landscape of technology services that are up to date, always available, inexpensive to implement / maintain, and readily available on a self-service basis.

3. About Accenture

Accenture is a global management consulting, technology services and outsourcing company. Combining unparalleled experience, comprehensive capabilities across all industries and business functions, and extensive research on the world's most successful companies.

4. Acronyms, Terminology, Appendix

| Term | Description |
| --- | --- |
| FW | Firewall |
| IP | Internet Protocol |
| ITSM | Information Technology Service Management |
| KB | Knowledge Base |
| KQL | Kusto Query Language |
| MS | Microsoft |
| NSG | Network Security Group |
| OS | Operating System |
| RBAC | Role Based Access Control |
| RCA | Root Cause Analysis |
| RDP | Remote Desktop Protocol |
| SDM | Service Delivery Manager |
| SIEM | Security Information and Event Management |
| SLA | Service Level Agreement |
| SNOW | ServiceNow |
| SOC | Security Operations Centre |
| VM | Virtual Machine |
| VPN | Virtual Private Network |
| RG | Resource Group |
| SUB | Subscription |
| MG | Management Group |
| DR | Disaster Recovery |
| LBI | Load Balancer (Internal) |
| ASG | Application Security Group |
| KV | Key Vault |
| LBE | Load Balancer (External) |
| ST | Storage Account |
| RSV | Site Recovery Vault |
| RT | Route Table |
| AA | Automation Account |

5. Document Call Outs

This section covers all the references to other documents

| Document | Link |
| --- | --- |
| Linux\_Operations\_Runbook | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ef7ro_AgHS1Lgzw_j08z2JEBSbx0Ev1bRuXnlyj7FvNp7A?e=pjLNDX) |
| Storage\_Operations\_Runbook | [click\_here](https://mtsinai.sharepoint.com/sites/CloudOperations-CMS/Shared%20Documents/General/Runbook/Azure%2C%20VMware%20%26%20Windows/CMS_Foundation_Runbook_v2.1.docx) |
| Backup\_Operations\_Runbook | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ed-8DGYuGGVCgf8_U9Goc3UBEYI_5mNCAuXMgA-7_NWlag?e=RJx3wE) |
| Foundation\_Runbook | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ef7ro_AgHS1Lgzw_j08z2JEBSbx0Ev1bRuXnlyj7FvNp7A?e=pjLNDX) |
| CMS DR runbook | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EWartxFi-uxBqun8thW8CR0BoYpsybnapPGR_wg4tJAA8Q?e=Qn7GbF) |
| HLD | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EfYmHfuXBNVGswXD5BQVNXIB3BUNbwo2sTG4_S4eZxE12g?e=lzoTJT) |
| LLD | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EYsn_F_K33xEhhlza_XCuZ8BFKfkptJmHUSx7NN8dq-ZBA?e=iFLWok) |
| DevOps | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EZeT5o8UhzVHphf5_Cyf2d4BUftpx4rz8FxTWgkZ4oO_hw?e=n9ecIW) |
| CIS Benchmark | [click\_here](https://mtsinai.sharepoint.com/%3Ap%3A/s/CloudOperations-CMS/EVLIN9hJimFLgwJH1VitBZUBXSFcLw0P0Sd67hVVgzProw?e=azbIkl) |
| Satellite Server Document | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EbCISmYtHjtKvNR3lTWI-R8Bh_PKG8wh-heQvd598PCI4Q?e=g1xPlj) |
| Monitoring Matrix Runbook | [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ea-xuDYvBzdKtyz42Zk2AXYBx82UiglB2yAhNd4L6svD2w?e=Z1pMR5) |
| Patching Document | [click\_here](https://mtsinai.sharepoint.com/%3Ap%3A/s/CloudOperations-CMS/ES1ndE5Z6ZpDklJW1j7cn1sBH4KWtlm3s39er_2t_VADmQ?e=PY8cX4) |

6. Common URLs

| Usage | URL |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

7. Scope

7.1 In Scope of services

This Run Book covers basic operating guidelines and procedures necessary for administering and maintaining servers in Linux infrastructure. The scope of this document and work package is to:

|  |  | | |
| --- | --- | --- | --- |
|  |  |  |  |
| IS 1 | Systems Management (Linux Scope)   * Operating System Administration * Operating System Patch Management * Operating System Configuration and Support * Vulnerability Remediation * Agent Installtion | | |
| IS 2 | Infrastructure monitoring and incident management   * Infrastructure monitoring and alert verification * Incident management and resolution | | |
| IS 3 | Service Request Fulfillment   * Provisioning, decommissioning, and Modification of the Azure IaaS environment | | |
|  |  | | |

Table 1 In Scope

7.2 Decisions, Important Notes and Recommendations Reference

Throughout this document decisions, important notes or recommendations are highlighted using the following:

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Important note | | |

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | Architecture Decision | | |

|  | **Decision required** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ? | Decision required | | |

|  | **Recommendation** | | |
| --- | --- | --- | --- |
|  |  |  |  |
|  | Recommendation by Build and/or MSHS. | | |

|  | **Infrormation Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | Dependency on HLD/LLD, KT or Deployment | | |

8. Environment Details

8.1 Azure VM Naming Standard

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer to LLD mentioned in the link.  [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EYsn_F_K33xEhhlza_XCuZ8BFKfkptJmHUSx7NN8dq-ZBA?e=iFLWok)  Design Decision on Naming Standard are available in LLD **Section 3.4**. | | |

8.2 Azure Virtual Machine Tagging

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | * Required tags will be defined within infrastructure deployment templates, ensuring resources are tagged at time of deployment * Tags will be monitored, controlled, and reported on as part of normal operations. * Common tags from Resource Groups will be inherited to all resources within the resource group. * Azure Policy will be used to audit resources missing required tags or with not-allowed values. Azure Policy can also enforce inheritance of common tags from the parent resource group. * Design Decision on Tag values are available in LLD **Section 3.7**. | | |

![](data:image/png;base64...)

8.3 Azure Access

Azure portal access is secured and authenticated through built-in Azure Active Directory within Azure and should be connected using VDI. The Azure team takes care of the access control to Grant or Deny access to the users who request for Azure portal access.

* Access Azure portal from MSHS VID using the SSO (Single Sign On)
* Log into Azure portal to access Azure system using the AD account with MFA (Multi Factor Authentication).

**Access to the Server:**

* A new PA account will be created for CMS team members
* AD Group for CMS members will be created: **MSH**-**LINUX Server Local Administrators-ACN**
* **The group will be attached to MSHS AD Group:** For example: MSH- Server Local Administrators

8.4 Azure Regions

Azure provides services across multiple geographic regions, each supported by multiple datacenters and availability zones. In some cases, these regions represent a resource boundary – for example, Certain Azure services, VM sizes are only available in certain regions.

|  | Architecture Decision | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | Due to the availability of virtual machines, as well as other required services, the MSHS services for the Cloud Migration project will be provisioned in the following regions:   * Primary Region “East US”. * Secondary Region “South Central US” for DR.     For updated regions, refer Latest LLD -[click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EYsn_F_K33xEhhlza_XCuZ8BFKfkptJmHUSx7NN8dq-ZBA?e=iFLWok)  Design Decision on azure region are available in LLD **Section 3.2**. | | |

![](data:image/png;base64...)

.

9. Operations and Governance

9.1 ITSM Functions

The following ITSM functions are currently being leveraged in MSHS. Below is a brief description of each and how they will be leveraged in the future state model.

**ITSM Process:**

* [Incident Management](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EUsndgXnlfZLr3ynr9mezFkB11ZKeMC4yWRnxvWn-Tqv0Q?e=UcYPLi)
* [Problem Management](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EdlalE_UJWRKuNJcXkD0LDoBmBmkiVz9TAQ_25Ck5DpRJA?e=HRGKGP)
* [Change Management](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EUPlbyvbshVNgAoXJQ2VsJgBQnoQ6EBjDZh1bArWYntBVg?e=WFHrT5)
* [Service request Management](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EeDhD-6GIDBIhFG4czwDpe0B0wQBRcADL0dF8-5AHDDJog?e=wDEu0s)
* [Configuration Management](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EU52EF1OriBNheim53sUkicB0qp09J80tjZ1XhIabATJFw?e=4sYqdw)

**Governance:**

CMS Operation governance model cover the daily, weekly, monthly cadence on the service performance

* **Daily Meeting:** Daily service dashboard review with MSHS CMS Leadership on applicable ITSM Functions (Duration: 10 Minutes)
* **Weekly Meeting**: Weekly Service Delivery review with MSHS CMS Leadership on overall service performance for the previous week (Every Wednesday @ 9:30 AM EST)
* **Monthly Meeting**: *(To be established)*

10. Operating System Administration

10.1 Compute Virtual Machines (VMs)

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | These general guidelines will be followed for virtual machine deployment to Azure:   * Avoid storing data on the OS disk. Instead create data disks, and in the case of databases ensure that caching is disabled. * Only store temporary data on the Temp Drive. There is no guarantee of data persistence for that drive. * VMs will be placed in availability sets to achieve a 99.95% uptime SLA, on a case-by-case basis. Requirements per application will be provided by the MSHS team. * VMs will be placed in availability zones to achieve a 99.99% uptime SLA, on a case-by-case basis. Requirements per application will be provided by the MSHS team. * Tag VMs with the metadata necessary to identify the owner, function, application, etc. * Deploy scale sets to achieve auto-scaling functionality for heavy-use applications with predictable loads. * It is recommended to use an endpoint protection solution on all Azure virtual machines. * Azure Managed disks are recommended for all production workloads. Non-managed disks can be used for Dev workloads. * All virtual machines must be hardened to meet CIS Benchmark compliance of at least 90%. The CIS L1 controls script will be executed against all machines in the MSHS environment. * Azure Storage Service Encryption (ASSE) will be used for all storage. * Use database-level encryption for databases, in addition to ADE. * Design Decision on VM Deployment are available in LLD **Section 6.3.2** * Deploying VM’s through Azure Portal is not approved as per the MSHS Design. * CMS Team leverage Azure DevOps Service to support the identified DevOps objectives, and provision the environment using Devops pipeline * Deployment using DevOps will be covered in the Devops runbook which CMS team will refer for deployments. DevOps runbook link will be updated post the document is completed. | | |

10.2 Operating Systems for Virtual Machines (VMs)

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | MSHS Will Use latest Marketplace Image for OS Deployment | | |

10.3 OS Licensing

The following licensing models are the most common for enterprise deployments.

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | * For Lift & Shift – hybrid * For Replat forming or new provisioning - Pay-As-You-Go (PAYG)/hybrid | | |

10.4 Encryption

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | By default, all MSHS’s VM disks are encrypted with Azure Storage Service Encryption. For additional security, Microsoft recommends encrypting the Azure VM disks at the OS level using Azure Disk Encryption. | | |

**Azure Disk Encryption**

Azure Disk Encryption (ADE) provides encryption of data at rest for both OS and data disks. Azure Disk Encryption utilizes the Bitlocker feature of Windows to encrypt at the volume-level of OS and data disks of virtual machines and virtual machine scale sets. For Linux machines, ADE uses the DM-Encryption feature to provide encryption. ADE is integrated with and relies upon Azure Key Vault to control and manage disk-encryption keys and secrets.

**Storage Service Encryption (SSE)**

Azure Storage Service Encryption (SSE) for data at rest of the Azure storage platform automatically encrypts the data before persisting it to Azure Managed Disks, Azure Blob, Queue, or Table storage, or Azure Files, and decrypts the data before retrieval. The handling of encryption, encryption at rest, decryption, and key management in SSE is transparent to users. All data written to the Azure storage platform is encrypted through 256-bit AES encryption. Storage Service Encryption is enabled for all new and existing storage accounts and cannot be disabled.

![](data:image/png;base64...)

10.5 Antivirus

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | For each MSHS subscription, Microsoft Defender for Cloud will be enabled to actively monitor the environment. Azure Defender will be automatically enabled for all resources except for endpoint protection and/or the OS agent for IaaS deployments, which will be protected with Crowdstrike.  The agent will be included and configured as part of the automation templates. | | |

To validate that the sensor is running on Linux host via the command line, run this command at a command prompt:

systemctl status falcon-sensor

Can see STATE: RUNNING, CrowdStrike is installed and running.

![](data:image/png;base64...)

Once the agent is running need to check with POC that the servers are reporting in console or not.

| POC | CybersecurityEngineering@mountsinai.org |
| --- | --- |

10.6 OS Hardening

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | The following policies, processes and hardening will be implemented on servers in Azure.   * Utilize Security Configuration Wizard and Security Compliance Toolkit to create a secure, comprehensive, and consistent base DC build * Deny access to the Internet from both the local machine (web browsing) and perimeter firewalls * Adhere strictly to patch management policies * Crowd Strike will be used for endpoint protection in Azure and on-premises. The agent will be included and configured as part of the automation templates. * Tenable.io will be used for vulnerability scanning in Azure and on-premises. The agentwill be deployed and configured as part of the automation templates*.* * In case of any vendor-built server, where appteam requests help in adding server in domain cyber security team's approval is required. | | |
|  |  | | |

As a part of build script hardening script will be updated

Following parameters are the part of hardening script file, As a part of ORC below parameters will be captured.

Refer Document Call Outs **section 5** for detailed procedure

* Ensure Autofs  service is off state
* Ensure sticky bit is set /tmp
* Ensure SELinux is installed and permissive mode
* Ensure telnet server is not enabled
* Ensure ntp is configured
* Ensure chrony is configured
* Ensure auditd is enabled
* Ensure  xinetd is not enabled
* Ensure nfs and rpc are not enabled
* Ensure ftp server not enabled
* Ensure ipv6 is disabled
* Ensure iptable is installed
* Ensure DHCP server not enabled.
* Ensure SSH root login is disabled
* Ensure Banner/motd is enabled

11. Operational Support

11.1 User and Group Management

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | User creation is not in CMS scope. All the user creation request to go through MSHS standard process via SailPoint request. They need to be part of the respective AD group to access the environment. For exceptions where a local user is needed follow the below steps post getting necessary approvals based on a Service Request | | |

11.1.1 User addition

* + **To add a simple user(test\_user)**

sudo useradd test\_user

* + **To give a home directory path for new user**

sudo useradd -d /home/test\_user test\_user

* + **To create a user with specific user id**

sudo useradd -u “**1234”** test\_user

* + **To create a user with specific group id**

sudo useradd -g “**1000**” test\_user

* + **To create a user with expiry date**

sudo useradd -e **2022-05-30** test\_user

* + **To create a user with changed login shell**

sudo useradd -s /bin/sh test\_user

* + **To set an unencrypted password for the user**

sudo useradd -p test\_password test\_user

11.1.2 Set Initial password

1 Log in with AD user and switch to sudo user (**sudo su)**

2. Use the command**passwd** "name of the user" (for example,**passwd roman**)

3. Share the password securely with the user

11.1.3 User Deletion

userdel username

Use the -r(--remove) option to force userdel to remove the user’s home directory and mail spool:

userdel -r username

11.1.4 Group addition

To create a new group in Linux, follow these steps:

1. Use the **groupadd “**Group name**”** command.
2. Replace Group name with the name of the group that is required to be created.
3. Confirm by checking the /etc/group file (for example, grep software /etc/group or cat /etc/group).

11.1.5 Changing a User’s Group

If the ask is to change the primary group a user is assigned to:

* Use the command **usermod**.

usermod -G examplegroup “name of user”

11.1.6 Group deletion

To delete the group, use the below command

groupdel “groupname”

11.2 Disk Management

|  | **Important note** | |
| --- | --- | --- |
|  |  |
| ! | * Activity to be performed based on the incident received in the Service Now or alert received using Azure Monitor or a service request raised by the business post the necessary approval. Please refer the section 9.1 ITSM Functions for raising the request. * Alerts threshold will be set based on the details mentioned below. * Drives to be extended on repetitive alert when there is no possibility of further housekeeping. | |

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | * Unless using [Resize without downtime (preview only supported for data disk)](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/expand-os-disk#resize-without-downtime-preview), resizing an OS or data disk of an Azure VM requires the VM to be deallocated (Stop). * Shrinking an existing disk isn’t supported and can potentially result in data loss. * After expanding the disks, need to [expand the volume in the operating system](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/expand-os-disk#expand-the-volume-in-the-operating-system) to take advantage of the larger disk. | | |

11.2.1 Add a disk to a Linux VM

Below steps show how to attach a persistent disk to the VM so that it can be used to preserve the data - even if the VM is reprovisioned due to maintenance or resizing.

Find the virtual machine

1. Go to the Azure portal to find the VM. Search for and select **Virtual machines**.
2. Choose the VM from the list.
3. In the **Virtual machines** page, under **Settings**, choose **Disks**.

**Attach a new disk**

1. On the **Disks** pane, under **Data disks**, select **Create and attach a new disk**.
2. Enter a name for the managed disk. Review the default settings, and update the **Storage type**, **Size (GiB)**, **Encryption** and **Host caching** as necessary.

![Review disk settings.](data:image/png;base64...)

1. When done, select **Save** at the top of the page to create the managed disk and update the VM configuration.

**Attach an existing disk**

1. On the **Disks** pane, under **Data disks**, select **Attach existing disks**.
2. Click the drop-down menu for **Disk name** and select a disk from the list of available managed disks.
3. Click **Save** to attach the existing managed disk and update the VM configuration:
4. **Format and mount for new disk additions**

**Find the disk**

Once connected to the VM, it is necessary to find the disk.
In this example, using **lsblk**to list the disks.

lsblk -o NAME,HCTL,SIZE,MOUNTPOINT | grep -i "sd"

The output is like the following example:

sda 0:0:0:0 30G

├─sda1 29.9G /

├─sda14 4M

└─sda15 106M /boot/efi

sdb 1:0:1:0 14G

└─sdb1 14G /mnt

sdc 3:0:0:0 50G

Here, sdc is the disk that required. If required to add multiple disks and aren't sure which disk it is based on size alone, then go to the VM page in the portal, select **Disks**, and check the LUN number for the disk under **Data disks**.

**Format the disk**

Format the disk with **parted**, if the disk size is 2 tebibytes (TiB) or larger then need to use GPT partitioning, if it is under 2TiB, then it is suggested to use either MBR or GPT partitioning.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | It is recommended to use the latest version parted that is available for the distro. If the disk size is 2 tebibytes (TiB) or larger, then must use GPT partitioning. If disk size is under 2 TiB, then either MBR or GPT partitioning can be used. | | |

The following example uses **parted** on /dev/sdc, which is where the first data disk will typically be on most VMs. Replace sdc with the correct option for the disk. Also formatting it using the [XFS](https://xfs.wiki.kernel.org/) filesystem.

sudo parted /dev/sdc --script mklabel gpt mkpart xfspart xfs 0% 100% # Can use mkpart to create the partition to span the entire drive by specifying the percentage to use (here 0% to 100%).

sudo mkfs.xfs /dev/sdc1

sudo partprobe /dev/sdc1

Use the [partprobe](https://linux.die.net/man/8/partprobe) utility to make sure the kernel is aware of the new partition and filesystem. Failure to use partprobe can cause the blkid or lslbk commands to not return the UUID for the new filesystem immediately.

1. **Mount the disk**

Now, create a directory to mount the file system using mkdir. The following example creates a directory at /datadrive:

sudo mkdir /datadrive

Use mount to then mount the filesystem. The following example mounts the /dev/sdc1 partition to the /datadrive mount point:

sudo mount /dev/sdc1 /datadrive

1. **Persist the mount**

To ensure that the drive is remounted automatically after a reboot, it must be added to the /etc/fstab file. It is also highly recommended that the UUID (Universally Unique Identifier) is used in /etc/fstab to refer to the drive rather than just the device name (such as, /dev/sdc1). If the OS detects a disk error during boot, using the UUID avoids the incorrect disk being mounted to a given location. Remaining data disks would then be assigned those same device IDs. To find the UUID of the new drive, use the blkid utility:

sudo blkid

**The output looks similar to the following example:**

/dev/sda1: LABEL="cloudimg-rootfs" UUID="11111111-1b1b-1c1c-1d1d-1e1e1e1e1e1e" TYPE="ext4" PARTUUID="1a1b1c1d-11aa-1234-1a1a1a1a1a1a"

/dev/sda15: LABEL="UEFI" UUID="BCD7-96A6" TYPE="vfat" PARTUUID="1e1g1cg1h-11aa-1234-1u1u1a1a1u1u"

/dev/sdb1: UUID="22222222-2b2b-2c2c-2d2d-2e2e2e2e2e2e" TYPE="ext4" TYPE="ext4" PARTUUID="1a2b3c4d-01"

/dev/sda14: PARTUUID="2e2g2cg2h-11aa-1234-1u1u1a1a1u1u"

/dev/sdc1: UUID="33333333-3b3b-3c3c-3d3d-3e3e3e3e3e3e" TYPE="xfs" PARTLABEL="xfspart" PARTUUID="c1c2c3c4-1234-cdef-asdf3456ghjk"

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Improperly editing the /etc/fstab file could result in an unbootable system. If unsure, refer to the distribution's documentation for information on how to properly edit this file. It is also recommended that a backup of the /etc/fstab file is created before editing. | | |

Next, open the ***/etc/fstab*** file in a text editor as follows:

**sudo nano /etc/fstab**

In this example, use the UUID value for the /dev/sdc1 device that was created in the previous steps, and the mountpoint of /datadrive. Add the following line to the end of the /etc/fstab file:

**UUID=33333333-3b3b-3c3c-3d3d-3e3e3e3e3e3e /datadrive xfs defaults,nofail 1 2**

In this example, using the nano editor, so once editing the file is done, use Ctrl+O to write the file and Ctrl+X to exit the editor.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Later removing a data disk without editing **fstab** could cause the VM to fail to boot. Most distributions provide either the ***nofail*** and/or ***nobootwait*** **fstab** options. These options allow a system to boot even if the disk fails to mount at boot time. Consult the distribution's documentation for more information on these parameters. | | |

The ***nofail*** option ensures that the VM starts even if the filesystem is corrupt, or the disk does not exist at boot time. Without this option, it is possible to encounter behavior as described in [**Cannot SSH to Linux VM due to FSTAB errors**](https://docs.microsoft.com/en-us/archive/blogs/linuxonazure/cannot-ssh-to-linux-vm-after-adding-data-disk-to-etcfstab-and-rebooting)

The Azure VM Serial Console can be used for console access to the VM if modifying fstab has resulted in a boot failure. More details are available in the [**Serial Console documentation**](https://docs.microsoft.com/en-us/troubleshoot/azure/virtual-machines/serial-console-linux).

1. **TRIM/UNMAP support for Linux in Azure**

Some Linux kernels support TRIM/UNMAP operations to discard unused blocks on the disk. This feature is primarily useful in standard storage to inform Azure that deleted pages are no longer valid and can be discarded and can save money if needed to create large files and then delete them.

There are two ways to enable TRIM support in the Linux VM. As usual, consult the distribution for the recommended approach:

* Use the discard mount option in**/etc/fstab**, for example:

UUID=33333333-3b3b-3c3c-3d3d-3e3e3e3e3e3e /datadrive xfs defaults,discard 1 2

* In some cases, the discard option may have performance implications. Alternatively, it is possible to run the **fstrim**command manually from the command line, or add it to the crontab to run regularly:

**Ubuntu**

sudo apt-get install util-linux

sudo fstrim /datadrive

**RHEL/CentOS**

sudo yum install util-linux

sudo fstrim /datadrive

11.2.2 Resize a disk:

If **LiveResize** is enabled and the disk meets the requirements in to resize a disk without downtime in the Azure portal.

1. In the [Azure portal](https://aka.ms/iaasexp/DiskLiveResize), go to the virtual machine in which the ask to expand the disk. Select **Stop** to deallocate the VM.
2. In the left menu under **Settings**, select **Disks**.

![Screenshot that shows the Disks option selected in the Settings section of the menu.](data:image/png;base64...)

1. Under **Disk name**, select the disk the ask to resize.

![Screenshot that shows the Disks pane with a disk name selected.](data:image/png;base64...)

1. In the left menu under **Settings**, select **Size + performance**.

![Screenshot that shows the Size and performance option selected in the Settings section of the menu.](data:image/png;base64...)

1. In **Size + performance**, select the disk size the based on the request.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | When a managed disk is expanded, the updated size is rounded up to the nearest managed disk size. | | |

1. Select **Resize** at the bottom of the page.

![Screenshot that shows the Size and performance pane with the Resize button selected.](data:image/png;base64...)

11.2.3 Expand the disk partition and filesystem

When the disk for the VM is expanded, need to go into the OS and expand the volume to encompass the new space. There are several methods for expanding a partition.

To use an expanded disk, expand the underlying partition and filesystem.

1. SSH to the VM with the appropriate credentials.
2. Expand the underlying partition and filesystem.

a. If the disk is already mounted, unmount it:

**sudo umount /dev/sdc1**

b. Use parted to view disk information and resize the partition:

**sudo parted /dev/sdc1**

View information about the existing partition layout with print. The output is similar to the following example, which shows the underlying disk is 215 GB:

GNU Parted 3.2

Using /dev/sdc1

Welcome to GNU Parted! Type 'help' to view a list of commands.

(parted) print

Model: Unknown Msft Virtual Disk (scsi)

Disk /dev/sdc1: 215GB

Sector size (logical/physical): 512B/4096B

Partition Table: loop

Disk Flags:

Number Start End Size File System Flags

1 0.00B 107GB 107GB ext4

c. Expand the partition with resizepart. Enter the partition number, 1, and a size for the new partition:

(parted) resizepart

Partition number? 1

End? [107GB]? 215GB

d. To exit, enter quit.

1. With the partition resized, verify the partition consistency with e2fsck:

**sudo e2fsck -f /dev/sdc1**

1. Resize the filesystem with resize2fs:

**sudo resize2fs /dev/sdc1**

1. Mount the partition to the desired location, such as /datadrive:

**sudo mount /dev/sdc1 /datadrive**

1. To verify the data disk has been resized, use df -h. The following example output shows the data drive /dev/sdc1 is now 200 GB:

Filesystem Size Used Avail Use% Mounted on

/dev/sdc1 197G 60M 187G 1% /datadrive

11.2.4 Extend an LV when the VG has available space

The traditional way to resize LVs is to extend an LV when the VG has space available. The below method can be used for nonencrypted disks, traditional LVM-encrypted volumes, and LVM-on-crypt configurations.

1. Verify the current size of the file system that the ask to increase:

**df -h /mountpoint**

![Screenshot showing code that checks the size of the file system. The command and the result are highlighted.](data:image/png;base64...)

1. Verify that the VG has enough space to increase the LV:

**vgs**

![Screenshot showing the code that checks for space on the VG. The command and the result are highlighted.](data:image/png;base64...)

**vgdisplay** can also be used:

**vgdisplay vgname**

![Screenshot showing the V G display code that checks for space on the VG. The command and the result are highlighted.](data:image/png;base64...)

1. Identify which LV needs to be resized:

**lsblk**

![Screenshot showing the result of the l s b l k command. The command and the result are highlighted.](data:image/png;base64...)

For LVM-on-crypt, the difference is that this output shows that the encrypted layer is at the disk level.

![Screenshot showing the result of the l s b l k command. The output is highlighted. It shows the encrypted layer.](data:image/png;base64...)

1. Check the LV size:

**lvdisplay lvname**

![Screenshot showing the code that checks the logical volume size. The command and the result are highlighted.](data:image/png;base64...)

1. Increase the LV size by using -r to resize the file system online:

**lvextend -r -L +2G /dev/vgname/lvname**

![Screenshot showing the code that increases the size of the logical volume. The command and the results are highlighted.](data:image/png;base64...)

1. Verify the new sizes for the LV and the file system:

**df -h /mountpoint**

![Screenshot showing the code that verifies the size of the LV and the file system. The command and the result are highlighted.](data:image/png;base64...)

The size output indicates that the LV and file system were successfully resized.

Can check the LV information again to confirm the changes at the level of the LV:

**lvdisplay lvname**

![Screenshot showing the code that confirms the new sizes. The sizes are highlighted.](data:image/png;base64...)

11.2.5 Extend a traditional LVM volume by adding a new PV

When it is needed to add a new disk to increase the VG size, extend the traditional LVM volume by adding a new PV.

1. Verify the current size of the file system that the ask to increase:

**df -h /mountpoint**

![Screenshot showing the code that checks the current size of a file system. The command and the result are highlighted.](data:image/png;base64...)

1. Verify the current PV configuration:

**pvs**

![Screenshot showing the code that checks the current PV configuration. The command and the result are highlighted.](data:image/png;base64...)

1. Check the current VG information:

**Vgs**

![Screenshot showing the code that checks the current volume group information. The command and the result are highlighted.](data:image/png;base64...)

1. Check the current disk list. Identify data disks by checking the devices **in /dev/disk/azure/scsi1/.**

**ls -l /dev/disk/azure/scsi1/**

![Screenshot showing the code that checks the current disk list. The command and the results are highlighted.](data:image/png;base64...)

1. Check the output of **lsblk**:

**lsblk**

![Screenshot showing the code that checks the output of l s b l k. The command and the results are highlighted.](data:image/png;base64...)

1. Attach the new disk to the VM by following the instructions in [Attach a data disk to a Linux VM](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal).
2. Check the disk list and notice the new disk.

ls **-l /dev/disk/azure/scsi1/**

![Screenshot showing the code that checks the disk list. The results are highlighted.](data:image/png;base64...)

**lsbk**

![Screenshot showing the code that checks the disk list by using l s b l k. The command and the result are highlighted.](data:image/png;base64...)

1. Create a new PV on top of the new data disk:

**pvcreate /dev/newdisk**

![Screenshot showing the code that creates a new PV. The result is highlighted.](data:image/png;base64...)

This method uses the whole disk as a PV without a partition. Alternatively, can use **fdisk**to create a partition and then use that partition for **pvcreate**.

1. Verify that the PV was added to the PV list:

**pvs**

![Screenshot showing the code that shows the physical volume list. The result is highlighted.](data:image/png;base64...)

1. Extend the VG by adding the new PV to it:

**vgextend vgname /dev/newdisk**

![Screenshot showing the code that extends the volume group. The result is highlighted.](data:image/png;base64...)

1. Check the new VG size:

**vgs**

![Screenshot showing the code that checks the volume group size. The results are highlighted.](data:image/png;base64...)

1. Use lsblk to identify the LV that needs to be resized:

**lsblk**

![Screenshot showing the code that identifies the local volume that needs to be resized. The results are highlighted.](data:image/png;base64...)

1. Extend the LV size by using -r to increase the file system online:

**lvextend -r -L +2G /dev/vgname/lvname**

![Screenshot showing code that increases the size of the file system online. The results are highlighted.](data:image/png;base64...)

1. Verify the new sizes of the LV and file system:

**df -h /mountpoint**

![Screenshot showing the code that checks the sizes of the local volume and the file system. The command and the result are highlighted.](data:image/png;base64...)

11.2.6 Extend a traditional LVM volume by resizing an existing PV

In some scenarios, the limitations might require resizing an existing disk. Here's how:

1. Identify the encrypted disks:

**ls -l /dev/disk/azure/scsi1/**

![Screenshot showing the code that identifies encrypted disks. The results are highlighted.](data:image/png;base64...)

**lsblk -fs**

![Screenshot showing alternative code that identifies encrypted disks. The results are highlighted.](data:image/png;base64...)

1. Check the PV information:

**pvs**

![Screenshot showing the code that checks information about the physical volume. The results are highlighted.](data:image/png;base64...)

The results in the image show that all of the space on all of the PVs is currently used.

1. Check the VG information:

**vgs**

**vgdisplay -v vgname**

![Screenshot showing the code that checks information about the volume group. The results are highlighted.](data:image/png;base64...)

1. Check the disk sizes. **fdisk**or **lsblk**can be used to list the drive sizes.

for disk in `ls -l /dev/disk/azure/scsi1/\* | awk -F/ '{print $NF}'` ; do echo "fdisk -l /dev/${disk} | grep ^Disk "; done | bash

lsblk -o "NAME,SIZE"

![Screenshot showing the code that checks disk sizes. The results are highlighted.](data:image/png;base64...)

Here identify that which PVs are associated with which LVs by using **lsblk -fs.** The associations can be identified by running **lvdisplay,**

**lvdisplay --maps VG/LV**

**lvdisplay --maps datavg/datalv1**

![Screenshot showing an alternative way to identify physical volume associations with local volumes. The results are highlighted.](data:image/png;base64...)

In this case, all four data drives are part of the same VG and a single LV. The configuration might differ.

1. Check the current file system utilization:

**df -h /datalvm\***

![Screenshot showing the code that checks file system utilization. The command and the results are highlighted.](data:image/png;base64...)

1. Resize the data disks by following the instructions in [Expand an Azure managed disk](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/expand-disks#expand-an-azure-managed-disk). The portal, the CLI, or PowerShell can be used.

**Important**

It is not possible to resize virtual disks while the VM is running. Deallocate the VM for this step.

1. Start the VM and check the new sizes by using **fdisk**.

for disk in `ls -l /dev/disk/azure/scsi1/\* | awk -F/ '{print $NF}'` ; do echo "fdisk -l /dev/${disk} | grep ^Disk "; done | bash

**lsblk -o "NAME,SIZE"**

![Screenshot showing the code that checks disk size. The result is highlighted.](data:image/png;base64...)

In this case, /dev/sdd was resized from 5 G to 20 G.

1. Check the current PV size:

**pvdisplay /dev/resizeddisk**

![Screenshot showing the code that checks the size of the P V. The result is highlighted.](data:image/png;base64...)

Even though the disk was resized, the PV still has the previous size.

1. Resize the PV:

**pvresize /dev/resizeddisk**

![Screenshot showing the code that resizes the physical volume. The result is highlighted.](data:image/png;base64...)

1. Check the PV size:

**pvdisplay /dev/resizeddisk**

![Screenshot showing the code that checks the physical volume's size. The result is highlighted.](data:image/png;base64...)

Apply the same procedure for all the disks that the ask to resize.

1. Check the VG information.

**vgdisplay vgname**

![Screenshot showing the code that checks information for the volume group. The result is highlighted.](data:image/png;base64...)

The VG now has enough space to be allocated to the LVs.

1. Resize the LV:

**lvresize -r -L +5G vgname/lvname**

**lvresize -r -l +100%FREE /dev/datavg/datalv01**

![Screenshot showing the code that resizes the L V. The results are highlighted.](data:image/png;base64...)

1. Check the size of the file system:

**df -h /datalvm2**

![Screenshot showing the code that checks the size of the file system. The result is highlighted.](data:image/png;base64...)

For the Filesystem cleanup , we have various scenarios to perform to keep the threshold under control.

i.e ) For syslog03:/data FS full issue, follow the below procedure to do housekeeping

root@syslog03:~# **cd /data/syslog/fw/HospitalPA**

root@syslog03:/data/syslog/fw/HospitalPA# **du -sh \* | sort -rh | more**

646G syslog-2025-02-07

383G syslog-2025-02-08

369G syslog-2025-02-09

283G syslog-2025-02-10

47G syslog-2025-02-06.gz

45G syslog-2025-02-04.gz

44G syslog-2025-02-05.gz

43G syslog-2025-02-03.gz

21G syslog-2025-02-02.gz

From the above command output, you can see there are four “syslog” files not compressed. Now let’s compress them on the background (so even though your Linux window gets time out, and kick your login out, it will continue run the compress until complete).

“nohup … &” is putting the compress command run on the background.

root@syslog03:/data/syslog/fw/HospitalPA# **nohup gzip syslog-2025-02-10 syslog-2025-02-09 syslog-2025-02-08 syslog-2025-02-07 &**

11.3 Server Performance Management

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Server Performance monitoring is covered in the monitoring section16 This section to include CPU, memory, Network, and Disk Management | | |

11.3.1 CPU usage troubleshooting guidance:

1. Using Azure Monitor,

**Step 1:** Log in to [Azure Portal](https://portal.azure.com/).

**Step 2:** Then go to **Virtual Machines** and select the respective azure VM.

**Step 3:** After choosing the Azure VM, from left hand side of the page, navigate to **Monitoring** >> select **Metrics**

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

**Step 4:** Select **Scope >> Required Azure VM**

* Select **Metric Namespace** == **Virtual Machine Host** c

 ![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

* Next, Choose the **Metric == “Percentage CPU” and Aggregation == “Avg”**

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

* Select Time Generated Number of Days as required

![Graphical user interface, text

Description automatically generated](data:image/png;base64...)

![Chart, line chart

Description automatically generated](data:image/png;base64...)

In the same way if want data for the period requested.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. Go to specific VM We can also verify the CPU utilization by SAR utility.

Below we can see the server resources two three times with one second interval

![Text

Description automatically generated](data:image/png;base64...)

1. Go to specific VM
   * Run the **top** command on the server, command **shows a real-time view of running processes and displays kernel-managed tasks**. The command also provides a system information summary that shows resource utilization, including CPU and memory usage.

![Text

Description automatically generated with low confidence](data:image/png;base64...)

From the above screen shot will find the max, idle & free used for CPU.

If the process can be stopped or a related service can be disabled, stop the process or the service. Then, check whether this mitigates the problem.

# ps  -ef  -- to view list of running process.

# kill -9 PID --- to kill the running process

11.3.2 Memory Management:

* 1. Using Azure Monitor:
     + Go to specific VM
     + Search for the respective sever name for which need to check the memory usage.
     + Go to INSIGHTS tab to monitor the Memory usage and performance within that server and can also get insights as in where the maximum memory is being consumed within the sever along with the timeline information.

![Graphical user interface

Description automatically generated](data:image/png;base64...)

* 1. Server level:
     + Run the **top** command on the server, command **shows a real-time view of running processes and displays kernel-managed tasks**. The command also provides a system information summary that shows resource utilization, including CPU and memory usage.

![Text

Description automatically generated with low confidence](data:image/png;base64...)

From the above screen shot will find the max, idle & free used for Memory.

From here, kill the process or applications that consume more memory post getting necessary approvals.

11.3.3 Disk usage troubleshooting guidance:

Run the du (**Disk Usage)** command, used to check the information of disk usage of files and directories on a server.

df -h shows disk space in human-readable format

![Text

Description automatically generated](data:image/png;base64...)

From above screen will get the total, used and available disk space. Check which folder consuming more disk usage, notify the application team and then clean up the folder to optimise the disk space based on the approval or request.

11.3.4 Log queries with Performance records

Azure Linux VM will have insight for monitoring and data enabled to send to Log analytics workspace.

The following table provides different examples of log queries that retrieve Performance records.

| Description | Query |
| --- | --- |
| All Performance data | Perf |
| All Performance data from a particular computer | Perf | where Computer == "MyComputer" |
| All Performance data for a particular counter | Perf | where CounterName == "Current Disk Queue Length" |
| Average CPU Utilization across all computers | Perf | where ObjectName == "Processor" and CounterName == "% Processor Time" and InstanceName == "\_Total" | summarize AVGCPU = avg(CounterValue) by Computer |
| Maximum CPU Utilization across all computers | Perf | where CounterName == "% Processor Time" | summarize AggregatedValue = max(CounterValue) by Computer |
| Average Current Disk Queue length across all the instances of a given computer | Perf | where ObjectName == "LogicalDisk" and CounterName == "Current Disk Queue Length" and Computer == "MyComputerName" | summarize AggregatedValue = avg(CounterValue) by InstanceName |
| 95th Percentile of Disk Transfers/Sec across all computers | Perf | where CounterName == "Disk Transfers/sec" | summarize AggregatedValue = percentile(CounterValue, 95) by Computer |
| Hourly average of CPU usage across all computers | Perf | where CounterName == "% Processor Time" and InstanceName == "\_Total" | summarize AggregatedValue = avg(CounterValue) by bin(TimeGenerated, 1h), Computer |
| Hourly 70 percentile of every % percent counter for a particular computer | Perf | where Computer == "MyComputer" and CounterName startswith\_cs "%" and InstanceName == "\_Total" | summarize AggregatedValue = percentile(CounterValue, 70) by bin(TimeGenerated, 1h), CounterName |
| Hourly average, minimum, maximum, and 75-percentile CPU usage for a specific computer | Perf | where CounterName == "% Processor Time" and InstanceName == "\_Total" and Computer == "MyComputer" | summarize ["min(CounterValue)"] = min(CounterValue), ["avg(CounterValue)"] = avg(CounterValue), ["percentile75(CounterValue)"] = percentile(CounterValue, 75), ["max(CounterValue)"] = max(CounterValue) by bin(TimeGenerated, 1h), Computer |
| Azure Linux VM Memory usage | Perf | where ObjectName == "Memory" and CounterName == "% Committed Bytes In Use" | summarize AggregatedValue = avg(CounterValue) by Computer, bin(TimeGenerated, 2m) |
| All Performance data from the Database performance object for the master database from the named SQL Server instance INST2. | Perf | where ObjectName == "MSSQL$INST2:Databases" and InstanceName == "master" |

11.3.5 Network Performance Monitor

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | To be covered as part Azure Foundation Runbook. | | |

11.3.6 Change Performance Tiers

The performance of the Azure managed disk is set when disk is created, in the form of its performance tier. The performance tier determines the IOPS and throughput the managed disk has. When the provisioned size of the disk is set, a performance tier is automatically selected. The performance tier can be changed at deployment or afterwards, without changing the size of the disk.

**New disks:**

The following steps show how to change the performance tier of the disk when the disk is first created:

1. Sign in to the [Azure portal](https://portal.azure.com/).
2. Navigate to the VM that needs the creation of a new disk for.
3. When selecting the new disk, first choose the size of the disk needed.
4. Once the selection of a size is done, then select a different performance tier, to change its performance.
5. Select **OK** to create the disk.

![Screenshot of the disk creation blade, a disk is highlighted, and the performance tier dropdown is highlighted.](data:image/png;base64...)

**Change the performance tier of an existing disk without downtime**

It is possible to change the performance tier without downtime, so it’s not required to deallocate the VM or detach the disk to change the tier.

**Prerequisites**

It is required to enable the feature for the subscription before changing the performance tier of a disk without downtime. Please follow the steps below to enable the feature for the subscription:

1. Execute the following command to register the feature for the subscription

Azure CLICopy

az feature register --namespace Microsoft.Compute --name LiveTierChange

1. Confirm that the registration state is **Registered** (may take a few minutes) using the following command before trying out the feature.

Azure CLICopy

az feature show --namespace Microsoft.Compute --name LiveTierChange

**Change performance tier**

Now that the feature has been registered, it is possible to change the applicable disk's performance tiers without downtime.

1. Sign-in to the Azure portal
2. Navigate to the VM containing the disk that is required to change.
3. Select the disk
4. Select **Size + Performance**.
5. In the **Performance tier** dropdown, select a tier other than the disk's current performance tier.
6. Select **Resize**.

![Screenshot of the size + performance blade, performance tier is highlighted.](data:image/png;base64...)

11.4 Mount Network Share

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Activity to be performed based on the service request received in Service Now raised by the business to create and mount a File Share. Steps to create File Share is covered in the Storage Runbook. | | |

1. Once the file share is created, select the share, and select **Connect from Linux**.
2. Enter the mount path to use, then copy the script.
3. Connect to your client and use the provided mounting script.

![Screenshot of file share connect blade.](data:image/png;base64...)

11.5 Server Rebooting Policy

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Planned reboot must be performed during the maintenance window or upon the approval of the application team or business following an approved ServiceNow ticket.  Unplanned reboot in case of server hung or inaccessible, can be performed over an incident with proper documentation. Normally for such cases, the operation team doesn’t seek approval to make sure server restart is performed and application availability is restored asap. | | |

11.6 Schedule Task Job

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | There should be a standard tool to schedule tasks Jobs such Control-M, Azure Scheduler.  In case, it is required from the cron scheduler on exception basis (to be approved by the Service Owner of Linux), below steps need to be followed. | | |

**Below step to create the schedule task**

1. Crontab –l: view the list jobs which are scheduled.

![Diagram

Description automatically generated](data:image/png;base64...)

1. To add or schedule new job/task:
2. Run the command # Crontab -e

30 8 \* \* \* /bin/sh /root/script.sh --- add and save the file, this job will run every day at 8:30 AM.

11.7 Common Issues:

11.7.1 Steps to resolve Sever Not Reachable Error:

**Step1:** Ping the server and check if the IP address is reachable.

![Text

Description automatically generated](data:image/png;base64...)

**Step 2:** If the server is not a pingable login to Azure console, then search with the server’s name

![Graphical user interface, application, email

Description automatically generated](data:image/png;base64...)

**Step 3:** Please check if the server is in Running state, if not then right click on server and start the server.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

**Step 4:** In case if the server is already in **Running** state, then try to login to Server Console.

If the server in **Hung** state, then need to follow the process for Server Reboot to fix this issue.

11.7.2 Service Hung Issues:

For Linux related service will make sure that service is running fine using the below mentioned steps

* + Check the service status by running the command on server # **systemctl status <service-name>**
  + Start the service if hung/stopped by running the command on server # **systemctl restart <service-name>**

11.7.3 New port opening request or issue with standard ports:

From Azure perspective, please check if the VM instance have correct NSG attached or not.

If the port is not enabled, raise a request as per standard process with Foundation team for NSG.

For non-standard ports raise a request with foundation and the on-premises firewall team to open the flow from both sides.

Using the command “**netstat -natu**” able check the list of ports that are listening to the server

![Text

Description automatically generated](data:image/png;base64...)

11.7.4 Encounter errors if a disk does not exist at LUN 0:

When adding data disks to a Linux VM, it is possible to encounter errors if a disk does not exist at LUN 0. If adding a disk manually using the az vm disk attach -new command and specify a LUN (--lun) rather than allowing the Azure platform to determine the appropriate LUN, take care that a disk already exists / will exist at LUN 0.

Consider the following example showing a snippet of the output from lsscsi:

[5:0:0:0] disk Msft Virtual Disk 1.0 /dev/sdc

[5:0:0:1] disk Msft Virtual Disk 1.0 /dev/sdd

The two data disks exist at LUN 0 and LUN 1 (the first column in the lsscsi output details [**host:channel:target:lun**]). Both disks should be accessible from within the VM. If manually specified the first disk to be added at LUN 1 and the second disk at LUN 2, then the disks may not see correctly from within the VM.

Important note

! The Azure host value is 5 in these examples, but this may vary depending on the type of storage selected.

This disk behaviour is not an Azure problem, but the way in which the Linux kernel follows the SCSI specifications. When the Linux kernel scans the SCSI bus for attached devices, a device must be found at LUN 0 for the system to continue scanning for additional devices. As such:

* Review the output of lsscsi after adding a data disk to verify that a disk at LUN 0 is present.
* If the disk does not show up correctly within the VM, verify a disk exists at LUN 0.

11.7.5 SSH issue due to permission issue in SSH config file.

Some time we may face an issue while log in to the server via putty with password.one of the reason behind this is in the ssh configuration file PasswordAuthentication mentioned as No .

go to azure portal and select password reset then select reset configuration only and update.

Once it is done we can able to login via password.

![](data:image/png;base64...)

![](data:image/png;base64...)

11.7.6 Issue in login to server with PA account

SSSD service was not able to connect to the KCM service. Same was identified by below error logs seen in sssd.msnyuhealth.org.log file

============================================================================================
 SSSD domain log shows a Kerberos related error:

(2022-12-12 16:50:28): [be[msnyuhealth.org]] [krb5\_auth\_done] (0x3f7c0): [RID#6] The krb5\_child process returned an error. Please inspect the krb5\_child.log file or the journal for more information
=============================================================================================

Below Steps were followed to fix the issue.

1. Edit /etc/krb5.conf.d/kcm\_default\_ccache

# vi /etc/krb5.conf.d/kcm\_default\_ccache

2. Comment-out the below lines:

[libdefaults]
 default\_ccache\_name = KCM:

3. Restart SSSD:
 #systemctl restart sssd

11.7.7 Error While running Crowdstrike agent

Server might face an issue while running crowdstrike agent on the server, check the error log for crowdstrike in var/log/messages or while running the agent , errors will be related to CID number update the cid and restart the crowdstrike.

/opt/CrowdStrike/falconctl -g --version

systemctl status falcon-sensor.service

falcon-sensor.service agent status

[root@zeuspldnsrslv001 ~]# /opt/CrowdStrike/falconctl -s --cid=2c74d7ac1f164081bef866aa48f41a51-7A

[root@zeuspldnsrslv001 ~]# systemctl start falcon-sensor.service

[root@zeuspldnsrslv001 ~]# systemctl status falcon-sensor.service

11.7.8 VM agent issue

Login to server and check VM agent is running or not

![](data:image/png;base64...)

If agent is not running restart the agent, if any error during restarting the agent check the var/log/messages and take action according to that.

Example:

Some time agent might be stuck due to /var high disk utilization issue

05T05:15:41.106399Z INFO Daemon Daemon Fetching new goal state [incarnation 194 (force update)]

2022-10-05T05:15:41.124610Z WARNING Daemon Daemon Fetching the goal state failed: [Errno 28] No space left on device: '/var/lib/waagent/0.prv

Resolution:

Check the /var utilization in the server housekeep the log files to reduce the /var disk utilization.

![](data:image/png;base64...)

12. Server Provisioning and Decommissioning

**Automation**

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | The team will leverage Azure DevOps Service to support the identified DevOps objectives, and more specifically, deliver the Azure cloud infrastructure in an automated and repeatable manner.   * Server Provisioning process * Server Modification/Update process * Server Decommission process | | |

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | A Change Request is required for any change to a production system at MSHS. This includes changes like the following:   * Provisioning of new servers and services * Decommission of servers and services. * Configuration changes to the servers * Rebooting of Production servers (not technically a change but potentially service impacting so still tracked in Change Management)   For detailed ITSM workflow, kindly refer to ITSM process in **section 9.1** | | |

**Note**: An Azure VM needs to be shut down from Azure Portal only while powering off the VM to address any decommission request or any other Azure VM shutdown request. If the VM is shut down from OS, Azure continues to charge for it. To avoid unnecessary costs, the VM must be stopped from the portal to ensure it is deallocated.

![](data:image/png;base64...)

The decommission request of any servers will be accepted only if complies with following criteria.

* ensure CIs in the decommissioning requests are clearly documented,
* engage the DB team for verification when database servers are involved, and
* require that decommissioning requests be raised or approved by the respective server/DB owner.

13. Join Server to Domain

|  | **Architecture Decision** | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
|  |  | | |  | |  |
| ☼ | * Dedicated identity subscription to host Linux Server Directory domain controllers and Infoblox servers for DNS. | | | | | |
|  | |  |  | |  | |

* **Join Server to domain:**

Deployment Steps: To be covered as part of DevOps KT.

The join process is built into DevOps via service account, no one should be joining the server manually.

**MSHS Linux Server AD Authentication process**

![](data:image/png;base64...)

14. Post Server Build Steps

To complete the post-installation steps.

14.1 Steps to check whether the server is joined to Active Directory

MSHS domains are MSNY.Health.org and MSSM.EDU.Campus

To test whether the system was successfully enrolled into a domain, verify login as a user from the domain.

14.2 Steps to check Tenable IO agent status / Qualys agent status

# /opt/nessus\_agent/sbin/nessuscli <cmd> <arg1> <arg2>

| # nessuscli agent status | Displays the status of the agent, rule-based scanning information, jobs pending, and whether the agent is linked to the server.  **Optional arguments:**   * --local — (Default behavior) Provides the status, current jobs count, and jobs pending. This option prevents the agent from contacting its management software to fetch the status. Instead, it shows the last known information from its most recent sync. * --remote — (Default behavior) Fetches the job count from the manager and displays the status.   **Note:** Tenable does not recommend running frequent status checks with the --remote option (for example, when using automation).   * --offline — Provides the most recently cached agent status when it cannot connect to Nessus Manager or Tenable.io. * --show-token — Displays the agent's token that is used to identify and authenticate with its manager. * --show-uuid — Displays the agent's Tenable UUID. |
| --- | --- |

Qualys Cloud Platform gives you everything you need to continuously secure all of your global IT assets. Now with Qualys Cloud Agent, there’s a revolutionary new way to help secure your network by installing lightweight cloud agents in minutes, on any host anywhere - server, virtual machine, laptop, desktop or cloud instance.

**Linux RPM based system**

# systemctl status qualys-cloud-agent

**Linux Debian based system**

# service qualys-cloud-agent restart

![Graphical user interface, text

Description automatically generated](data:image/png;base64...)

14.3 Steps to check/verify the Public IP in the Overview of the VM in the Azure Portal

![](data:image/png;base64...)

The Public IP isn't visible "inside the VM".

14.4 Steps to check/verify CrowdStrike agent

To confirm the sensor is running, run the following command in terminal:

ps -e | grep falcon-sensor

Must see a similar output as below, CrowdStrike is running.

[user@test ~]# sudo ps -e | grep falcon-sensor 635? 00:00:03 falcon-sensor

**OR**

/opt/CrowdStrike/falconctl -g --version

systemctl status falcon-sensor.service

14.5 Steps to check/verify Disk Encryption.

Verify the disks are encrypted:

In the Azure portal, inside the **Extensions** section, select the Azure Disk Encryption extension in the list. The information for **Status message** indicates the current encryption status:

![Portal check with status, version, and status message highlighted](data:image/png;base64...)

Another way to validate the encryption status is by looking at the **Disk settings** section.

![Encryption status for OS disk and data disks](data:image/png;base64...)

To check on the encryption status of an IaaS VM, use the [Get-AzVmDiskEncryptionStatus](https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus) cmdlet.

To [Sign in to the Azure account with Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/authenticate-azureps), use the [Connect-AzAccount](https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount) cmdlet.

Command: Get**-AzVmDiskEncryptionStatus -ResourceGroupName 'MyVirtualMachineResourceGroup' -VMName 'MySecureVM'**

14.6 Steps to check/verify NTP configuration

Show Information:

**ntpdate -q domainNameOrIpaddress**

**timedatectl**

![](data:image/png;base64...)

Below are the NTP server details:

| **Name** | **Service Status** | **IPv4 Address** | **Site** |
| --- | --- | --- | --- |
| zeus-blox01.mountsinai.org | NTP Service is working | 10.113.4.201 | EastUS |
| zeus-blox02.mountsinai.org | NTP Service is working | 10.113.4.202 | EastUS |
| msmc-blox01.mountsinai.org | NTP Service is working | 10.2.24.21 | MSH |
| msmc-blox02.mountsinai.org | NTP Service is working | 10.5.132.10 | MSH |

![](data:image/png;base64...)

14.7 Steps to verify the server is update in CMDB.

**Step1:** Go to ServiceNow

**Step2:** Select “Create an Incident”

**Step3:** Under Configuration Item tab, enter the server’s name and check if it is populating the server details.

**Step4:** If the details are populated, then the servers are updated in the CMDB.

![](data:image/png;base64...)

![](data:image/png;base64...)

14.8 Steps to verify the server is added to backup

In the Azure portal on the **Backup Items** pane, the list of protected VMs and last backup status with latest restore points time can be verified.

For detailed steps, kindly refer to Backup Runbook process document.

![](data:image/png;base64...)

14.9 Steps to verify the server is added to monitoring

For detailed steps, kindly refer to Monitoring Section 16.

14.10 Steps to validate the IP Address and number of NIC attached:

* Log in to [**Azure Portal**](https://portal.azure.com/).
* Then go to **Virtual Machines** and select the respective azure VM.
* In overview will find the server IP address

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

Azure – If NIC is added or not

VM Properties – Vnet is added or not

From Azure VM properties, under networking section find the NIC details and can check if the NIC is enabled.

![Text

Description automatically generated](data:image/png;base64...)

From Server perspective - Run the ifconfig command on the Server.

ifconfig stands for Interface Configuration. This command is the same as ipconfig and is used to view all the current TCP/IP network configurations values of the computer.  The ifconfig command displays only the enabled configurations of networking devices that are currently connected to the system. In the below screenshot, can see the working of ifconfig command on a Server.

![Text

Description automatically generated](data:image/png;base64...)

14.11 Steps to Identify the OS Version:

Go to Azure Console – Search the VM

Later from the Overview, required OS information can be validated.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

Server – Run the command in Server

# cat /etc/os-release

![Text

Description automatically generated](data:image/png;base64...)

14.12 Steps to validate VM status:

Go to Azure Console -> search Server name –> from here will see if the Server status if it’s in Running/Stopped state.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

14.13 Steps to validate VM Lock to Prevent Deletion is enabled:

* Log in to [Azure Portal](https://portal.azure.com/).
* Then go to **Virtual Machines** and select the respective azure VM.
* Then select the Lock option

![Graphical user interface, application

Description automatically generated](data:image/jpeg;base64...)

14.14 Steps to validate SELinux status on Server:

Go to Azure Console -> search Server name

Connect to specific VM and run the command **#sestatus** to check the SElinux status.

![](data:image/png;base64...)

14.15 Steps to validate a disk exists at LUN 0:

When the Linux kernel scans the SCSI bus for attached devices, a device must be found at LUN 0 for the system to continue scanning for additional devices. As such:

* Review the output of lsscsi after adding a data disk to verify that a disk at LUN 0 is present.
* If the disk does not show up correctly within the VM, verify a disk exists at LUN 0.

Run the following command from the console.

$ lsscsi

[5:0:0:0] disk Msft Virtual Disk 1.0 /dev/sdc

[5:0:0:1] disk Msft Virtual Disk 1.0 /dev/sdd

The two data disks exist at LUN 0 and LUN 1 (the first column in the lsscsi output details [**host:channel:target:lun**]).

Both disks should be accessible from within the VM. If manually specified the first disk to be added at LUN 1 and the second disk at LUN 2, then the disks may not see correctly from within the VM.

14.16 Steps to ensure Azure VM Guest Agent is started

**Ensure Azure VM Guest Agent service is started and up to date**:

* Ensure the Azure VM Guest Agent service is running by executing the command ps -e. Also, ensure the [latest version](https://docs.microsoft.com/en-us/azure/virtual-machines/extensions/update-linux-agent) is installed. To learn more, see [Linux VM guest agent issues](https://docs.microsoft.com/en-us/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms).
* Ensure the [Linux VM agent dependencies on system packages](https://docs.microsoft.com/en-us/azure/virtual-machines/extensions/agent-linux#requirements) have the supported configuration. For example: Supported Python version is 2.6 and above.
* Review the support matrix to check if VM runs on the [supported Linux operating system.](https://docs.microsoft.com/en-us/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
* For Ubuntu: service walinuxagent status
* For other distributions: service waagent status

![](data:image/png;base64...)

14.17 Steps for IP forwarding – How to Disable/Enable using net.ipv4.ip\_forward

The term IP Forwarding describes sending a network package from one network interface to another one on the same device. It should be enabled when you want your system to act as a router that transfers IP packets from one network to another

Most systems will be able to use the sysctl command, which can apply kernel variables. Therefore, you can use the following **sysctl** command to check whether IP forwarding is enabled or disabled.

# sysctl net.ipv4.ip\_forwardnet.ipv4.ip\_forward = 0

The **net.ipv4.ip\_forward** kernel setting is 0. That means it’s off. If it were set to 1, that would mean it’s enabled.

This setting can also be viewed inside the **/proc/sys/net/ipv4/ip\_forward** file on systems with systemd or any other init system.

# cat /proc/sys/net/ipv4/ip\_forward

0

14.17.1 Enable or disable IP forwarding

You can use the following **sysctl** command to enable or disable Linux IP forwarding on your system.

# sysctl -w net.ipv4.ip\_forward=0 OR

# sysctl -w net.ipv4.ip\_forward=1

You can also change the setting inside **/proc/sys/net/ipv4/ip\_forward** to turn the setting on or off.

# echo 0 > /proc/sys/net/ipv4/ip\_forward OR

# echo 1 > /proc/sys/net/ipv4/ip\_forward

Using either method above will not make the change persistent. To make sure the new setting survives a reboot, you need to edit the **/etc/sysctl.conf** file.

# sudo nano /etc/sysctl.conf

Add one of the following lines to the bottom of the file, depending on whether you’d like Linux IP forwarding to be off or on, respectively. Then, save your changes to this file. The setting will be permanent across reboots. The net.ipv4.ip\_forward setting controls whether IP forwarding is turned on or off for IPv4.

net.ipv4.ip\_forward = 0 OR

net.ipv4.ip\_forward = 1

After editing the file, you can run the following command to make the changes take effect right away.

# sysctl -p

14.17.2 Troubleshooting

Note that the **sysctl** command if the service isn’t currently running. Check the status of **sysctl** with this command.

$ systemctl status sysctl

The service should say that it’s active. If not, start the service with this command:

$ sudo systemctl start sysctl

14.18 Steps to register the server in Satellite server

A Linux repository is **a storage location from which your system retrieves and installs OS updates and applications**. Each repository is a collection of software hosted on a remote server and intended to be used for installing and updating software packages on Linux systems

**Yum** is the Red Hat package manager that can query for information about available packages, fetch packages from repositories, install and uninstall them, and update an entire system to the latest available version. Yum performs automatic dependency resolution on packages you are updating, installing, or removing, and thus can automatically determine, fetch, and install all available dependent packages.

Yum can be configured with new, additional repositories, or *package sources*, and provides many plug-ins which enhance and extend its capabilities. Yum can perform many of the same tasks that **RPM** can; additionally, many of the command-line options are similar. Yum enables easy and simple package management on a single machine or on groups of them.

To see which installed packages on your system have updates available, use the following command:

yum check-update

![](data:image/png;base64...)

To shows all enabled repositories

# yum repolist

![](data:image/png;base64...)

All the servers should be pointing to satellite repos and Microsoft repos for updating Microsoft dependencies.

For detailed description refer the satellite document in document Call out’s **section 5** .

14.19 Steps to enable high availability repo

Login to red hat satellite portal.

* 1. click on hosts => content hosts => search for VM to which you would like to assign Red Hat satellite infrastructure subscription => click on VM profile =. click on "subscriptions" +> click on "add" => select red hat infrastructure" subscription and assign it to the VM by clicking on "add selected
  2. click on "repository sets => then search for high availability repository => select it and from drop down arrow of "select action" click on "override to enable"
  3. ssh terminal install the pcs package by below command

# yum install pcs

15. Networking

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed Network Design, kindly refer to LLD. [click\_here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EYsn_F_K33xEhhlza_XCuZ8BFKfkptJmHUSx7NN8dq-ZBA?e=iFLWok)  This is covered in the LLD file **section 4.2.4**  For more information, refer to Foundation Runbook under Document Call Outs section. | | |

16. Monitoring

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Azure Monitor is to be used until My Wizard is deployed. | | |

Design Decision on Azure Monitor are available in LLD **Section 5.1.3.1.**

16.1 Azure Monitor

From a management and monitoring perspective the Azure virtual machines can utilize Operations Management Suite (Log Analytics). Log Analytics provides detailed insights into virtual machines including, but not limited to:

* CPU utilization
* Memory utilization
* Network utilization
* Disk Utilization.

These VM metric are displayed in Log Analytics through dashboard and tile views.

Azure Monitor collects monitoring telemetry from a variety of on-premises and Azure sources. Management tools, such as those in Azure Security Center and Azure Automation, also push log data to Azure Monitor. The service aggregates and stores this telemetry in a log data store that is optimized for cost and performance. Analyze data, set up alerts, get end-to-end views of the applications and use machine learning–driven insights to quickly identify and resolve problems.

![](data:image/jpeg;base64...)

**STEP BY STEP PROCEDURE FOR COLLECTING LOG DATA AND SETTING UP ALERTS**

**Collecting event and performance data:**

1. Azure Monitor Logs provides monitoring, alerting, and alert remediation capabilities across cloud and on-premises assets. The Log Analytics virtual machine extension for Linux is published and supported by Microsoft. The extension installs the Log Analytics agent on Azure virtual machines and enrolls virtual machines into an existing Log Analytics workspace. In the Azure portal, click **More services** found on the lower left-hand corner. In the list of resources, type **Log Analytics**. As begin typing, the list filters based on the input. Select **Log Analytics**.
2. Select **Advanced settings**.

![](data:image/png;base64...)

1. Select **Data**,
2. Here, adds the Health Service event channel by typing in the name below and then click the plus sign **+**.
3. In the table, check the severities **Error** and **Warning**.
4. Click **Save** at the top of the page to save the configuration.
5. Select Performance **Counters** to enable collection of performance counters on a computer.
6. While configuring Performance counters for a new Log Analytics workspace for the first time, an option to quickly create several common counters is given. They are listed with a checkbox next to each.

![](data:image/png;base64...)

Click **Add the selected performance counters**. They are added and preset with a ten second collection sample interval or select the Custom Log Search.

![](data:image/png;base64...)

1. Click **Save** at the top of the page to save the configuration.

16.2 Creating Alert

Steps for creating an alert.

1. In the Azure portal, click **All services**. In the list of resources, type **Log Analytics**. As begin typing, the list filters based on the input. Select **Log Analytics**.
2. In the left-hand pane, select **Alerts** and then click **New Alert Rule** from the top of the page to create a new alert.

![](data:image/png;base64...)

1. For the first step, under the **Create Alert** section, need to select the Log Analytics workspace as the resource, since this is a log-based alert signal. Filter the results by choosing the specific **Subscription** from the drop-down list if there are more than one, which contains Log Analytics workspace created earlier. Filter the **Resource Type** by selecting **Log Analytics** from the drop-down list. Finally, select the **Resource** **DefaultLAWorkspace** and then click **Done**.

![](data:image/png;base64...)

1. Under the section **Alert Criteria**, click **Add Criteria** to select the saved query and then specify logic that the alert rule follows.
2. Configure the alert with the following information: a. From the **Based on** drop-down list, select **Metric measurement**. A metric measurement will create an alert for each object in the query with a value that exceeds our specified threshold. b. For the **Condition**, select **Greater than** and specify a threshold. c. Then define when to trigger the alert. For example, make the selection as **Consecutive breaches** and from the drop-down list select **Greater than** a value of 3. d. Under Evaluation based on section, modify the **Period** value to **30** minutes and **Frequency** to 5. The rule will run every five minutes and return records that were created within the last thirty minutes from the current time. Setting the period to a wider window account for the potential of data latency, and ensures the query returns data to avoid a false negative where the alert never fires.
3. Click **Done** to complete the alert rule.

![](data:image/png;base64...)

1. Now moving onto the second step, provide a name of the alert in the **Alert rule name** field, such as **Alert on all Error Events**. Specify a **Description** detailing specifics for the alert and select
   **Critical (Sev 0)** for the **Severity** value from the options provided.
2. To immediately activate the alert rule on creation, accept the default value for **Enable rule upon creation**.
3. For the third and final step, need to specify an **Action Group**, which ensures that the same actions are taken each time an alert is triggered and can be used for each rule that is defined.

   **Configure a new action group with the following information:**
   a. Select **New action group** and the **Add action group** pane appears.
   b. For **Action group name**, specify a name such as **IT Operations - Notify** and a **Short name** such as **itops-n**.
   c. Verify the default values for **the Subscription** and **Resource group** are correct. If not, select the correct one from the drop-down list.
   d. Under the Actions section, specify a name for the action, such as **Send Email** and under **Action Type** select **Email/SMS/Push/Voice** from the drop-down list.

   The **Email/SMS/Push/Voice** properties pane will open to the right in order to provide additional information.

   e. On the **Email/SMS/Push/Voice** pane, select and setup the preference.
   For example, enable **Email** and provide a valid email SMTP address to deliver the message to

   f. Click **OK** to save the changes.

![](data:image/png;base64...)

1. Click **OK** to complete the action group.
2. Click **Create alert rule** to complete the alert rule. It starts running immediately.

![](data:image/png;base64...)

16.3 Log queries with Performance records

The following table provides different examples of log queries that retrieve Performance records.

| Query | Description |
| --- | --- |
| Perf | All Performance data |
| Perf | where Computer == "MyComputer" | All Performance data from a particular computer |
| Perf | where CounterName == "Current Disk Queue Length" | All Performance data for a particular counter |
| Perf | where ObjectName == "Processor" and CounterName == "% Processor Time" and InstanceName == "\_Total" | summarize AVGCPU = avg(CounterValue) by Computer | Average CPU Utilization across all computers |
| Perf | where CounterName == "% Processor Time" | summarize AggregatedValue = max(CounterValue) by Computer | Maximum CPU Utilization across all computers |
| Perf | where ObjectName == "LogicalDisk" and CounterName == "Current Disk Queue Length" and Computer == "MyComputerName" | summarize AggregatedValue = avg(CounterValue) by InstanceName | Average Current Disk Queue length across all the instances of a given computer |
| Perf | where CounterName == "Disk Transfers/sec" | summarize AggregatedValue = percentile(CounterValue, 95) by Computer | 95th Percentile of Disk Transfers/Sec across all computers |
| Perf | where CounterName == "% Processor Time" and InstanceName == "\_Total" | summarize AggregatedValue = avg(CounterValue) by bin(TimeGenerated, 1h), Computer | Hourly average of CPU usage across all computers |
| Perf | where Computer == "MyComputer" and CounterName startswith\_cs "%" and InstanceName == "\_Total" | summarize AggregatedValue = percentile(CounterValue, 70) by bin(TimeGenerated, 1h), CounterName | Hourly 70 percentile of every % percent counter for a particular computer |
| Perf | where CounterName == "% Processor Time" and InstanceName == "\_Total" and Computer == "MyComputer" | summarize ["min(CounterValue)"] = min(CounterValue), ["avg(CounterValue)"] = avg(CounterValue), ["percentile75(CounterValue)"] = percentile(CounterValue, 75), ["max(CounterValue)"] = max(CounterValue) by bin(TimeGenerated, 1h), Computer | Hourly average, minimum, maximum, and 75-percentile CPU usage for a specific computer |
| Perf | where ObjectName == "MSSQL$INST2:Databases" and InstanceName == "master" | All Performance data from the Database performance object for the master database from the named SQL Server instance INST2. |

16.4 Create custom query with below metrics for monitoring

**Monitoring Rules to be configured:**

**Interim Threshold (temp)**

**Linux OS Baseline\_Non\_Prod**

| Host: Reporting no data (Availability Up/Down) | Down | Major (P2) | NA | NA |
| --- | --- | --- | --- | --- |
| Memory Usage | ≥ 90% | Minor(P3) | ≥ 95% | Major (P2) |
| CPU utilization | ≥ 90% | Minor(P3) | ≥ 95% | Major (P2) |
| Disk Space Usage | ≥ 90% | Minor(P3) | ≥ 95% | Major (P2) |

**Windows OS Baseline \_Prod**

| Host: Reporting no data (Availability Up/Down) | Down | Major(P3) | NA | NA |
| --- | --- | --- | --- | --- |
| Memory Usage | ≥ 95% | Minor(P4) | ≥ 98% | Major(P3) |
| CPU utilization | ≥ 95% | Minor(P4) | ≥ 98% | Major(P3) |
| Disk Space Usage | ≥ 90% | Minor(P4) | ≥ 90% | Major(P3) |

For detailed description regarding azure monitoring refer the document Monitoring Matrix runbook in Document Call out’s **section 5**

16.5 Monitoring the alerts

16.5.1 Disk Utilization

![](data:image/png;base64...)

**Housekeeping of OS FileSystem:**

[root@zeusdlmwdep001 ~]# cd /var

[root@zeusdlmwdep001 var]# du -sh ./\* |grep G

1.6G ./lib

2.8G ./log

1.4G ./opt

./log is consuming more disk space go to ./log folder and check which is consuming more space

[root@zeusdlmwdep001 log]# du -sh ./\* |grep G

1.3G ./messages

If messages is consuming more utilization

* 1. Copy messages file in different file , rename it and make it zip.

cp messages messages-currentdate

zip messages-currentdate

* 1. If there is less space in /var and you are not able to copy and zip then follow below steps:

2.a copy messages file in other drive

E.G Cp messages /tmp

2.b Go to /tmp , rename messages file and make it zip.

mv messages messages-currentdate

zip messages-currentdate

* 1. Move zip file to /var/log

mv messages-currentdate.gz /var/log

* 1. Null the original messages file

>messages

cp –rp messages messages-currentdate

gzip messages-currentdate

**Housekeeping of Data FileSystem:**

example2: if /opt/splunk is consuming more disk space

Check with same command du -sh ./\* and see which file/folder is consuming more space

If that is handle by application team, kindly contact application team and inform them which application is

Consuming more disk space, if needed suggest to increase the disk space.

16.5.2 Memory utilization

Use the below command to check how much memory server is consuming

[root@zeus2nldbsbx002 ~]# free -m

total used free shared buff/cache available

Mem: 64050 7055 43294 0 13701 56278

Swap: 8187 0 8187

[root@zeus2nldbsbx002 ~]# free -g

total used free shared buff/cache available

Mem: 62 6 42 0 13 54

Swap: 7 0 7

Check in var log messages any error related to memory

[root@zeus2nldbsbx002 ~]# cat /var/log/messages |grep -i memory

Top command to check which process is taking more memory

![](data:image/png;base64...)

Sar command to check how much percentage of memory is consuming.

![](data:image/png;base64...)

Check the processes which is consuming more utilization if it is related to application processes Inform application team to housekeep the processes to reduce the utilization below threshold. If there is a requirement to increase the memory then approved request is required for the same.

16.5.3 CPU utilization

Check with top/htop command to see which process/command is taking more CPU's utilization.

![](data:image/png;base64...)

To check how many CPU's are server having

[root@zeus2nldbsbx002 ~]# nproc

8

[root@zeus2nldbsbx002 ~]# lscpu

Architecture: x86\_64

CPU op-mode(s): 32-bit, 64-bit

Byte Order: Little Endian

CPU(s): 8

On-line CPU(s) list: 0-7

Sar command to check the cpu consumption in the server.

![](data:image/png;base64...)

Below command shows which process is consuming more cpu usage it will display the top 10 cpu users.

![](data:image/png;base64...)

Check which process is consuming more CPU utilization, if it related to application process inform application team to housekeep the same.

16.5.4 Heartbeat/Host Reporting no data

Once you receive the hard beat alert check server is pinging continuously. If the server is not pinging check server status in azure portal.

if the server is stopped check in the activity log who has stopped it. Verify the console logs take action.

If Server is decommissioned, raise a request with Mywizard team to remove the server from monitoring.

If servers is not decommissioned, check the splunk agent status.

17. Backups & Restore

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed Backup & Restore process, kindly refer to Backup runbook.   * Backup and Patching Schedule shouldn’t overlap. * Back up Azure VMs in a Recovery Services vault * Install the VM agent on the VM: Azure Backup backs up Azure VMs by installing an extension to the Azure VM agent running on the machine. If the VM was created from an Azure Marketplace image, the agent is installed and running. If create a custom VM, or migrate an on-premises machine, might need to [install the agent manually](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-vms-prepare#install-the-vm-agent) | | |

|  | **Information Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | Dependency on HLD/LLD, KT or Deployment | | |

18. Server Patching

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | * Azure Update is the identified solution as per the HLD/LLD. * When there is a change in the patching schedule of the server, Linux team to ensure or take necessary action for CMDB repository must reflect with the same patch tag. | | |

This section covers the Linux Server environment and is applicable for Operating System patching.

18.1 Patching Schedule

**Patching tags:**

| **Tag Name** | **Usage** | **Tag Value** |
| --- | --- | --- |
| PatchSchedule | Used to identify patch schedule and the exceptions | TAG: PatchSchedule (Value: <environment= D/T/P>-<OSType>-<S1/S2/S3/S4>) Value 1 = D-W-S1   Value 2 = D-W-S2 Value 3 = D-L-S1 Value 4 = D-L-S2 Value 5 = T-W-S1 Value 6 = T-W-S2 Value 7 = T-L-S1 Value 8 = T-L-S2 Value 9 = P-W-S1 Value 10 = P-W-S2 Value 11 = P-W-S3 Value 12 = P-W-S4 Value 13 = P-L-S1 Value 14 = P-L-S2 Value 15 = P-L-S3 Value 16 = P-L-S4 Value 17 = Exempted |

| **Patching Tags** | **Maintenance Window Start Time (EST)** | **Maintenance Window End Time (EST)** |
| --- | --- | --- |
| ZCMSZLS102AM - Linux DMZ Thursday after 2nd Tuesday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSZLS202AM - Linux DMZ Friday after 2nd Tuesday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSDLS102AM - Linux DEV Saturday after 2nd Tuesday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSDLS202AM - Linux DEV Sunday after 2nd Tuesday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSTLS102AM - Linux TEST Saturday after 3rd Tuesday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSTLS202AM - Linux TEST Sunday after 3rd Tuesday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSPLS102AM - Linux PROD Saturday after 4th Tuesday | 2:00 AM | 6:00 AM |
| ZCMSPLS202AM - Linux PROD Sunday after 4th Tuesday | 2:00 AM | 6:00 AM |
| ZCMSPLS302AM - Linux PROD 5th/1st Saturday 02:00 AM | 2:00 AM | 6:00 AM |
| ZCMSPLS402AM - Linux PROD 5th/1st Sunday 02:00 AM | 2:00 AM | 6:00 AM |

**Note:** If in case of any change in existing Patch Schedule (Post approval from POC), the same needs to be updated in CMDB with the help of Service Management team. The new Patch Schedule value should reflect under **CI Classification -> Patch Cycle**.

18.2 Patching Approval Process

The Patching Approval process will go through the Change Control process IT Service Management (ITSM) - Change Management and will require a Change Request approval from CAB team.

A change request with applicable patches in Service Now for Linux and Windows VM instances for the patching window will be created and taken through the Change Control process.

| Responsible Role | Activity |
| --- | --- |
| CMS | A change request will be raised and seek approval as per - IT Service Management (ITSM) - Change Management. |
| Application Owner | Not required as it is scheduled based on request and pre-approval. |
| MSHS Cloud Operations Lead | Not required as it is scheduled based on request and pre-approval. |
| CAB Approver | Reviews and approves the emergency patching change request. |
| CMS | Following approval, the email notification will be sent to the stakeholders and patching would be executed for any specific reason or to remediate a patching failure at appropriate maintenance window. |

18.3 Emergency or Adhoc Patching Process

In the event a system must be patched outside of the patching (zero-tolerance critical patch release by vendor), following process should be followed.

| Responsible Role | Activity |
| --- | --- |
| CMS | An emergency change request will be raised and seek approval as per - IT Service Management (ITSM) - Change Management. |
| Application Owner | Reviews and approves the emergency patching change request. |
| MSHS Cloud Operations Lead | Reviews and approves the emergency patching change request. |
| CAB Approver | Reviews and approves the emergency patching change request. |
| CMS | Following approval, the email notification will be sent to the stakeholders and patching would be executed for any specific reason or to remediate a patching failure at appropriate maintenance window. |

18.4 Rollback

| Responsible Role | Activity |
| --- | --- |
| CMS | Update Management does not offer any patch rollback option.  System will be restored from the latest backup, in case of any rollback is required.  Example: System failure post patching activities. |

18.5 Patching Exception

| Responsible Role | Activity |
| --- | --- |
| CMS | The following step needs to be confirmed.  All servers with specific tag key ‘ops-exclude-patch’ (TBD) and value as “RITM Number” will be excluded from patch schedules. Approved RITM details will be shared by Application Owner |
| Application Owner | * Any existing or newly introduced system in Landing Zone, which deviates from the patching guidelines in this Runbook must gain exception approval. * Any system owner who requires their servers be excluded from the patching guidelines in this Runbook will gain exception approval before that server is excluded from patching.   All exceptions will be submitted and approved via ServiceNow.  The ServiceNow catalog item to be submitted is to be checked.  Note: The server needs to be excluded from the update deployment schedule. |
| Application Owner | Any ad-hoc exceptions that cannot adhere to the Patching Exception process will need the email approval from MSHS Cloud Operations lead to be excluded from scheduled patching. The Application Owner will be required to formally request exception approval through the Patching Exception process as defined above. |
| Cloud Operations Engineer | Systems that received Adhoc exception approval will be re-added to the patch schedule after the exception period agreed to by the MSHS Cloud Operations lead.  Any system that has formal patching exception approval and needs to be re-introduced into the patching schedule will require approved RITM submitted by Application Owner. |

18.6 Patching Compliance Report

| Responsible Role | Activity |
| --- | --- |
| CMS | The overall patch compliance summaries can be in the navigation pane of the **Update management center**.  The values displayed for each column are:   | **Field Name** | **Description** | | --- | --- | | Machine Name | Name of the machine attached to Update Management. | | Compliance | State of the system's compliance with security and critical updates. | | Update agent readiness | View the health of the update agent. If there's an issue, select the link to go to troubleshooting documentation that can help you correct the problem. | | Platform | Lists the platform as either Azure or non-Azure. | | Operating system | Lists the operating system as either Windows or Linux. | | Critical missing updates | Count of missing critical updates. | | Security missing updates | Count of missing security updates. | | Other missing updates | Count of non-security and non-critical updates. | | Update approval source | The source of updates. Either Windows update, WSUS, and Microsoft update *applicable to Windows*. | | Windows auto update | Default OS update setting on the machine *applicable to Windows*. | |

18.7 Patching Communications

| Responsible Role | Activity |
| --- | --- |
| CMS | **Pre-Patching Communication:**  Application Owners will be notified through manual email communication on patching activity, refer the document Patching process in Document call Out’s **section 5**.  **Post-Patching Communication:**  Application Owners will be notified through manual email communication on patching activity status, refer the document Patching process in Document call Out’s **section 5**. |

18.8 Azure Update Management

The Azure Update Management solution can be used to manage updates and patches for virtual machines (VMs). Through Azure Update Management, all the available updates can be managed, can schedule the installation of required updates, and review deployment results after installing updates.

18.9 Enable Update Management

To enable Update Management on the VM:

1. Open the Azure portal. In the left menu, select **Virtual machines**. Select a VM from the list.
2. On the VM page, under **OPERATIONS**, select **Update management**. The **Enable Update Management** window opens.

Select the **Enable for this VM**option and update the**Location, Log Analytics workspace**, and **Automation account**details. Then select **Enable**.

![](data:image/png;base64...)

Once the Update Management is enabled, it will take a few minutes for completion. After that, the **Update management window will open. The missing updates will be displayed under the Missing Updates tab.**

![](data:image/png;base64...)

To get the details of missing updates, click on any update to open the **Log Search**window. see a predefined query for that specific update. The query for detailed information can be modified if required.

![](data:image/png;base64...)

18.10 Schedule an Update Deployment

The next step is to schedule an update deployment. Open the automation account. In the left menu, select **Update Management**.

The update Management window will open. Under the **Machines** tab, all the machines connected to the automation account through the linked workspace will be displayed. Under the **Update Deployments** tab, the status of past scheduled deployments will be visible. Under the **Schedule update deployment**tab, a list of upcoming and completed deployments will be listed.

In this step, schedule the new deployment for specific VMs or multiple VMs at once, select the update classification, include or exclude certain updates, and specify the schedule.

Select **Schedule update deployment**. The **New update deployment**window will open, and specify the following information:

* **Name:** Enter a unique name for the update deployment.
* Add the VM's to the Automation Account for the Environment Subscription.
* **Operating system:** Select the operating system (OS) (Windows or Linux) based on the VMs.
* **Groups to update (preview):** Select the subscription and select edit option, Once the edit option opens select the PatchSchedule Tag.

![](data:image/png;base64...)

* **Create Schedule for the VM's**
  + Provide start Date @ time
  + Select the Time zone for patching (preferably EST)
  + Reoccurrence Type
  + Reoccur Type
  + Select Day
  + Set Expiration
  + Expiry
* **Machines to update:**Select **Machines** option. All the Azure-hosted VMs will display under the **Type** drop-down list. Click on the VMs that need to be added in the update deployment. The selected VMs will be displayed under **the Selected items**section. Click **OK**.
* **Update classification:** Select the classification for type of updates need to install on the VM. By default, all classifications will be selected. Modify the classification to choose security and critical.

The classification types are below, categorized by the OS of the VM:

![](data:image/png;base64...)

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

* **Pre-scripts and Post-scripts:** Select the scripts to run before and after the deployment.

![NewUpdateDeployment2_thumb[5]](data:image/png;base64...)

* **Maintenance window (minutes):** Keep it as default.
* **Reboot options:** Select from the options listed below as per requirement. The suggested and default option is “Reboot if required. “
  + Reboot if required
  + Always reboot
  + Never reboot
  + Only reboot – will not install updates

Once specify all settings, select **Create**.

See the newly created update deployment under the **Update deployment** tab. It will show the next run time details and other settings that have been configured.

![](data:image/png;base64...)

18.11 View Results of an Update Deployment

To see the status of an update deployment, select the **Update deployments** tab under **Update management**. **“In progress”** indicates that deployment is currently running. When the deployment is completed, the status will show either “Succeeded” if each update was deployed successfully or “Partially failed” if there were errors for one or more of the updates.

To see all the details of the update deployment, click on the update deployment from available list.

![](data:image/png;base64...)

The **Machine update run status**will be categorized into several fields, and as shown in the image above.

19. Storage Management

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed Storage process, kindly refer to Storage runbook mentioned in the Document Call outs. | | |

20. Vulnerability Management

|  | **Information Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | Tenable.io is used for VA assessment (Scan) on Regular basis. | | |

Based on the vulnerability report we need to remediate the vulnerabilities ASAP and share the artifacts.

Vulnerability Scanning in LLD **Section 5.1.1.2.**

21. Tools

| Tool | Description | Requirements |
| --- | --- | --- |
| My Wizard | Monitoring |  |
| Tenable.io | Vulnerability Scan |  |
| Crowd strike | Antivirus |  |
| DevOps / Ansible | Configuration management |  |
| Veritas / Recovery service vault | Backup |  |
| SCCM / Azure Update | Patching |  |
| Azure Site Recovery | Disaster Recovery |  |
| Service Now | ITSM |  |
| My Nav | Migration |  |

22. Vendor Management & SLA

22.1 Azure case logging

AZURE enterprise support, log a case for Azure systems via AZURE. AZURE has four support plans for the customers. MSHS has Premium Support.

Below are the details on how to log case with Azure from Azure portal.

![](data:image/png;base64...)

22.2 Escalation Matrix

Microsoft Support Account Manager for MSHS is **Bill Pritchett** (bipritch@microsoft.com)

23. Contacts

23.1 CMS contacts

| Name | Role | Organization | Email |
| --- | --- | --- | --- |
| Annapurna Nayak  Souvik Battacharya | Linux Leads | CMS | a.balchandra.nayak@accenture.com  Souvik.battacharya@accenture.com |
| Naveen Achugatla | Service Lead | CMS | naveen.k.achugatla@accenture.com |
| Nilofer | Window Lead | CMS | nilofer.l.mujawar@accenture.com |
| Manoj Sharma | Azure Lead | CMS | m.k.sharm@accenture.com |

| Escalation Contact | | | |
| --- | --- | --- | --- |
| Thrivikraman Elayath | Delivery Manager | Offshore | thrivikraman.elayath@accenture.com |
| Taha Rashidi | Delivery Manager | Onshore | Taha.rashidi@accenture.com |
| Suprovat | Support Manager | Offshore | suprovat.sinha@accenture.com |

23.2 Build and Migration contacts

| **Name** | **Role** | **Email** |
| --- | --- | --- |
| **Cesar Ceniceros** | Foundation Build | cesar.ceniceros@avanade.com |
| **Jose Ivey** | Non – EPIC Migration | jose.ivey@accenture.com |
| **Zach Nemitz** | EPIC Migration | zach.c.nemitz@accenture.com |
| **Bryan Long** | DevOps | bryan.m.long@accenture.com |

23.3 Escalation Matrix Internal CMS

| **Escalation Level** | **Name** | **Email** |
| --- | --- | --- |
| **L1** | Tower Leads | MSHS.CMS.TowerLeads@accenture.com |
| **L2** | Vikram  Taha | Thrivikraman.elayath@accenture.com  Taha.rashidi@accenture.com |
| **L3** | KJ  BG | jayasankar.k.j@accenture.com  bharathi.ganesh.ns@accenture.com |
| **L4** | Neelam  Amit Gaur | neelam.l.gurbaxani@accenture.com  amit.gaur@accenture.com |

23.4 Escalation MSHS

| Escalation Level | Name | Email |
| --- | --- | --- |
| L1 | Joseph Brittelli  Andrew Pizzimenti | Joseph.Brittelli@mountsinai.org  andrew.pizzimenti@mssm.edu |
| L2 | Joseph Gimigliano | Joseph.Gimigliano@mountsinai.org |
|  |  |  |
|  |  |  |

24. SOP

**Please refer below link for the SOP:**

Adding server to domain click here

Post build activities click here

DR activities Fail over Fail back click here

File Recovery click here

RMT build click here

Note: Links will be updated once respective SOP’s are approved.

