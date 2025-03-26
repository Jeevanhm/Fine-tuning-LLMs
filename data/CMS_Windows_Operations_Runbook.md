

**CMS: Windows Runbook**

Document Control

| Version | Status | Date | Author | Summary of Change |
| --- | --- | --- | --- | --- |
| V 1.1 | Initial Draft | 15th March 2022 | Satheesh | Initial Draft |
| V 1.2 | Update Draft | 20th April 2022 | Satheesh | Content Update |
| V 1.3 | Update Draft | 14th May 2022 | Taha Rashidi | Content Update |
| V 2.0 | Update Draft | 28th June 2022 | Satheesh / Manoj | SCCM – sec 20Hardening Policies – sec 13.3Common Issues - sec 13.8.8 to 13.8.12Screenshots and Links updatedMonitoring Rules updated - sec 18.4 |
| V 2.1 | Update Draft | 5th Sept 2022 | Nilofer / Manoj | ITSM Process - 10.1  Updated POC details - 12.8.7  Added Post build steps - 15.19 and 15.20  Added Azure Update Patch Management steps - 19.1 and 19.2  Patching Communication Details updated - 19.16  Microsoft Escalation Matrix Updated - 26.2  CMS contacts updated - 27.1  Escalation Matrix Internal CMS updated - 27.3  RBAC groups  AD details & SMTP Relay - 14.0  Verify Server OU details - 15.12 |
|  |  | 16th August 2023 | Gangappa Hugge | Added MSSN support process |
|  |  | 24th August 2023 | Anshu Kumawat | Added Steps to delete Recovery Partition |
|  |  | 1st January 2024 | Anshu Kumawat | Added Steps to Create Service Health Alert in Azure |
|  |  | 24 January 2024 | Gangappa Hugge | Connexall Server Patching |
|  |  | 3rd January 2025 | Mahesh | Added steps for azure capacity process approval |
|  |  | 11th January 2025 | Anshu Dhaneria | Added troubleshooting step for backup failure. |

Document Approval Details

| Date | Version | Approver | Comments |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

Document Reviews

| Date | Company | Reviewer | Notes |
| --- | --- | --- | --- |
| 1st April 2022 | Accenture | Taha and Vikram | Provided Review comments on the structure, formatting, and operational activities. |
| 15th May 2022 | Accenture | KJ | Provided Review comments on the structure, formatting, and operational activities. |
| 4th July 2022 | Accenture | Hemant Kumar | Peer Review done |
| 8th July 2022 | Accenture | Taha/Vikram |  |

[2. About Client 7](#_Toc118808418)

[3. About Accenture 8](#_Toc118808419)

[4. Acronyms, Terminology, Appendix 9](#_Toc118808420)

[5. Document Call Outs 11](#_Toc118808421)

[6. Common URLs 12](#_Toc118808422)

[7. Scope 13](#_Toc118808423)

[7.1 In Scope of services 13](#_Toc118808424)

[7.2 Out of Scope of Services 13](#_Toc118808425)

[7.3 Decisions, Important Notes and Recommendations Reference 14](#_Toc118808426)

[8. Access 15](#_Toc118808427)

[8.1 Citrix VDI Access 15](#_Toc118808428)

[8.2 Azure Portal Access 15](#_Toc118808429)

[8.3 Virtual Server Access 15](#_Toc118808430)

[8.4 ServiceNow & CMS Distribution List 15](#_Toc118808431)

[9. Environment Details 16](#_Toc118808432)

[9.1 Azure VM Naming Standard 16](#_Toc118808433)

[9.2 Azure Virtual Machine Tagging 16](#_Toc118808434)

[9.3 Windows Operating System License 17](#_Toc118808435)

[9.4 Azure Regions 17](#_Toc118808436)

[10. Operations and Governance 19](#_Toc118808437)

[10.1 ITSM Functions 19](#_Toc118808438)

[11.Operating System Administration 20](#_Toc118808439)

[11.1 Virtual Machines Deployment (VMs) 20](#_Toc118808440)

[11.2 Operating Systems for Virtual Machines (VMs) 21](#_Toc118808441)

[11.3 Virtual Machines (VMs) Sizing 21](#_Toc118808442)

[11.4 Encryption 22](#_Toc118808443)

[11.5 Antivirus 22](#_Toc118808444)

[12. Operational Support 24](#_Toc118808445)

[12.1 Disk Management 24](#_Toc118808446)

[12.2 OS Hardening - System policy and Group policy flow process 34](#_Toc118808447)

[12.3 Mapped Shared Drive 35](#_Toc118808448)

[12.4 Allowed Traffic 36](#_Toc118808449)

[12.5 Task Scheduler 36](#_Toc118808450)

[12.6 Common Issues 40](#_Toc118808451)

[13. Server Provisioning and Decommissioning 49](#_Toc118808452)

[14. Join Server to Domain 50](#_Toc118808453)

[15. Post Server Build Steps 51](#_Toc118808454)

[15.1 Steps to check whether the server is joined to Active Directory 51](#_Toc118808455)

[15.2 Steps to check Tenable IO agent status: 51](#_Toc118808456)

[15.3 Steps to Re-Install Tenable: 51](#_Toc118808457)

[15.4 Steps to check/verify CrowdStrike agent 52](#_Toc118808458)

[15.5 Steps to check/verify Disk Encryption. 52](#_Toc118808459)

[15.6 Steps to turn off IE Enhance Security Configuration 52](#_Toc118808460)

[15.7 Steps to verify the server is updated in CMDB. 53](#_Toc118808461)

[15.8 Steps to verify the server is added to backup 54](#_Toc118808462)

[15.9 Steps to validate the IP Address 54](#_Toc118808463)

[15.10 Steps to validate the number of NIC attached: 55](#_Toc118808464)

[15.11 Steps to validate the RDP Access 55](#_Toc118808465)

[15.12 Validate OU of the server 57](#_Toc118808466)

[15.13 Steps to validate the Ports Open 57](#_Toc118808467)

[15.14 Steps to validate Disk Partition Drive Number 58](#_Toc118808468)

[15.15 Steps to validate Windows Firewall Status: 59](#_Toc118808469)

[15.16 Steps to identify the OS version: 59](#_Toc118808470)

[15.17 Steps to identify the VM System status 60](#_Toc118808471)

[15.18 SCCM Agent Verification 61](#_Toc118808472)

[15.19 Flexera Agent Verification 62](#_Toc118808473)

[15.20 My Wizard Agent Verification 62](#_Toc118808474)

[16. Networking 66](#_Toc118808475)

[17. Monitoring 67](#_Toc118808476)

[17.1 Monitor 67](#_Toc118808477)

[17.2 Creating Alert 69](#_Toc118808478)

[17.3 Log queries with Performance records 72](#_Toc118808479)

[17.4 Monitoring Rules to be configured in Azure Monitor: 73](#_Toc118808480)

[18. Backup & Restore 75](#_Toc118808481)

[19. Patch Management 76](#_Toc118808482)

[19.1 Azure Update - Schedule an Update Deployment 76](#_Toc118808483)

[19.2 View Results of an Update Deployment 79](#_Toc118808484)

[19.3 Deployment classification 80](#_Toc118808485)

[19.4 Patching Schedule to be decided 80](#_Toc118808486)

[19.5 Patching Approval Process 81](#_Toc118808487)

[19.6 Emergency or Adhoc Patching Process 81](#_Toc118808488)

[19.7 Rollback 82](#_Toc118808489)

[19.8 Patching Exception 82](#_Toc118808490)

[19.9 Patching Compliance Report 82](#_Toc118808491)

[19.10 Patching Communications 83](#_Toc118808492)

[19.11 Server Discovery Methods – Using SCCM 83](#_Toc118808493)

[20. Storage Management 84](#_Toc118808494)

[22. Vulnerability Remediation 85](#_Toc118808495)

[25. Tools 86](#_Toc118808496)

[26. Vendor Management & SLA 87](#_Toc118808497)

[26.1. Azure case logging 87](#_Toc118808498)

[26.2 Escalation Matrix 87](#_Toc118808499)

[27 Contacts 88](#_Toc118808500)

[27.1 CMS contacts 88](#_Toc118808501)

[27.2 Build and Migration contacts 88](#_Toc118808502)

[27.3 Escalation Matrix Internal CMS 89](#_Toc118808503)

[27.4 Escalation MSHS 89](#_Toc118808504)

[28. SOP 90](#_Toc118808505)

This document will act as a handbook which consists of all the technical procedures and processes that are required to support the MSHS Azure Windows Operations. The CloudOps Windows Operation team will leverage this document for all the processes, tools, procedures, and resources to perform day-to-day operations within the IT Infrastructure and provide world-class service to the business and end-users.

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
| Linux\_Operations\_Runbook | [Linux\_Operations\_Runbook](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ef7ro_AgHS1Lgzw_j08z2JEBSbx0Ev1bRuXnlyj7FvNp7A?e=pjLNDX) |
| Storage\_Operations\_Runbook | [Storage\_Operations\_Runbook](https://mtsinai.sharepoint.com/sites/CloudOperations-CMS/Shared%20Documents/General/Runbook/Azure%2C%20VMware%20%26%20Windows/CMS_Foundation_Runbook_v2.1.docx) |
| Backup\_Operations\_Runbook | [Backup Operations Runbook](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7B6417337E-C3B8-4CAF-8F48-C87B0009B376%7D&file=CMS_Backup_Operations_Runbook_v2.1.docx&action=default&mobileredirect=true) |
| Foundation\_Runbook | [Foundation\_Runbook](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ef7ro_AgHS1Lgzw_j08z2JEBSbx0Ev1bRuXnlyj7FvNp7A?e=pjLNDX) |
| CMS DR runbook | Link will be updated |
| HLD | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7BE01CD5B6-F1B0-4E5A-B71D-F24A118C7125%7D&file=AIL-2022.03_%20Azure_High-Level_Design_v008.docx&action=default&mobileredirect=true) |
| LLD | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7B21B35005-CE9A-4B50-8DB1-9F1DE76F7994%7D&file=AIL-2022.05_%20Azure_Low-Level_Design_v004.docx&action=default&mobileredirect=true) |
| DevOps | Link will be updated |

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

This Run Book covers basic operating guidelines and procedures necessary for administering and maintaining Windows Infrastructures. The scope of this document and work package is to:

|  |  | | |
| --- | --- | --- | --- |
|  |  |  |  |
| IS 1 | Systems Management (Windows Scope)   * Operating System Administration * Operating System Patch Management * Operating System Configuration and Support * Agent Installation * Vulnerability Remediation | | |
| IS 2 | Infrastructure monitoring and incident management   * Infrastructure monitoring and alert verification * Incident management and resolution | | |
| IS 3 | Service Request Fulfillment   * Provisioning, decommissioning and Modification the Azure IaaS environment | | |

Table 1 In Scope

7.2 Out of Scope of Services

|  |  | | | |
| --- | --- | --- | --- | --- |
|  |  |  |  |
| OOS 1 | Anything that is not mentioned in Scope (Section 8.1). | | | |

Table 2 Out of scope

7.3 Decisions, Important Notes and Recommendations Reference

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

|  | **Information Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | Dependency on LLD, KT or Deployment | | |

8. Access

8.1 Citrix VDI Access

First level of the access to Mount Sinai is via Citrix VDI using msnyuhealth.org domain and VIP Symantec MFA.

Link to access the Citrix VDI URL: <https://mountsinai.cloud.com/Citrix/StoreWeb/#/home>

8.2 Azure Portal Access

Post the access to Citrix VDI, Azure portal access is made using privilege account (PA) as per the Mount Sinai access guideline. No access to MSHS will be allowed through non-PA account.

CMS Cloud Foundation access to the **Azure Portal** is provided through the Active Directory **MSH-Cloud Foundation-ACN** group membership on the PA account.

8.3 Virtual Server Access

Virtual Server Access is via Citrix VDI using RDP. All Authentication must be done usingprivilege account (PA) as per the Mount Sinai access guideline. No access to MSHS will be allowed through non-PA account.

CMS Virtual Server access is provided through the Active Directory **MSH**-**WINTEL Server Local Administrators-ACN** group membership on the PA account.

8.4 ServiceNow & CMS Distribution List

In addition, CMS Support will hold the following ServiceNow Assignment & Team Distribution group for the day-to-day operation activity:

* ServiceNow Assignment group: **MSHS-Wintel-Migrate**
* CMS Support team Distributions: **CMS-Wintel@mountsinai.org** & **Mt.Sinai.CMS.Offshore.team@accenture.com**

9. Environment Details

9.1 Azure VM Naming Standard

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer to LLD mentioned in the link.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7B21B35005-CE9A-4B50-8DB1-9F1DE76F7994%7D&file=AIL-2022.05_%20Azure_Low-Level_Design_v004.docx&action=default&mobileredirect=true)  Design Decision on Naming Standard are available in LLD **Section 3.3**. | | |

9.2 Azure Virtual Machine Tagging

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | * Required tags will be defined within infrastructure deployment templates, ensuring resources are tagged at time of deployment * Tags will be monitored, controlled, and reported on as part of normal operations. * Common tags from Resource Groups will be inherited to all resources within the resource group. * Azure Policy will be used to audit resources missing required tags or with not-allowed values. Azure Policy can also enforce inheritance of common tags from the parent resource group. * Design Decision on Tag values are available in LLD **Section 3.7**. | | |

All resources deployed in Azure must have the following tags with associated values.

![](data:image/png;base64...)

9.3 Windows Operating System License

The following licensing models are the most common for enterprise deployments.

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | * For Lift & Shift (migration) – Hybrid * For Replat forming or new provisioning - Hybrid | | |

9.4 Azure Regions

Azure provides services across multiple geographic regions, each supported by multiple datacenters and availability zones. In some cases, these regions represent a resource boundary – for example, Certain Azure services, VM sizes are only available in certain regions.

|  | Architecture Decision | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | * Due to the availability of virtual machines, as well as other required services, the MSHS services for the Cloud Migration project will be provisioned in the following regions:   + Primary Region “East US”.   + Secondary Region “South Central US” | | |
|  | Azure Region is available in LLD **Section 3.2**. | | |

Region or Location

![](data:image/png;base64...)

|  | Important note | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Not all resource SKUs are available in all regions.  Approved list of SKUs available for MSHS is located – Link. | | |

10. Operations and Governance

10.1 ITSM Functions

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

11.Operating System Administration

11.1 Virtual Machines Deployment (VMs)

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | These general guidelines will be followed for virtual machine deployment to Azure:   * Avoid storing data on the OS disk. Instead create data disks, and in the case of databases ensure that caching is disabled. * Only store temporary data on the Temp Drive (Default Drive Letter D). There is no guarantee of data persistence for that drive. * VMs will be placed in availability sets to achieve a 99.95% uptime SLA, on a case-by-case basis. Requirements per application will be provided by the MSHS team. * VMs will be placed in availability zones to achieve a 99.99% uptime SLA, on a case-by-case basis. Requirements per application will be provided by the MSHS team. * Tag VMs with the metadata necessary to identify the owner, function, application, etc. * Deploy scale sets to achieve auto-scaling functionality for heavy-use applications with predictable loads. * It is required to use an endpoint protection solution on all Azure virtual machines. * Azure Managed disks are recommended for all VM’s * All virtual machines must be hardened to meet CIS Benchmark compliance of at least 90%. The CIS L1 controls script will be executed against all machines in the MSHS environment. * Azure Storage Service Encryption (ASSE) will be used for all storage. * Use database-level encryption for databases, in addition to ADE. * Design Decision on VM Deployment are available in LLD **Section 6.3.2** * Deploying VM’s through Azure Portal is not approved as per the MSHS Design. * CMS Team leverage Azure DevOps Service to support the identified DevOps objectives, and provision the environment using Devops pipeline * Deployment using DevOps will be covered in the Devops runbook which CMS team will refer for deployments. DevOps runbook link will be updated post the document is completed. | | |

11.2 Operating Systems for Virtual Machines (VMs)

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | MSHS Will Use latest Marketplace Image for OS Deployment  OS Hardening implemented via GPO. | | |

11.3 Virtual Machines (VMs) Sizing

There are predefined versions of the VM sizing available for MSHS Clients which are approved by MSS Standard

Users are listed only those lists of the approved VM sizing to be used for any new provisioning

“standard\_d4s\_v4",

"standard\_d8s\_v5",

"standard\_d4s\_v5",

"standard\_d8s\_v4",

"standard\_d2s\_v4",

"standard\_ds11\_v2",

"standard\_d2s\_v3",

"standard\_d4\_v2",

"standard\_d2s\_v5",

"standard\_ds3\_v2",

"standard\_e8s\_v5",

"standard\_e8ads\_v5",

"standard\_d8s\_v3",

"standard\_e4bds\_v5",

"standard\_d4s\_v3",

"standard\_e2bds\_v5",

"standard\_e104ids\_v5",

"standard\_d16s\_v5",

"standard\_e16s\_v5"

“standard\_D32\_v3”,
 “standard\_E8s\_v5”,
 “standard\_E8-2s\_v5",
 “standard\_E8-4s\_v5",
 “standard\_NC8as\_T4\_v3”,
 “standard\_F16s\_v2”,
 “standard\_F2s\_v2”,
 “standard\_F4s\_v2”,
 “standard\_F8s\_v2”,
 “standard\_F32s\_v2”,

11.4 Encryption

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | By default, all MSHS’s VM disks are encrypted with Azure Storage Service Encryption. For additional security, Microsoft recommends encrypting the Azure VM disks at the OS level using Azure Disk Encryption.  Design Decision on Azure Disk Encryption are available in LLD **Section 5.4.3.1.**  Design Decision on Storage Service Encryption are available in LLD **Section 5.4.3.2.** | | |

**Azure Disk Encryption**

Azure Disk Encryption (ADE) provides encryption of data at rest for both OS and data disks. Azure Disk Encryption utilizes the Bit Locker feature of Windows to encrypt at the volume-level of OS and data disks of virtual machines and virtual machine scale sets. For Linux machines, ADE uses the DM-Encryption feature to provide encryption. ADE is integrated with and relies upon Azure Key Vault to control and manage disk-encryption keys and secrets.

**Storage Service Encryption (SSE)**

Azure Storage Service Encryption (SSE) for data at rest of the Azure storage platform automatically encrypts the data before persisting it to Azure Managed Disks, Azure Blob, Queue, or Table storage, or Azure Files, and decrypts the data before retrieval. The handling of encryption, encryption at rest, decryption, and key management in SSE is transparent to users. All data written to the Azure storage platform is encrypted through 256-bit AES encryption. Storage Service Encryption is enabled for all new and existing storage accounts and cannot be disabled.

![](data:image/png;base64...)

11.5 Antivirus

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | For each MSHS subscription, Microsoft Defender for Cloud will be enabled to actively monitor the environment. Azure Defender will be automatically enabled for all resources except for endpoint protection and/or the OS agent for IaaS deployments, which will be protected with CrowdStrike.  The agent will be included and configured as part of the automation templates.  Design Decision for Microsoft defender available in LLD Section 5.1.1.4  Design Decision for Endpoint Protection (CrowdStrike) available in LLD Section 5.1.1.3 | | |

To validate that the sensor is running on a Windows host via the command line, run this command at a command prompt:

**sc query CSFalconService**

If see **STATE: 4 RUNNING**, CrowdStrike is installed and running.

![](data:image/jpeg;base64...)

12. Operational Support

12.1 Disk Management

|  | **Important note** | |
| --- | --- | --- |
|  |  |
| ! | * Activity to be performed based on the incident received in the Service Now or alert received using Azure Monitor or a service request raised by the business post the necessary approval. * Alerts threshold will be set based on the details mentioned below. * Drives to be extended on repetitive alert when there is no possibility of further housekeeping. 10 % can be added as part of blanket approval to avoid outage. * Unless use [resize without downtime (preview only supported for data disk)](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/expand-os-disk#resize-without-downtime-preview), resizing an OS or data disk of an Azure VM requires the VM to be deallocated (Stop). * Shrinking an existing disk isn’t supported and can potentially result in data loss. * After expanding the disks in Azure, we need to [expand the volume in the operating system](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/expand-os-disk#expand-the-volume-in-the-operating-system) to take advantage of the larger disk. * Adding / Resizing will be done via DevOps, we are providing manual steps for disk management in case needed. | |
| IMP Note | for servers in Azure only they are to be transferred to Utpal’s org for review   * for servers in Azure only they are to be transferred to Utpal’s org for review * Add storage to a VM in Azure * Add memory to a VM in Azure * Add disk to a VM in Azure   If there is an emergency that will cause an outage in Azure due to any of the above 3 conditions, you have my approval to add it immediately to avoid an outage.   * + If this happens, please cc JOe B, Jim, Deng and Utpal and get update   All tickets for the above should go into the queue below –   * MSHS-ARCH-ENG-DEVOPS | |

12.1.1 Add a data disk

1. Sign-in to the Azure portal.
2. Search for and select **Virtual machines**.
3. Select a virtual machine from the list.
4. On the **Virtual machine** pane, select **Disks**.
5. On the **Disks** pane, select **Create and attach a new disk**.
6. In the dropdowns for the new disk, make the selections as per the ticket, and name the disk by following approved naming conventions.
7. Select **Save** to create and attach the new data disk to the VM.

**Initialize a new data disk**

1. Connect to the VM.
2. Select the Windows **Start** menu inside the running VM and enter **diskmgmt.msc** in the search box. The **Disk Management** console opens.
3. Disk Management recognizes that we have a new, uninitialized disk and the **Initialize Disk** window appears.
4. Verify the new disk is selected and then select **OK** to initialize it.
5. The new disk appears **unallocated**. Right-click on the disk and select **New simple volume**. The **New Simple Volume Wizard** window opens.
6. Proceed through the wizard, keeping all the defaults, and when 're done select **Finish**.
7. Close **Disk Management**.
8. A pop-up window appears notifying that we need to format the new disk before can use it. Select **Format disk**.
9. In the **Format new disk** window, check the settings, and then select **Start**.
10. A warning appears notifying that formatting the disks erases all the data. Select **OK**.
11. When the formatting is complete, select **OK**.
12. ORC will be performed post this

12.1.2 Resize a disk

1. In the Azure portal, go to the virtual machine in which is needed to expand the disk. Select **Stop** to deallocate the VM.
2. In the left menu under **Settings**, select **Disks**.

![](data:image/png;base64...)

1. Under **Disk name**, select the disk that is needed to resize.
2. In the left menu under **Settings**, select **Size + performance**.

![](data:image/png;base64...)

1. In **Size + performance**, select the disk size as required.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | The new size should be greater than the existing disk size. The maximum allowed is 4,095 GB for OS-disks. (It's possible to expand the VHD blob beyond that size, but the OS works only with the first 4,095 GB of space.) | | |

![](data:image/png;base64...)

1. Select **Resize** at the bottom of the page.

![](data:image/png;base64...)

12.1.3 Expand the volume in the operating system

When the disk is expanded for the VM, go into the OS, and expand the volume to encompass the new space. There are several methods for expanding a partition. This section covers connecting the VM using an RDP connection to expand the partition using **Disk Manager.**

1. Start a remote desktop session with the VM.
2. Open **Disk Management**.

![Screenshot showing Disk Management.](data:image/png;base64...)

1. Right-click on existing **C:** drive partition -> Extend Volume.

![Screenshot showing how to extend the volume.](data:image/png;base64...)

1. Follow the steps to be able to see the disk with updated capacity:

![Screenshot showing the larger C: volume in Disk Manager.](data:image/png;base64...)

How to identify disk LUN number:

**Using Disk Manager**

1. Access Disk Manager under "Computer Management" in "Server Manager" or in the command prompt with diskmgmt.msc
2. Right-Click on the side-bar of the disk you wich to view and select "Properties"
3. ![](data:image/png;base64...)
4. You will see the LUN number and the target name. In this example it's "LUN 3" and "PURE FlashArray"

   ![](data:image/png;base64...)

**Using Command Line & diskpart**

Open a command prompt:

Start > Run > cmd

Start up the DISKPART utility:

C:\ Users\Administrators>diskpart

Select the disk you wish to view (example uses disk 1, it can be any valid disk number):

DISKPART> select disk 1

View the details of the selected disk:

DISKPART> detail disk

**In case you need to extend C, drive and C drive is having recovery partition present in disk management.**

Follow the steps below to Delete Healthy partition on Azure Migrated servers.

Recovery partition was required in physical servers for OS recovery, but it's not required once it's migrated in azure, hence this can be deleted and post that you can even extend C drive to higher value once C drive is having low space issues.

For example-

DISKPART> list disk

DISKPART> select disk 4

Disk 4 is now the selected disk.

DISKPART> list partition

Partition ### Type Size Offset

------------- ---------------- ------- -------

Partition 1 Primary 223 GB 1024 KB

Partition 3 Recovery 450 MB 223 GB

DISKPART> select partition 3

Partition 3 is now the selected partition.

DISKPART> delete partition override

DiskPart successfully deleted the selected partition.

Now check if the recovery partition is deleted.

DISKPART> list partition

Partition ### Type Size Offset

------------- ---------------- ------- -------

Partition 1 Primary 223 GB 1024 KB

**Approvals:**

**Process for No-Cost & Low-Cost Upgrades in Azure**

1. **Request for Cost Information**:
   1. CMS sends an email to Hank requesting cost details for the proposed upgrade.
2. **Providing Cost Information**:
   1. **Responsible**: Chao, Hank
   2. Hank reviews and provides the cost information to CMS.
3. **Decision Based on Cost**:
   1. **If the cost increase is ≤ $500/year (≤ $42/month)**:
      1. Hank informs CMS to proceed with the change.
      2. No additional approval is required.
   2. **If the cost increase is > $500/year (> $42/month)** (To Be Determined):
      1. **Using App Team’s Fund**: Approval is required from the App Team’s financial approver.
      2. **Using DTP Fund**: Approval is required from Rachel or Jeevan.

12.1.4 Housekeeping of C: drive

**Note: For any issue related to SQL has to be sent to SQL team looping POC in CC.**

**And rest all issues the email must go to POC**

**Clean-up of C: drive**

1. Delete the files inside the recyclebin.

2. Delete the files inside C:\Windows\softwaredistribution\download

3. Delete the files inside C:\Windows\Temp

4. Delete the files inside C:\Windows\installer\$PatchCache$\Managed

5. Delete old log files under C:\Windows\ccmcache

6. Delete unwanted files under C:\temp

7. Go to run, Type > %temp% > press OK --> Delete all files in the temp folder

8. Delete Unused Users Profiles

To reclaim disk space without replacing it with a new disk.

**Steps to free up disk space in Windows Server with Disk Cleanup:**

* 1. Press Windows and E together to open File Explorer, right click C: drive and select Properties.
  2. Click Disk Cleanup in the pop-up window

![](data:image/png;base64...)

* 1. Wait Disk Cleanup to scan the files that can be removed safely. (The time depends on server performance and the amount of junk files.)

![Scanning](data:image/png;base64...)

4. Click the checkboxes in front of the files that is to be deleted and then click OK.

![Select files](data:image/png;base64...)

5. Click Delete Files in the pop-up window to confirm and start deleting.

![Confirm](data:image/png;base64...)

**Defragmentation of the Drive:** Launch Defragmentation, Start è Defragmentation

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

You can either **analyze** or **optimize** the defragmentation of the drive you wish to defragment.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

* **Delete old Log files**

Based on the Incident ticket for C drive space issue.

1. Find the folder which is taking high space utilization.
2. Find the application owner and send mail for old log deletion approval
3. Post confirmation, attach the approval mail in incident ticket and delete the old logs

**Temp Folder Cleanup:**

Go to run, Type > **%temp%** > press OK

Delete all files in the temp folder

**Delete Unused Users Profile:**

**Step 1**: Go to advanced system settings (sysdm.cpl), advanced tab, click on settings in the user profiles box (middle of screen), under “profiles stored on this computer” click on the user profile you want to delete, and press Delete.

Or

**Using Control Panel**

1. Select **Start**, search for *Control Panel*, and select **Control Panel** in the result.
2. Select **Large icons** in **View by** and then select **System**.
3. Select the **Advanced System settings** link.
4. In the dialog that opens, select **Settings** in the **User Profiles** section.
5. In the next dialog, there is a list of profiles on the system. Select the profile that you want to remove and select **Delete**.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

**From registry:**

**Open the Registry editor**
Press the “Start” button and type “regedit”, then click “Run as administrator”.

**Navigate to the profile list in registry editor**

In the search bar or side menu, navigate to the profile list in registry editor, which is found at:

Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows NT\ProfileList

![Graphical user interface, text

Description automatically generated](data:image/png;base64...)

**Find the account in the profile list registry key**

The profile list registry key will have several SID keys for each user. To find the one you’re looking for, click on each and check the “Data” field next to the “ProfileImagePath” entry.

![](data:image/png;base64...)

**Delete the user profile registry key**

In the left-hand side menu, right-click the correct user SID and press “Delete”.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

**Confirm the user profile registry key deletion**

Make sure you’re deleting the key for the correct user before clicking “Yes”.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

12.2 OS Hardening - System policy and Group policy flow process

|  | **Architecture Decision** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | The following policies, processes and hardening will be implemented on servers in Azure.   * Utilize Security Configuration Wizard and Security Compliance Toolkit to create a secure, comprehensive, and consistent base DC build * Utilize GPOs to enforce Windows Firewall and other security configuration settings * Deny access to the Internet from both the local machine (web browsing) and perimeter firewalls * Adhere strictly to patch management policies * CrowdStrike will be used for endpoint protection in Azure and on-premises. The agent will be included and configured as part of the automation templates. * Tenable.io will be used for vulnerability scanning in Azure and on-premises. The agent will be deployed and configured as part of the automation templates*.* * Design Decision for Hardening are available in LLD **Section 5.3.2** * In case of vendor-built server, where app team requests to help in adding the server in domain, cyber security team’s approval is required | | |

**OU Details:**

For New Provisioning: Servers will be built in the designated OU

For Lift & Shift: Servers will be migrated to the designated OU mentioned above.

![image](data:image/png;base64...)

**AD Details:**

For New Provisioning: Servers will be joined to the domain post build as part of Post Installation Script.

For Lift & Shift: Servers will be already joined to the domain.

Forest root "**msnyuhealth.org**"
Child domain "mssm.edu"

Please refer to this [link](https://mtsinai.sharepoint.com/%3Ax%3A/s/CloudOperations-CMS/EVjZ8PIAyMlLvfZ1eZYEdlEBVe24qkHDNZBbKi0vClhQvw?e=EtF6aG) to know more about the OS Hardening policies.

For reference: Check **“Level 1 - Member Server**” sheets from the link provided.

**Four levels of priority for Group Policy:**

• Local Policy
• Site-level policies
• Domain-level policies
• OU-level policies

12.3 Mapped Shared Drive

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Activity to be performed based on the service request received in Service Now raised by the business to create and mount a File Share. Steps to create File Share is covered in the Storage Runbook. | | |

**Steps to perform:**

1. Click on the folder icon on the bottom of the screen in the task bar.
2. Click “Computer” depending on the windows operating system version.
3. On the top bar there should now be either of the following options. “Computer” or “Map Network
4. Please click on it and it will then display the “Map Network Drive”
5. This should now be presented with a box that looks like this
6. Provide the full FQDN with the share name <<\\FDQN\Share Name>>

![how to map a shared drive](data:image/png;base64...)

12.4 Allowed Traffic

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | All Network Traffic be flowing via Palo Alto firewall.  Any new port opening request will be processed by the palo alto firewall support up on the submission of Service Request or change. | | |

12.5 Task Scheduler

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | There should be a standard tool to schedule tasks Jobs such Control-M, Autosys (Out of Scope) or Azure Scheduler.  In case, it is required from the windows scheduler on exception basis (to be approved by the Service Owner of Windows), below steps need to be followed. | | |

**Below are the steps to create the schedule task:**

1. Give the new task a name and a description and click the Next button to continue

![choose Create Basic Task](data:image/png;base64...)

![give the task a name and a description](data:image/png;base64...)

1. The created task can be run daily, weekly, monthly, one time, when the computer starts, when log on or when a specific event is logged.

![choose the time to start the task](data:image/png;base64...)

1. Set the exact time for the task to run. Then click Next.

![set specified time intervals to run the task](data:image/png;base64...)

![choose Start a program click Next](data:image/png;base64...)

![click Finish after the task is created](data:image/png;base64...)

1. View the Schedule task

Open task manager.
Navigate to **File > Run new task**, type “**taskschd.msc**”, and click **OK**.

![open Task Scheduler within Task Manager](data:image/png;base64...)

![Manage Task Schedulers](data:image/png;base64...)

12.6 Common Issues

12.6.1 Sever Not Reachable

**Step 1:** login to Azure console, then search with the server’s name

![](data:image/png;base64...)

**Step 2:** Please check if the server is in Running state, if not then right click on server and start the server.

![](data:image/png;base64...)

**Step 3:** In case if the server is already in **Running** state, then try to login to Server Console.

If we find the server in **Hung** state, then we need to follow the process for Server Reboot to fix this issue.

12.6.2 Application or Service Hung Issues

1. For application-based services we will restart the service on best effort as per the agreed process with no further troubleshooting.

2. For Window's related service we will troubleshoot and make sure that service is running fine using the below mentioned steps

**Step 1:** Navigate to **Start > Run**, type “**services.msc**”, and click **OK**.

![](data:image/png;base64...)

Or by going to **Start> Run**, type “compmgmt.msc”, and click **OK**. This will open **the Computer Management** window and from here select **Services** tab.

![](data:image/png;base64...)

**Step 2:** Search for the in hung/stopped state. Right click the service and click on Start option to start the service.

![](data:image/png;base64...)

**Step 3:** After restarting the service, if it is still in Hung state, then look for dependency service within the “Dependencies” tab. From there once we find the dependency service, we need to kill those services from the task manger and once again we will get back to service console and start the service.

12.6.3 DNS resolution issue

For any issues with respect to DNS resolution, please raise a request by following the below steps. Fill out the fields and submit the request along with the hostname and IP address details

Service Now - [Link](https://mountsinaihealth.service-now.com/navpage.do)

Open Service now as per the link given above, Go to Service Catalog > Infrastructure > Servers > MSH Unix Engineering Request.
ServiceNow Assignment Group: MSHS-Unix Engineering.

Once the request is submitted, please send an email to the below mentioned POC’s:
***1. Valko, Andy <andy.valko@mssm.edu
2. Tempel, Philippe <philippe.tempel@mssm.edu***

12.6.4 CPU usage troubleshooting guidance

1. Using Azure Monitor,

**Step 1:** Log in to [Azure Portal](https://portal.azure.com/).

**Step 2:** Then go to the Virtual Machines and select the respective azure VM.

**Step 3:** After choosing the Azure VM, from left hand side of the page, navigate to Monitoring è select

**Metrics:**

![](data:image/png;base64...)

**Step 4:** Select **Scope à Required Azure VM**

* + Select **Metric Namespace** == **Virtual Machine Host**

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

* + Next, Choose the **Metric == “Percentage CPU” and Aggregation == “Avg”**

![](data:image/png;base64...)

* + Select Time Generated Number of Days as required

![](data:image/png;base64...)

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

In the same way if want data for the period requested.

![](data:image/png;base64...)

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

* 1. **Using Task Manager**
* Use Task Manager to view CPU consumption to help identify the process or application that's causing high CPU usage:
* Open the Task Manager by clicking “Start” and typing “Task Manager” into the search bar, or by using a keyboard shortcut by holding down Ctrl+Shift+Esc or Ctrl+Alt+Delete.

![](data:image/png;base64...)

* The Task Manager window defaults to the Processes tab.
* Select the CPU column header to sort the list by CPU usage. Make sure that the arrow that appears on the header points down to sort the data from highest to lowest CPU consumption.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

* If the process can be stopped, or a related service can be disabled, stop the process or the service. Then, check whether this mitigates the problem.

12.6.5 Memory Management

1. **Using Azure Monitor:**
   * + Go to specific VM
     + Search for the respective sever name for which we need to check the memory usage.
     + Go to INSIGHTS tab to monitor the Memory usage and performance within that server and we can get insights as in where the maximum memory is being consumed within the sever along with the timeline information.

![](data:image/png;base64...)

1. **Using Task Manager:**
   * + Open the Task Manager by clicking “Start” and typing “Task Manager” into the search bar, or by using a keyboard shortcut by holding down Ctrl+Shift+Esc or Ctrl+Alt+Delete.

![](data:image/png;base64...)

* + Click “More details” to expand to full view.
  + Navigate to the “Processes” tab and click the “Memory” header. This will sort all processes from most to least RAM usage.

![Graphical user interface, table

Description automatically generated](data:image/png;base64...)

* + From here, select and click on “End Task” for the processes or applications that consume more memory post getting necessary approvals.
  + For more details on the memory consumption, please open Resource Monitor from the task manager and check the memory usage details.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

12.6.6 Defender Issues:

After every login receiving following error : 0x80073b01

![](data:image/png;base64...)

Resolution:

The error is related to MS defender and is resolved as follows

* the machine has the latest OS patched and definition
* The machine has installed the new unified agent Microsoft Defender of Endpoint
* It was verified the also the machine as SCEP installed and running.
* The machine as 2 Anti-malware platform and engines running at the same time (SCEP and Unified agent Defender for Endpoint) **NOT RECOMMENDED**
* The MMA still has the workplace ID onboarded **NOT RECOMMENDED**
* Uninstall the SCEP service . and remove the MMA workplace ID.. because the machine is already with the Unified agent Microsoft defender Endpoint installed, Running and onboarded correctly and reporting well to the portal
* This will reflect an improvement in performance and remove the error that you are experiencing.
* Please restart the machine after these steps taken. ( not mandatory, but still recommended )

[**Onboard Windows servers to the Microsoft Defender for Endpoint service | Microsoft Learn**](https://urldefense.proofpoint.com/v2/url?u=https-3A__learn.microsoft.com_en-2Dus_microsoft-2D365_security_defender-2Dendpoint_configure-2Dserver-2Dendpoints-3Fview-3Do365-2Dworldwide-23windows-2Dserver-2D2012-2Dr2-2Dand-2Dwindows-2Dserver-2D2016&d=DwMGaQ&c=eIGjsITfXP_y-DLLX0uEHXJvU8nOHrUK8IrwNKOtkVU&r=bmaHICaR4XfFkbJrxwZFXSm5pgDarniHKfjSKELq8bj8iqd_AOxyqSGML9Rxk8Cz&m=XA0Ba07zvbnfFjRj93fiyniSPsjKvK2MjvjmSKwPkaiY5AnMAV3JNqv--A-EOeui&s=nFEQfwSlrNMJ38gH0xPXs-JAbgFYmNU-xIgZk9bptF8&e=)

13. Server Provisioning and Decommissioning

**Automation**

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | A Change Request is required for any change to a production system at MSHS. This includes changes like the following:   * Provisioning of new servers and services * Decommission of servers and services. * Configuration changes to the servers * Rebooting of Production servers (not technically a change but potentially service impacting so still tracked in Change Management)   The team will leverage Azure DevOps Service to support the identified DevOps objectives, and more specifically, deliver the Azure cloud infrastructure in an automated and repeatable manner.   * Server Provisioning process * Server Modification/Update process * Server Decommission process   For detailed ITSM workflow, kindly refer to Change Management process mentioned in the Operation and Governance Section.  If the information is unclear in the request, please seek clarification form requester before proceeding with decommissioning:   * ensure CIs in the decommissioning requests are clearly documented, * engage the DB team for verification when database servers are involved, and * require that decommissioning requests be raised or approved by the respective server/DB owner. | | |

|  | **Information Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | * **Server Provisioning process:**   Deployment Steps: will be covered as part of DevOps KT. | | |

1. **Physical Server:**

| Task | Activity | Owner |
| --- | --- | --- |
| Task 1 | Final Archival Backup/Remove server from backup Schedule | Backup Team |
| Task 2 | Blackout Monitoring for the servers | Server Team |
| Task 3 | Shutdown the server | Server Team |
| Task 4 | Cleanup Zoning/ Reclaim Storage (just unmap) | Storage Team |
| Task 5 | Remove from Network Monitoring | Network Team |
| Task 6 | Remove DNS record (Host & CNAME) | DNS Team |
| Task 7 | Delete the server Object | AD Team |
| Task 8 | Mark servers as Retired in CMDB | CMDB Team |
| Task 9 | Remove Server(s) from Monitoring | Monitoring Team |
| Task 10 | Remove server(s) from Patching | Servers Team |
| Task 11 | Remove from Vulnerability Management Database | IT security Team |
| Task 12 | Cleanup Zoning/ Reclaim Storage (Fully) | IT security Team |
| Task 13 | De-rack the Server in Data center | DC Ops team |

1. **Virtual Server:**

| Task | Activity | Owner |
| --- | --- | --- |
| Task 1 | Final Archival Backup/Remove server from backup Schedule | Backup Team |
| Task 2 | Shutdown the server | Server Team |
| Task 3 | Cleanup Zoning/ Reclaim Storage (if applicable) | Storage Team |
| Task 5 | Remove DNS record (Host & CNAME) | DNS Team |
| Task 6 | Delete the server Object | AD Team |
| Task 7 | Mark servers as Retired in CMDB | CMDB Team |
| Task 8 | Remove Server(s) from Monitoring | Monitoring Team |
| Task 9 | Add to ALL\_DECOM\_SERVERS | Servers Team |
| Task 10 | Release IP | Network Team |
| Task 11 | Remove from Vulnerability Management Database | IT security Team |
| Task 12 | Delete the Server | Servers Team |

1. **Azure Server**

| Task | Activity | Owner |
| --- | --- | --- |
| Task 1 | Final 30 days Backup | Backup Team |
| Task 2 | Remove Server(s) from Monitoring  (From myWizard) | Server Team |
| Task 3 | Shutdown the server from Azure portal & Disconnect Virtual Nic | Server Team |
| Task 4 | Mark servers as Retired in CMDB     (Raise SNOW request ?) | CMDB Team |
| Task 5 | Please add to ALL\_DECOM\_SERVERS for Patching | Servers Team |
| Task 6 | Delete the resource | MSHS-ARCH-ENG-DEVOPS |
| Task 7 | Delete the server Object (If applicable) | MSHS-AD & Messaging Engineering |
| Task 8 | Update the Pipeline | MSHS-ARCH-ENG-DEVOPS |
| Task | Please remove DNS record (Host & CNAME) & Release IP: Data, Backup & Mgmt. IP. | MSHS-Unix Engineering |

14. Join Server to Domain

|  | **Important Note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | * Dedicated Windows Server Active Directory domain controllers and Infoblox servers for DNS will be deployed. * MSHS will maintain their existing forest root “msnyuhealth.org” and child domain “mssm.edu”.   AD joined is covered in the LLD in the S**ection 5.3.1** | | |

**AD servers** created in the Azure Cloud (captured from the portal):

zeuspwaddc001 - 10.113.4.5

zeuspwaddc002 - 10.113.4.6

|  | **Information Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | * **Join Server to domain:**   Deployment Steps: will be covered as part of the DevOps KT. | | |

Domain Join manually,

1. On the **Start** screen, type **Control Panel**, and then press ENTER.
2. Navigate to **System and Security**, and then click **System**.
3. Under **Computer name, domain, and workgroup settings**, click **Change settings**.
4. On the **Computer Name** tab, click **Change**.
5. Under **Member of**, click **Domain**, type the name of the domain that wish this computer to join, and then click **OK**.
6. Click **OK**, and then restart the computer.

**SMTP relay details:**

| **Source Address**  **(System initiating the network communications)** | **Destination Address**  **(System listening for connection to the specified port)** | **Destination Protocol/Port** | **Rule: Add/Remove/Modify** | **Description**  **(Include a brief description of the type of traffic taking place over the listed port)** |
| --- | --- | --- | --- | --- |
| All Azure  MSH.azure | SMTP Relay  10.2.204.13 | smtp-starttls  smtp-base  smtp    tcp/25/587 | Add | SMTP Relay - mshrelay.mountsinai.org |

15. Post Server Build Steps

15.1 Steps to check whether the server is joined to Active Directory

MSHS domains are MSNY.Health.org and MSSM.EDU.Campus

**systeminfo | findstr /i "domain”** to check if server added to correct domain.

15.2 Steps to check Tenable IO agent status:

C:\Program Files\Tenable\Nessus Agent\nessuscli.exe <cmd> <arg1> <arg2>

| # nessuscli agent status | Displays the status of the agent, rule-based scanning information, jobs pending, and whether the agent is linked to the server.  **Optional arguments:**   * --local — (Default behavior) Provides the status, current jobs count, and jobs pending. This option prevents the agent from contacting its management software to fetch the status. Instead, it shows the last known information from its most recent sync. * --remote — (Default behavior) Fetches the job count from the manager and displays the status.   **Note:** Tenable does not recommend running frequent status checks with the --remote option (for example, when using automation).   * --offline — Provides the most recently cached agent status when it cannot connect to Nessus Manager or Tenable.io. * --show-token — Displays the agent's token that is used to identify and authenticate with its manager. * --show-uuid — Displays the agent's Tenable UUID. |
| --- | --- |

15.3 Steps to Re-Install Tenable:

1. Uninstall tenable from control panel
2. For migrated servers the installable is already present in the server at
   1. C:\temp\binar\*\*
3. Go to the binary and copy the path of the agent
4. Open command prompt as admin route you cmd path to the path of the agent
5. Then execute the command
6. msiexec.exe /i agent path NESSUS\_GROUPS="azure-win-server" NESSUS\_SERVER="cloud.tenable.com:443" NESSUS\_KEY="498546d69782c3d00bd04eeb9d22a0ab583e5762a588700a633cdc149f4ad876" /qn
7. You can do manual installation by double clicking the installable and point the following values when asked
   1. NESSUS\_GROUPS="azure-win-server
   2. NESSUS\_SERVER="cloud.tenable.com:443
   3. NESSUS\_KEY="498546d69782c3d00bd04eeb9d22a0ab583e5762a588700a633cdc149f4ad876

15.4 Steps to check/verify CrowdStrike agent

To validate that the sensor is running on a Windows host via the command line, run this command at a command prompt:

**sc query CSFalconService**

If see STATE: 4 RUNNING, CrowdStrike is installed and running.

![](data:image/jpeg;base64...)

15.5 Steps to check/verify Disk Encryption.

Verify the disks are encrypted: To check on the encryption status of an IaaS VM, use the [Get-AzVmDiskEncryptionStatus](https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus) cmdlet.

To [Sign in to the Azure account with Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/authenticate-azureps), use the [Connect-AzAccount](https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount) cmdlet.

Command: **Get-AzVmDiskEncryptionStatus -ResourceGroupName 'MyVirtualMachineResourceGroup' -VMName 'MySecureVM'**

15.6 Steps to turn off IE Enhance Security Configuration

Click on Server Manager on Local Server. **Turn off IE Enhanced Security Configuration** for administrators and users.

![Windows Server post installation configuration turn off IE Enhanced Security Configuration](data:image/png;base64...)

15.7 Steps to verify the server is updated in CMDB.

**Step1:** Go to ServiceNow

**Step2:** Select “Create an Incident”

**Step3:** Under Configuration Item tab, enter the server’s name and check if it is populating the server details.

**Step4:** If the details are populated, then the servers are updated in the CMDB.

![](data:image/png;base64...)

![](data:image/png;base64...)

15.8 Steps to verify the server is added to backup

In the Azure portal on the **Backup Items** pane, the list of protected VMs and last backup status with latest restore points time can be verified.

For detailed steps, kindly refer to Backup Runbook process document.

![](data:image/png;base64...)

15.9 Steps to validate the IP Address

* Log in to [Azure Portal](https://portal.azure.com/).
* Then go to the **Virtual Machines** and select the respective azure VM.
* In overview we can find the server IP address

![](data:image/png;base64...)

Navigate to **Start > Run**, type “**CMD**”, type **ipconfig -all** and click **OK**.

![](data:image/png;base64...)

15.10 Steps to validate the number of NIC attached:

From Azure VM properties, we can find the NIC details and can check if the NIC is enabled.

![](data:image/png;base64...)

Later from the server - Navigate to **Start > Run**, type “**NCPA.CPL**”, and click **OK**.

It will give the number of NIC’s attached along with the status

15.11 Steps to validate the RDP Access

Following are the steps to enable the RDP port in NSG

* Sign-in to the Azure portal.
* Then go to Virtual Machines, select the VM.
* In Settings, select Networking.
* In Inbound port rules, check whether the port for RDP is set correctly.
* Need to check if port 3389 is allowed or not, from the Azure console
* We need to create the incident request for port opening

![](data:image/png;base64...)

From server perspective, in the Server Manager window, click on Local Server in the left side panel.

The Remote Desktop option will be shown as Disabled in Windows 2019 version.

 ![](data:image/png;base64...)

Click on the **Disabled** option and this will open the **Remote** tab in the **System** **Properties** window.

Choose an option, as per requirement to enable or disable the access.

Specific access can be given to respective users.

![](data:image/png;base64...)

15.12 Validate OU of the server

**Check the Server OU details using PowerShell command (with admin privilege):**

 **([adsisearcher]"(&(name=$env:computername)(objectClass=computer))").findall().path**

15.13 Steps to validate the Ports Open

From Azure perspective, please check if the VM instance have correct NSG attached or not.

If the port is not enabled, raise a request as per standard process with Foundation team for NSG.

From server end, need to validate the specific number of ports open in the server by using the below mentioned command.

Navigate to **Start> Run**, type “**CMD**”, type **netstat -aon | find /i "listening"** and click **OK**

![](data:image/png;base64...)

15.14 Steps to validate Disk Partition Drive Number

Login to Azure Portal and search with server name. In overview we can find the disk details.

![](data:image/png;base64...)

Navigate to **Start > Run**, type “**CMD**”, click **OK**

Once the Command Prompt is open, type the command Disk part followed by List disk command to get the disk partition number

Along with list of disks, for a list of detected volumes. At the “DISKPART>” prompt, type list volume.

![](data:image/png;base64...)

15.15 Steps to validate Windows Firewall Status:

Navigate to **Start> Run**, type “**CMD**”, click **OK**

Once the Command Prompt is open, type this command to get Firewall status **“Netsh Advfirewall show allprofiles”**

![](data:image/png;base64...)

15.16 Steps to identify the OS version:

Go to Azure Console – Search the VM

Later from the Overview, required OS information can be validated.

![](data:image/png;base64...)

Within local server, navigate to **Start> Run**, type “**CMD**”, click **OK**

Once the Command Prompt is open, type this command **systeminfo | findstr /B /C:"OS Name" /C:"OS Version"**

![](data:image/png;base64...)

![](data:image/png;base64...)

15.17 Steps to identify the VM System status

Go to Azure Console -> search Server name –> from here we can see if the Server status if it’s in Running/Stopped state.

![](data:image/png;base64...)

15.18 SCCM Agent Verification

Login to server – go to Control Panel – Check if Configuration Manager is installed - If Configuration Manager is visible, then the SCCM Agent is installed.

![](data:image/jpeg;base64...)

![](data:image/jpeg;base64...)

Check the “**Configuration Manager service or SMSExec service, or just SMSExec service**” status on the server.

![](data:image/png;base64...)

15.19 Flexera Agent Verification

Login to server –> go to Control Panel –> Check for Flexera Agent

![](data:image/png;base64...)

15.20 My Wizard Agent Verification

**Splunk agent installation steps for windows**

1: - Download the Splunk agent for windows and keep it into the server C: drive. Please find the below link for reference.

<https://download.splunk.com/products/universalforwarder/releases/8.2.3/windows/splunkforwarder-8.2.3-cd0848707637-x64-release.msi>

2: - Open the command prompt as administrator and execute the command as mentioned below in the screenshots.

Sample command line.

**(msiexec.exe /i splunkforwarder-8.2.3-cd0848707637-x64-release.msi AGREETOLICENSE=YES DEPLOYMENT\_SERVER="10.113.2.22:8089" LOGON\_USERNAME="[DOMAIN\USERNAME]" LOGON\_PASSWORD="[SERVICEACCOUNTPASSWORD]" SET\_ADMIN\_USER=0 /quiet)**

![Graphical user interface, text

Description automatically generated](data:image/png;base64...)

**Manual Installation:**

Go to the Path having Setup file downloaded, Run the setup file

![](data:image/png;base64...)

Check the marked values, Click Next

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

Provide the service account credentials, Click Next

Next:

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

Provide the Deployment Server Hostname / IP and port (Default), Click Next.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

Click Install

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

Click finish

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

3: - Once command executed click here to ok.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

4: - Go to system services and open the Splunk properties.  Splunk status should be running state.

![](data:image/png;base64...)

5: - Go to Splunk forwarder properties and check the log on page, local account should be reflected once installation is done.

![](data:image/png;base64...)

6: - Open the control panel, go to program and features, Splunk agent status should be reflected.

![](data:image/png;base64...)

15.21 Update the Hardware configuration in Azure Hosted Services

For all requests noted below for servers in Azure only they are to be transferred to Utpal’s org for review.

* Add storage to a VM in Azure
* Add memory to a VM in Azure
* Add disk to a VM in Azure

Please take note of the following -

* As of today, this does not apply to on prem VMs (1425, NY6, NYEE, MSSN, SOM, SunGard)
* If there is an emergency that will cause an outage in Azure due to any of the above 3 conditions, you have my approval to add it immediately to avoid an outage.
  + If this happens, please cc me, Jim, Deng and Utpal to advise us

All tickets for the above should go into the queue below –

* MSHS-ARCH-ENG-DEVOPS

16. Networking

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed Network Design, kindly refer to LLD. [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7B21B35005-CE9A-4B50-8DB1-9F1DE76F7994%7D&file=AIL-2022.05_%20Azure_Low-Level_Design_v004.docx&action=default&mobileredirect=true)  This is covered in the LLD file S**ection 4.2.4**  For more information, refer to Foundation Runbook under Document Call Outs section. | | |

The proposed configuration provides a secure perimeter and network-based controls for services deployed to Azure.

**For example:**

* The network design will implement user-defined routes (UDRs) that will route internet-bound traffic to the next-gen firewalls for inspection and logging. For specific Azure services, internet-bound traffic will need to be routed directly to the internet. Those UDRs will be created accordingly.
* The network design will implement user-defined routes (UDRs) that will route cross-VNet traffic to the Palo Alto virtual appliances for inspection and logging, then to the destination.
* The network design will implement user-defined routes (UDRs) that will route intra-VNet traffic between subnets to the Palo Alto virtual appliances for inspection and logging, then to the destination.

17. Monitoring

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | * Azure Monitor will be used until My Wizard is deployed. | | |

Design Decision on Azure Monitor are available in LLD **Section 5.1.3.1.**

17.1 Monitor

From a management and monitoring perspective the Azure virtual machines can utilize Operations Management Suite (Log Analytics). Log Analytics provides detailed insights into virtual machines including, but not limited to:

* CPU utilization
* Memory utilization
* Network utilization
* Disk Utilization.

These VM metrics are displayed in Log Analytics through dashboard and tile views.

Azure Monitor collects monitoring telemetry from a variety of on-premises and Azure sources. Management tools, such as those in Azure Security Center and Azure Automation, also push log data to Azure Monitor. The service aggregates and stores this telemetry in a log data store that is optimized for cost and performance. Analyze data, set up alerts, get end-to-end views of the applications and use machine learning–driven insights to quickly identify and resolve problems.

![](data:image/jpeg;base64...)

**STEP BY STEP PROCEDURE FOR COLLECTING LOG DATA AND SETTING UP ALERTS**

**Collecting event and performance data:**

Log Analytics can collect events from the Windows event log and performance counters that specify for longer term analysis and reporting and act when a particular condition is detected. Follow these steps to configure collection of events from the Windows event log, and several common performance counters to start with.

1. In the Azure portal, click **More services** found on the lower left-hand corner. In the list of resources, type **Log Analytics**. As begin typing, the list filters based on the input. Select **Log Analytics**.
2. Select **Advanced settings**.

![](data:image/png;base64...)

1. Select **Data**, and then select **Windows Event Logs**.
2. Here, adds the Health Service event channel by typing in the name below and then click the plus sign **+**.

**Event Channel: Microsoft-Windows-Health/Operational**

1. In the table, check the severities **Error** and **Warning**.
2. Click **Save** at the top of the page to save the configuration.
3. Select **Windows Performance Counters** to enable collection of performance counters on a Windows computer.
4. During the configuration of Windows Performance counters for a new Log Analytics workspace, the option is available to quickly create several common counters. They are listed with a checkbox next to each.

![](data:image/png;base64...)

Click **Add the selected performance counters**. They are added and preset with a ten second collection sample interval or select the Custom Log Search. Then provide the Custom Query

Perf

| where ObjectName == “LogicalDisk” and CounterName == “% Free Space” and InstanceName == “C:”

| summarize arg\_max(TimeGenerated, \*) by InstanceName

* 2. Save the query and select the SIGNAL in the condition.
  + Save the query in Logs pane.

Sample to collect Free space for C drive

1. Click **Save** at the top of the page to save the configuration.

17.2 Creating Alert

**Steps for creating an alert.**

1. In the Azure portal, click **All services**. In the list of resources, type **Log Analytics.**
2. In the left-hand pane, select **Alerts** and then click **New Alert Rule** from the top of the page to create a new alert.

![](data:image/png;base64...)

1. For the first step, under the **Create Alert** section, select Log Analytics workspace as the resource, since this is a log-based alert signal. Filter the results by choosing the specific **Subscription** from the drop-down list, which contains Log Analytics workspace created earlier. Filter the **Resource Type** by selecting **Log Analytics** from the drop-down list. Finally, select the **Resource** **DefaultLAWorkspace** and then click **Done**.

![](data:image/png;base64...)

1. Under the section **Alert Criteria**, click **Add Criteria** to select saved query and then specify logic that the alert rule follows.
2. Configure the alert with the following information: a. From the **Based on** drop-down list, select **Metric measurement**. A metric measurement will create an alert for each object in the query with a value that exceeds our specified threshold. b. For the **Condition**, select **Greater than** and specify a threshold. c. Then define when to trigger the alert.

For example, select **Consecutive breaches** and from the drop-down list select **Greater than** a value of 3. d. Under Evaluation based on section, modify the **Period** value to **30** minutes and **Frequency** to 5. The rule will run every five minutes and return records that were created within the last thirty minutes from the current time. Setting the time to a wider window account for the potential of data latency and ensures the query returns data to avoid a false negative where the alert never fires.

1. Click **Done** to complete the alert rule.

![](data:image/png;base64...)

1. Now moving onto the second step, provide a name of alert in the **Alert rule name** field, such as **Alert on all Error Events**. Specify a **Description** detailing specifics for the alert and select **Critical (Sev 0)** for the **Severity** value from the options provided.
2. To immediately activate the alert rule on creation, accept the default value for **Enable rule upon creation**.
3. For the third and final step, specify an **Action Group**, which ensures that the same actions are taken each time an alert is triggered and can be used for each rule defined.

   **Configure a new action group with the following information:**
   a. Select **New action group** and the **Add action group** pane appears.
   b. For **Action group name**, specify a name such as **IT Operations - Notify** and a **Short name** such as **itops-n**.
   c. Verify the default values for **the Subscription** and **Resource group** are correct. If not, select the correct one from the drop-down list.
   d. Under the Actions section, specify a name for the action, such as **Send Email** and under **Action Type** select **Email/SMS/Push/Voice** from the drop-down list.

   The **Email/SMS/Push/Voice** properties pane will open to the right to provide additional information.

   e. On the **Email/SMS/Push/Voice** pane, select and set up the agreed process which is Email.
   For example, enable **Email** and provide a valid email SMTP address to deliver the message to

   f. Click **OK** to save the changes.

![](data:image/png;base64...)

1. Click **OK** to complete the action group.
2. Click **Create alert rule** to complete the alert rule. It starts running immediately.

![](data:image/png;base64...)

17.3 Log queries with Performance records

The following table provides different examples of log queries that retrieve Performance records.

| Description | Query | |
| --- | --- | --- |
| All Performance data | Perf | |
| All Performance data from a particular computer | Perf | where Computer == "MyComputer" | |
| All Performance data for a particular counter | Perf | where CounterName == "Current Disk Queue Length" | |
| Average CPU Utilization across all computers | Perf | where ObjectName == "Processor" and CounterName == "% Processor Time" and InstanceName == "\_Total" | summarize AVGCPU = avg(CounterValue) by Computer | |
| Maximum CPU Utilization across all computers | Perf | where CounterName == "% Processor Time" | summarize AggregatedValue = max(CounterValue) by Computer | |
| Average Current Disk Queue length across all the instances of a given computer | Perf | where ObjectName == "LogicalDisk" and CounterName == "Current Disk Queue Length" and Computer == "MyComputerName" | summarize AggregatedValue = avg(CounterValue) by InstanceName | |
| 95th Percentile of Disk Transfers/Sec across all computers | Perf | where CounterName == "Disk Transfers/sec" | summarize AggregatedValue = percentile(CounterValue, 95) by Computer | |
| Hourly average of CPU usage across all computers | Perf | where CounterName == "% Processor Time" and InstanceName == "\_Total" | summarize AggregatedValue = avg(CounterValue) by bin(TimeGenerated, 1h), Computer | |
| Hourly 70 percentile of every % percent counter for a particular computer | Perf | where Computer == "MyComputer" and CounterName startswith\_cs "%" and InstanceName == "\_Total" | summarize AggregatedValue = percentile(CounterValue, 70) by bin(TimeGenerated, 1h), CounterName | |
| Hourly average, minimum, maximum, and 75-percentile CPU usage for a specific computer | Perf | where CounterName == "% Processor Time" and InstanceName == "\_Total" and Computer == "MyComputer" | summarize ["min(CounterValue)"] = min(CounterValue), ["avg(CounterValue)"] = avg(CounterValue), ["percentile75(CounterValue)"] = percentile(CounterValue, 75), ["max(CounterValue)"] = max(CounterValue) by bin(TimeGenerated, 1h), Computer | |
| Perf | where ObjectName == "Memory" and CounterName == "% Committed Bytes In Use" | summarize AggregatedValue = avg(CounterValue) by Computer, bin(TimeGenerated, 2m) | Azure Windows VM Memory usage | **Perf | where ObjectName == "Memory" and CounterName == "% Committed Bytes In Use" | summarize AggregatedValue = avg(CounterValue) by Computer, bin(TimeGenerated, 2m)** |
| All Performance data from the Database performance object for the master database from the named SQL Server instance INST2. | **Perf | where ObjectName == "MSSQL$INST2:Databases" and InstanceName == "master"** | |

17.4 Monitoring Rules to be configured in Azure Monitor:

As interim solution the below monitoring thresholds are configured. These thresholds will be optimized and updated based on the feedback from MSHS POC (Discussion in progress).

**Interim Threshold (temp)**

**Windows OS Baseline\_Prod**

| Host: Reporting no data (Availability Up/Down) | Down | Major (P2) | NA | NA |
| --- | --- | --- | --- | --- |
| Memory Usage | ≥ 90% | Minor(P3) | ≥ 95% | Major (P2) |
| CPU utilization | ≥ 90% | Minor(P3) | ≥ 95% | Major (P2) |
| Disk Space Usage | ≥ 90% | Minor(P3) | ≥ 95% | Major (P2) |

**Windows OS Baseline\_Non\_Prod**

| Host: Reporting no data (Availability Up/Down) | Down | Major(P3) | NA | NA |
| --- | --- | --- | --- | --- |
| Memory Usage | ≥ 95% | Minor(P4) | ≥ 98% | Major(P3) |
| CPU utilization | ≥ 95% | Minor(P4) | ≥ 98% | Major(P3) |
| Disk Space Usage | ≥ 90% | Minor(P4) | ≥ 90% | Major(P3) |

17.5 Onboarding Servers in MyWizard

* 1. We collate the data
  2. Create ticket with mywizard teamto onboard the servers to MyWizard

17.6 Creating Blackout in MyWizard

1. Login into Splunk console.

2. Click on MyWizard AiOps Stack Monitoring Suite. Go to configwizrd Blackout.

![](data:image/png;base64...)

* 1. Create blackout, import the server list, set the key and metric value, and provide the date and time.

![](data:image/png;base64...)

![](data:image/png;base64...)

* 1. Add the server list and click on Metric tab and put the \* value to sprees all kinds of alerts.

![](data:image/png;base64...)

5 Schedule the date and time and configured.

![](data:image/png;base64...)

18. Backup & Restore

**18.1 Steps to Troubleshoot Error Code: GuestAgentSnapshotTaskStatusError for Windows VM During Backup**

**Error Details**

* **Error Code**: GuestAgentSnapshotTaskStatusError
* **Error Message**:

[00000031] 2025-01-08T07:38:01.487Z [WARN] Status file C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot\1.0.92.0\Status\792.status is not available for the Extension '' yet.

[00000038] 2025-01-08T07:38:10.014Z [WARN] Trying to download VMSettingsProfile with etag 13033797738084609833

[00000038] 2025-01-08T07:38:10.026Z [INFO]VMSettingsConsistenceCheckIfFabricSource Passed.

**Action Plan**

**Step 1: Analyze Logs**

1. Review the logs to identify missing or corrupted files.
   1. Example of a missing file:
       C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot\1.0.92.0\Status\792.status

**Step 2: Access a Non-Affected Server**

1. Log in to a **working server** (non-affected environment).
2. Navigate to the directory:

C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot

**Step 3: Copy Required Folders**

1. Copy the entire folder from the working server:

C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot

1. Log in to the **non-working server**.
2. Rename the existing folder on the non-working server to mark it as old:

C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot.old

1. Paste the copied folder from the working server into the same directory on the non-working server.

**Step 4: Reinstall the Extension**

1. Open an **elevated Command Prompt** on the non-working server.
2. Run the following command to enforce reinstallation of the backup extension:

REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgent" /v IsProviderInstalled /t REG\_SZ /d False /f

**Step 5: Re-trigger the Backup**

1. Log in to the **Azure Portal**.
2. Navigate to the affected VM's backup settings.
3. Re-trigger the backup operation from the Azure Portal.

**Step 6: Verify the Resolution**

1. Confirm that the backup completes successfully.
2. Check the logs to ensure the error no longer persists.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed Backup & Restore process, kindly refer to Backup runbook – check the Document Call out section.   * Back up Azure VMs in a Recovery Services vault * Install the VM agent on the VM: Azure Backup backs up Azure VMs by installing an extension to the Azure VM agent running on the machine. If the VM was created from an Azure Marketplace image, the agent is installed and running. If create a custom VM, or migrate an on-premises machine, might need to [install the agent manually](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-vms-prepare#install-the-vm-agent) | | |

19. Patch Management

This Section covers Patch management using Azure Update manager, SCCM POC Completed Successfully.

Document preparation in progress for SCCM.

This section covers for the Windows Server environment and applicable for Operating System patching - like Windows Server 2016 & 2019.

Design Decision on Patch Management are available in LLD **Section 5.1.2.**

19.1 Azure Update - Schedule an Update Deployment

**Until SCCM can be used for Patch Update, we will be using Azure Update manager for patching Windows and Linux Servers.**

**Step 1**: To schedule an update deployment, open the automation account.
**Step 2:** In the left menu, select **Update Management**. The update Management window will open.
**Step 3:** Under the **Machines** tab, all the machines connected to the automation account through the linked workspace will be displayed. Under the **Update Deployments** tab, the status of past scheduled deployments will be visible.
**Step 4:** Under the **Schedule update deployment**tab, a list of upcoming and completed deployments will be listed.
**Step 5:** In this step, schedule the new deployment for specific VMs or multiple VMs at once, select the update classification, include, or exclude certain updates, and specify the schedule.

Select **Schedule update deployment**. The **New update deployment**window will open, and specify the following information:

* **Name:** Enter a unique name for the update deployment.
* Add the VM's to the Automation Account for the Environment Subscription.
* **Operating system:** Select the operating system (OS) (Windows or Linux) based on the VMs.
* **Groups to update (preview):** Select the subscription and select edit option, Once the edit option opens select the Patch Schedule Tag.

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

| **Servers** | **Classification** |
| --- | --- |
| Windows Servers | Critical Updates |
| Windows Servers | Security Updates |

![](data:image/png;base64...)

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

19.2 View Results of an Update Deployment

To see the status of an update deployment, select the **Update deployments** tab under **Update management**. **“In progress”** indicates that deployment is currently running. When the deployment is completed, the status will show either “Succeeded” if each update was deployed successfully or “Partially failed” if there were errors for one or more of the updates.

To see all the details of the update deployment, click on the update deployment from available list.

![](data:image/png;base64...)

The **Machine update run status**will be categorized into several fields, and as shown in the image above.

19.3 Deployment classification

The next step is to schedule an update deployment

The classification types are below, categorized by the OS of the VM:

| **Servers** | **Classification** |
| --- | --- |
| Windows Servers | Critical Updates |
| Windows Servers | Security Updates |

**Include/exclude updates:** In this section, include or exclude the patches as per the requirement.

19.4 Patching Schedule to be decided

Follow the standard maintenance window. Need to ensure patching occurs in lower environments (DEV and TST) prior to production environment (PRD).

**Maintenance Window for Windows OS (Non-DMZ):**

The below schedules in table are for DEV, TST and PRD tier instances

| **Environment** | **Maintenance Window (UTC+8 Time)** | **Tags** |
| --- | --- | --- |
| Windows Dev instances | Schedule 1: Saturday following 2nd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: D-W-S1 |
| Schedule 2: Sunday following 2nd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: D-W-S2 |
| Windows Test instances | Schedule 1: Saturday following 3rd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: T-W-S1 |
| Schedule 2: Sunday following 3rd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: T-W-S2 |
| Windows Prod instances | Schedule 1: Saturday following 4th Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: P-W-S1 |
| Schedule 2: Sunday following 4th Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: P-W-S2 |
| Schedule 3: 1st Saturday of next calendar Month, 1 AM, 5 hours window | Key: Patch; Value: P-W-S3 |
| Schedule 4: 1st Sunday of next calendar Month, 1 AM, 5 hours window | Key: Patch; Value: P-W-S4 |
| Windows Instances/Appliance | No Schedule | Key: Patch; Value: Exclude Patch |

**Maintenance Window for Windows OS (DMZ):**

The below schedules in table are for DEV, TST and PRD tier instances

| **Environment** | **Maintenance Window (UTC+8 Time)** | **Tags** |
| --- | --- | --- |
| Windows Dev instances | Schedule: Thursday following 2nd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: D-W-S3 |
| Windows Test instances | Schedule: Friday following 2nd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: T-W-S3 |
| Windows Prod instances | Schedule 1: Saturday following 2nd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: P-W-S5 |
| Schedule 2: Sunday following 2nd Tuesday of Each Month, 1 AM, 5 hours window | Key: Patch; Value: P-W-S6 |

19.5 Patching Approval Process

The Patching Approval process will go through the Change Control process IT Service Management (ITSM) - Change Management and will require a Change Request approval from CAB team.

A change request with applicable patches in Service Now for Linux and Windows VM instances for the patching window will be created and taken through the Change Control process.

| Responsible Role | Activity |
| --- | --- |
| CMS | A change request will be raised and seek approval as per - IT Service Management (ITSM) - Change Management. |
| Application Owner | Not required as it is scheduled based on request and pre-approval. |
| MSHS Cloud Operations Lead | Not required as it is scheduled based on request and pre-approval. |
| CAB Approver | Reviews and approves the emergency patching change request. |
| CMS | Following approval, the email notification will be sent to the stakeholders and patching would be executed for any specific reason or to remediate a patching failure at appropriate maintenance window. |

19.6 Emergency or Adhoc Patching Process

In the event a system must be patched outside of the patching (zero-tolerance critical patch release by vendor), following process should be followed.

| Responsible Role | Activity |
| --- | --- |
| CMS | An emergency change request will be raised and seek approval as per - IT Service Management (ITSM) - Change Management. |
| Application Owner | Reviews and approves the emergency patching change request. |
| MSHS Cloud Operations Lead | Reviews and approves the emergency patching change request. |
| CAB Approver | Reviews and approves the emergency patching change request. |
| CMS | Following approval, the email notification will be sent to the stakeholders and patching would be executed for any specific reason or to remediate a patching failure at appropriate maintenance window. |

19.7 Rollback

| Responsible Role | Activity |
| --- | --- |
| CMS | Update Management does not offer any patch rollback option.  System will be restored from the latest backup, in case of any rollback is required.  Example: System failure post patching activities. |

19.8 Patching Exception

| Responsible Role | Activity |
| --- | --- |
| CMS | All servers with specific tag key “**Exclude**” in the patch schedule tag will be Excluded from Patching. |
| Application Owner | * Any existing or newly introduced system in Landing Zone, which deviates from the patching guidelines in this Runbook must gain exception approval. * Any system owner who requires their servers be excluded from the patching guidelines in this Runbook will gain exception approval before that server is excluded from patching.   All exceptions will be submitted and approved via ServiceNow.  The ServiceNow catalog item to be submitted.  Note: The server needs to be excluded from the update deployment schedule. |
| Application Owner | Any ad-hoc exceptions that cannot adhere to the Patching Exception process will need the email approval from MSHS Cloud Operations lead to be excluded from scheduled patching. The Application Owner will be required to formally request exception approval through the Patching Exception process as defined above. |
| Cloud Operations Engineer | Systems that received Adhoc exception approval will be re-added to the patch schedule after the exception period agreed to by the MSHS Cloud Operations lead.  Any system that has formal patching exception approval and needs to be re-introduced into the patching schedule will require approved RITM submitted by Application Owner. |

19.9 patching Connexall servers

Reference Ticket: CHG0075253- Connexall server patching

| **Server Name** | **Ip Address** | **Other** | **ILO Details** | **Vcenter** |
| --- | --- | --- | --- | --- |
| SCNXAPPP018001 | 10.9.49.21 | Virtual Server | NA | svmwvcip018001 |
| scnxbkpp019001 | 10.9.49.22 | Virtual Server | NA | svmwvcip018001 |
| SCNXAPPP018003 | 10.9.49.23 | Virtual Server | NA | svmwvcip018001 |
| Scnxappp516001 | 10.15.129.58 | Physical Server | 10.15.128.58 | NA |
| Scnxappp516002 | 10.15.129.59 | Physical Server | 10.15.128.59 | NA |

1. Login to Vcenter <https://svmwvcip018001.msnyuhealth.org/> with pa credentialàSearch server “SCNXAPPP018001” àSelect the server à Open web console.

![](data:image/png;base64...)

![Inserting image...](data:image/png;base64...)

1. Now Login the server with pa credential à Go to start, select runàNavigate to the central location ([\\10.113.2.54\c$](file://10.113.2.54/c%24)), if it prompt for credential then provide pa account credential à copy the required month patches from below path and paste inside server.

![](data:image/png;base64...)

![](data:image/png;base64...)

1. Double click on patch which was pasted on the server (SCNXAPPP018001) and install it.
2. Repeat step 1 to 3 for rest two server “scnxbkpp019001 and SCNXAPPP018003”.
3. Do not reboot the server, we need to inform requester to reboot it.
4. Now login to physical server Scnxappp516002 through ILO IP: 10.15.128.59 with user name: \*\*\*\*\* and password: \*\*\*\*\*\* (Insert https:// 10.15.128.59 in web browser

![](data:image/png;base64...)

![](data:image/png;base64...)

1. Go to server management àSelect remote control.

![](data:image/png;base64...)

1. Check mark the box (Allow others to request my remote session disconnect) and click start remote control in multiple user mode.

![](data:image/png;base64...)

1. New web page will open in few seconds àSelect ctrl-Alt-DelàClick send

![Inserting image...](data:image/png;base64...)

1. Now login the server with pa credential à Go to start, select runà Navigate to the central location ([\\10.113.2.54\c$](file://10.113.2.54/c%24)), if prompt for credential then provide pa account credential à Copy the required month patches from below path and paste inside server.

![](data:image/png;base64...)

1. Double click on patch which was pasted on the server and install it.
2. From the above ILO server (10.15.128.59), access other physical serverà Go to Start àSelect Remote desktop connectionàInsert server name “Scnxappp516001” not IP.

![](data:image/png;base64...)

1. Repeat step 10 and 11.
2. Do not reboot the server, we need to inform requester to reboot it.
3. Drop mail to requester once patches are installed, so requester will perform reboot
4. Drop mail to requester once patches are installed, so requester will perform reboot

Please find jump server SCNXAPPT018006 to access all the 5 server through Remote Desktop Connection. Use IP address to access physical server.

**Important point to be noted:**

1)Server reboot will be handled by requester.
2)Pre and post communication mail must be sent before and after activity.
 3)If patches are not available on central location, then download require month patches from Microsoft site: “[Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Home.aspx)

19.10 Patching Compliance Report

| Responsible Role | Activity |
| --- | --- |
| CMS | The overall patch compliance summaries can be in the navigation pane of the **Update management center**.  The values displayed for each column are:   | **Field Name** | **Description** | | --- | --- | | Machine Name | Name of the machine attached to Update Management. | | Compliance | State of the system's compliance with security and critical updates. | | Update agent readiness | View the health of the update agent. If there's an issue, select the link to go to troubleshooting documentation that can help you correct the problem. | | Platform | Lists the platform as either Azure or non-Azure. | | Operating system | Lists the operating system as either Windows or Linux. | | Critical missing updates | Count of missing critical updates. | | Security missing updates | Count of missing security updates. | | Other missing updates | Count of non-security and non-critical updates. | | Update approval source | The source of updates. Either Windows update, WSUS, and Microsoft update *applicable to Windows*. | | Windows auto update | Default OS update setting on the machine *applicable to Windows*. | |

19.11 Patching Communications

| Responsible Role | Activity |
| --- | --- |
| CMS | **Pre-Patching Communication:**  Application Owners will be notified through manual email communication on patching activity 48 hours, 24hours and 2hours prior to the scheduled window, post the change request is approved by the CAB.  **Post-Patching Communication:**  Application Owners will be notified through manual email communication on patching activity status within 24 hours. |

Template for patch communication to Mount Sinai VM Owners

![](data:image/x-emf;base64...)

19.12 Server Discovery Methods – Using SCCM

Other Scenario to patch the servers is via SCCM Server (DP’s)

For patching using SCCM will be covered in the SCCM Guide, link will be provided soon.

19.13 Login Details for Connexall servers

The below mentioned servers are behind GE Firewall, kindly try to login with SCNXAPPT018006 server to login below servers and try to login with IP Address for below servers.

| Scnxappp516001 | 10.15.129.58 |
| --- | --- |
| Scnxappp516002 | 10.15.129.59 |

20. My Wizard Monitoring

20.1 C drive Clean-up incident

1. Delete the files inside the recyclebin.

2. Delete the files inside C:\Windows\softwaredistribution\download

3. Delete the files inside C:\Windows\Temp

4. Delete the files inside C:\Windows\installer\$PatchCache$\Managed

5. Delete old log files under C:\Windows\ccmcache

6. Delete unwanted files under C:\temp

7. Go to run, Type > %temp% > press OK --> Delete all files in the temp folder

8. Delete Unused Users Profiles

To reclaim disk space without replacing it with a new disk.

**Steps to free up disk space in Windows Server with Disk Cleanup:**

* 1. Press Windows and E together to open File Explorer, right click C: drive and select Properties.
  2. Click Disk Cleanup in the pop-up window

![](data:image/png;base64...)

* 1. Wait Disk Cleanup to scan the files that can be removed safely. (The time depends on server performance and the amount of junk files.)

![Scanning](data:image/png;base64...)

4. Click the checkboxes in front of the files that is to be deleted and then click OK.

![Select files](data:image/png;base64...)

5. Click Delete Files in the pop-up window to confirm and start deleting.

![Confirm](data:image/png;base64...)

**Defragmentation of the Drive:** Launch Defragmentation, Start è Defragmentation

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

You can either **analyze** or **optimize** the defragmentation of the drive you wish to defragment.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

* **Delete old Log files**

Based on the Incident ticket for C drive space issue.

1. Find the folder which is taking high space utilization.
2. Find the application owner and send mail for old log deletion approval
3. Post confirmation, attach the approval mail in incident ticket and delete the old logs

**Temp Folder Cleanup:**

Go to run, Type > **%temp%** > press OK

Delete all files in the temp folder

**Delete Unused Users Profile:**

**Step 1**: Go to advanced system settings (sysdm.cpl), advanced tab, click on settings in the user profiles box (middle of screen), under “profiles stored on this computer” click on the user profile you want to delete, and press Delete.

Or

**Using Control Panel**

1. Select **Start**, search for *Control Panel*, and select **Control Panel** in the result.
2. Select **Large icons** in **View by** and then select **System**.
3. Select the **Advanced System settings** link.
4. In the dialog that opens, select **Settings** in the **User Profiles** section.
5. In the next dialog, there is a list of profiles on the system. Select the profile that you want to remove and select **Delete**.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

**From registry:**

**Open the Registry editor**
Press the “Start” button and type “regedit”, then click “Run as administrator”.

**Navigate to the profile list in registry editor**

In the search bar or side menu, navigate to the profile list in registry editor, which is found at:

Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows NT\ProfileList

![Graphical user interface, text

Description automatically generated](data:image/png;base64...)

**Find the account in the profile list registry key**

The profile list registry key will have several SID keys for each user. To find the one you’re looking for, click on each and check the “Data” field next to the “ProfileImagePath” entry.

![](data:image/png;base64...)

**Delete the user profile registry key**

In the left-hand side menu, right-click the correct user SID and press “Delete”.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

**Confirm the user profile registry key deletion**

Make sure you’re deleting the key for the correct user before clicking “Yes”.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

20.2 Non -OS drive clean-up Incident

**For any issue related to SQL has to be sent to SQL team looping POC in CC.**

**And rest all issues the email must go to POC**

20.3 CPU usage troubleshooting incidents

1. Using Azure Monitor,

**Step 1:** Log in to [Azure Portal](https://portal.azure.com/).

**Step 2:** Then go to the Virtual Machines and select the respective azure VM.

**Step 3:** After choosing the Azure VM, from left hand side of the page, navigate to Monitoring è select

**Metrics:**

![](data:image/png;base64...)

**Step 4:** Select **Scope à Required Azure VM**

* + Select **Metric Namespace** == **Virtual Machine Host**

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

* + Next, Choose the **Metric == “Percentage CPU” and Aggregation == “Avg”**

![](data:image/png;base64...)

* + Select Time Generated Number of Days as required

![](data:image/png;base64...)

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

In the same way if want data for the period requested.

![](data:image/png;base64...)

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

* 1. **Using Task Manager**
* Use Task Manager to view CPU consumption to help identify the process or application that's causing high CPU usage:
* Open the Task Manager by clicking “Start” and typing “Task Manager” into the search bar, or by using a keyboard shortcut by holding down Ctrl+Shift+Esc or Ctrl+Alt+Delete.

![](data:image/png;base64...)

* The Task Manager window defaults to the Processes tab.
* Select the CPU column header to sort the list by CPU usage. Make sure that the arrow that appears on the header points down to sort the data from highest to lowest CPU consumption.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

* If the process can be stopped, or a related service can be disabled, stop the process or the service. Then, check whether this mitigates the problem.

20.4 Memory usage troubleshooting Incidents

1. **Using Azure Monitor:**
   * + Go to specific VM
     + Search for the respective sever name for which we need to check the memory usage.
     + Go to INSIGHTS tab to monitor the Memory usage and performance within that server and we can get insights as in where the maximum memory is being consumed within the sever along with the timeline information.

![](data:image/png;base64...)

1. **Using Task Manager:**
   * + Open the Task Manager by clicking “Start” and typing “Task Manager” into the search bar, or by using a keyboard shortcut by holding down Ctrl+Shift+Esc or Ctrl+Alt+Delete.

![](data:image/png;base64...)

* + Click “More details” to expand to full view.
  + Navigate to the “Processes” tab and click the “Memory” header. This will sort all processes from most to least RAM usage.

![Graphical user interface, table

Description automatically generated](data:image/png;base64...)

* + From here, select and click on “End Task” for the processes or applications that consume more memory post getting necessary approvals.
  + For more details on the memory consumption, please open Resource Monitor from the task manager and check the memory usage details.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

20.5 Server Onboarding Procedure

1. Login to splunk console <https://10.113.2.18:8443>
2. Go to the Splunk Homepage and click on the highlighted segment as shown in the below snap. ![](data:image/png;base64...)

![](data:image/png;base64...)

1. Click on the **Onboard Management Dashboard** for the server onboarding.![Graphical user interface, application

   Description automatically generated](data:image/png;base64...)
2. Drop-down the **OS Name** and **Host** field and paste the server’s name you want to onboard and then select it (if server is not listing in host field, please check splunk forwarder service is running or not)

**Note:** Can add bulk servers to onboard but based on OS Name.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

![](data:image/png;base64...)

1. Accordingly choose Environment, System, Sub\_system, type fields.

![](data:image/png;base64...)

1. Select the **System** as per your requirement and **Contract\_Type** as **MSHS** for any remote server to be onboarded.

![](data:image/png;base64...)

1. Choose description field as per your requirement.

![](data:image/png;base64...)

1. In the **RITM** field, give the RITM number and click on **Submit**.

![](data:image/png;base64...)

1. Once you click Submit, the server would be adding in mywizard(inprogress) as below and the details of the server would be visible below in the dashboard (e.g what time it was added, user who added).

![](data:image/png;base64...)

1. After few minutes (5 - 10mins), you can see server which is onboarded successfully

![](data:image/png;base64...)

Or else you can see the onboard and offboard status by filtering time in below dashboard

![](data:image/png;base64...)

![](data:image/png;base64...)

ESS Portal & Cluster DL Details:

* If still you have any issues, then kindly log a ticket in **ESS portal** for assistance from the cluster team.
* Access ESS portal with the below link:

<https://accentureplc.service-now.com/clientportal>

* For ESS portal access enablement drop a mail to GSM.ISTools.IM@accenture.com
* Please find the attached PPT with steps to create an RITM for the cluster team.
* For any further queries drop a mail to,

**NA Cluster-1 DL:** Tools.Cluster.NA1@accenture.com

20.6 Server offboarding Procedure

1. Login to splunk console <https://10.113.2.18:8443>

1. Click on offboard Management Dashboard, choose the server which want to remove or offboard from mywizard and enter RITM number, click on submit.

![](data:image/png;base64...)

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

![Graphical user interface, text, application, chat or text message

Description automatically generated](data:image/png;base64...)

1. Once click on submit, it will display the server details in below window. Confirm the server and then click on server name.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. It will delete in all lookups in which server was present. It will show the output as updated successfully in all panels. It is showing **No results found**, that means server has been deleted from inventory.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Offboard status panel will give all details like at what time server was deleted with username, RITM and Source host as per above screenshot, if it doesn’t display please refresh that panel at right end which was highlighted below

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

Or else you can see the onboard and offboard status by filtering time in below dashboard

![](data:image/png;base64...)

![](data:image/png;base64...)

ESS Portal & Cluster DL Details:

* If still you have any issues, then kindly log a ticket in **ESS portal** for assistance from the cluster team.
* Access ESS portal with the below link:

<https://accentureplc.service-now.com/clientportal>

* For ESS portal access enablement drop a mail to GSM.ISTools.IM@accenture.com
* Please find the attached PPT with steps to create an RITM for the cluster team.
* For any further queries drop a mail to,

**NA Cluster-1 DL:** Tools.Cluster.NA1@accenture.com

![](data:image/x-emf;base64...)

20.7 Config Wizard Blackout

**Key Points**

Make sure blackout is created minimum 1 hour before the start of activity

**Step 1:** Login to MyWizard URL

<https://10.113.2.18:8443>

**Step 2:** Click on **MyWizard AiOps Stack Monitoring Suite**

![](data:image/png;base64...)

**Step 3:** Select **configwizard -> Blackout -> ConfigWizard Blackout**

![](data:image/jpeg;base64...)

![](data:image/png;base64...)

**Step 4:** click on **ADD Button** to Add Blackout

![](data:image/png;base64...)

**Step 5:** Click on Filters, Select Contract Type as “MSHS” and click on import from CSV option as below.

![](data:image/png;base64...)

**Step 6:** Create CSV file to import blackout for single or multiple server as below format.

| Key | metric | instance |
| --- | --- | --- |
| Device1\* | \* | \* |
| Device2\* | \* | \* |

**Step 7:** import CSV to Blackout Portal.

![](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/x-emf;base64...)

**Step 8:** check all import data in portal

![](data:image/x-emf;base64...)

**Step 9:** Click on **Next** Button

**Step 10:** Select timing as per your time zone and update

![](data:image/x-emf;base64...)

Validate time window along with Key, metric and instance reflecting

![](data:image/x-emf;base64...)

**Step 11:** Below is the final window to validate. Click **Next** and **Confirm**

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

**Step 12:** Please Wait for 60 mins, then you can see the blackout on the portal.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

21. Storage Management

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed Storage process, kindly refer to Storage runbook mentioned in the Document Call outs. | | |

22. Vulnerability Remediation

|  | **Information Pending** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| Hourglass Finished with solid fill | Tenable.io is used for VA assessment (Scan) for core.  Defender is used in sandbox for interim solution | | |

Based on the vulnerability report we need to remediate the vulnerabilities ASAP and share the artifacts.

25. Tools

| Tool | Description | Requirements |
| --- | --- | --- |
| ServiceNow | ITSM tool |  |
| DevOps / Ansible | Configuration management |  |
| My Nav | Migration |  |

26. MSSN Infrastructure :

Client is having physical and virtual servers in on Prem VMware infrastructure.

We must follow the same procedure of MSHS on day-to-day operations to support this infrastructure.

Use PA account to login to the vcenter.

15.1 vCenter access

| Env | vCenter Name |
| --- | --- |
| Prod | <https://hpv-vctr-001.snch-home.org> |
| Prod | <https://opv-vctr-001.snch-home.org> |

![](data:image/png;base64...)

**Client is having 2 datacentres and address is**

**Datacenter address:**

**Hicksville**

1000 South Oyster Bay Road
 Hicksville, NY, 11801

**Oceanside**

One Healthy Way, Oceanside, NY 11572

For any Hardware issues, need to send mail to

ISSystems@snch.org

**Contact Numbers:**

kenneth law 917-359-7962

Ditalia, Paul P. 917-566-8150

**Server naming convention:**

Hv- Hicksville

Ov- Ocean side

P – Production

T – Test

-AAA- Application

-XX – number

Ex- HVP-CTX-01

OVP-CTX-19

**Domain Name: snch-home.org**

**AD Servers:**

HDQPADCIF01

HVP-INF-DC-01

OSDPADCIF01

OVP-INF-DC-01

NTP server: OVP-INF-DC-01.snch-home.org

ILO is not configured for the physical servers; hardware support engineer will visit the datacenter and validate the servers physically.

There are no cluster servers in the infrastructure.

**Login to the servers:**

Launch RDP session from VDI desktop and To Login any server we need to user port 4389 or 2327

![](data:image/png;base64...)

**Monitoring:** Currently servers are in SCOM monitoring and after transition servers are monitored through mywizard

**Patching:**

Currently servers are in manual patching.

**andrew.lacorte@snch.org**POC for coordinating with the server POC’s and scheduling the patching changes.

For IP reservation, IPAM tools is used.

http://vp-ops-mgr-01.snch-home.org:8060/apiclient/ember/index.jsp#/Home/Dashboard/Overview/dashboard.name.enterprisedashboard

**Software repository:** Templates are used to build new servers.

**![](data:image/png;base64...)**

**Server commissioning:**

Requestor will send the server build request template and need to raise a change.

Perform the server-built activity after receiving all the required approvals in the change control**.**

**Steps :**

* 1. Select the OS template as requested in the request document.
  2. Right click on the template and click on ‘ New VM from this template” option.

![](data:image/png;base64...)

* 1. Provide the server’s name and select the appropriate folder.

![](data:image/png;base64...)

* 1. Select the datacentre and cluster resource name accordingly.

![](data:image/png;base64...)

* 1. Select the Storage

![](data:image/png;base64...)

* 1. Select Customise OS and hardware options.

![](data:image/png;base64...)

* 1. Select operating system.

![](data:image/png;base64...)

* 1. Update the IP details

![](data:image/png;base64...)

* 1. Customise the server hardware as per the request.

![](data:image/png;base64...)

* 1. Validate the option selected and click on finish.

![](data:image/png;base64...)

* 1. Once server is up join the server to the domain.
  2. Install following basic tools.
  3. Crowd strike
  4. Rapid7
  5. Sysmon
  6. Gaurdicore

Perform the basic checks and handover the servers to requestor.

**AD server OU Details:**

![](data:image/png;base64...)

**AD Groups OU details:**

![](data:image/png;base64...)

**Server Policy Details :**

![](data:image/png;base64...)

26.1 **To fix NLA issue for Azure servers follow the below steps:**

1. Login to azure portal

2.Locate the server

3.Go to run command

4.Disable NLA using run command

5.Reboot the server

6. Remove it from domain

$securePass = ConvertTo-SecureString “Credeantial for pa account" -AsPlainText -Force

$cred = New-Object System.Management.Automation.PSCredential ("msnyuhealth\-pa account", $securePass)

Remove-Computer -Credential $cred -Force -Restart

7.Delete AD object(note the down the OU details)

8.Add server in domain

$securePass = ConvertTo-SecureString " Credeantial for pa account " -AsPlainText -Force

$cred = New-Object System.Management.Automation.PSCredential ("msnyuhealth\\-pa account ", $securePass)

Add-Computer -DomainName "msnyuhealth.org" -Credential $cred -Force –Restart

9.Move the server to correct OU

10.Enable the NLA run the below commands

 REG add "HKLM\SYSTEM\CurrentControlSet\Control\Lsa" /v disabledomaincreds /t REG\_DWORD /d 0 /f

REG add "HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp" /v UserAuthentication /t REG\_DWORD /d 1 /f

![](data:image/png;base64...)

![](data:image/png;base64...)

27. Vendor Management & SLA

27.1. Azure case logging

Microsoft Azure support case can be logged using Azure portal. Below screenshot is for your reference.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

Note: Current Microsoft Azure Support for MSHS is “Enterprise”

**27.2 Cloud Managed Service – How to Create Azure Service Health to notify when there are service issues affecting a specific service**

27.3 Escalation Matrix

Microsoft Support Account Manager for MSHS is **Bill Pritchett** (bipritch@microsoft.com)

28 Contacts

28.1 CMS contacts

| Name | Role | Organization | Email |
| --- | --- | --- | --- |
| Mujawar, Nilofer L | Windows Lead | CMS | nilofer.l.mujawar@accenture.com |
| Jeetendra Verma | Azure Lead | CMS | Jeetendra.Verma@ accenture.com |
| Escalation Contact | | | | |
| Thrivikraman Elayath | Delivery Manager | Offshore | thrivikraman.elayath@accenture.com | |
| Taha Rashidi | Delivery Manager | Onshore | Taha.rashidi@accenture.com | |
| Suprovat | Support Manager | Offshore | suprovat.sinha@accenture.com | |

28.2 Build and Migration contacts

| Name | Role | Email |
| --- | --- | --- |
| Cesar Ceniceros | Foundation Build | cesar.ceniceros@avanade.com |
| Jose Ivey | Non – EPIC Migration | jose.ivey@accenture.com |
| Zach Nemitz | EPIC Migration | zach.c.nemitz@accenture.com |
| Bryan Long | DevOps | bryan.m.long@accenture.com |

28.3 Escalation Matrix Internal CMS

| Escalation Level | Name | Email |
| --- | --- | --- |
| L1 | Tower Leads | MSHS.CMS.TowerLeads@accenture.com |
| L2 | Vikram  Taha | Thrivikraman.elayath@accenture.com  Taha.rashidi@accenture.com |
| L3 | KJ  BG | jayasankar.k.j@accenture.com  bharathi.ganesh.ns@accenture.com |
| L4 | Gurbaxani, Neelam L. Amit Gaur | neelam.l.gurbaxani@accenture.com  amit.gaur@accenture.com |

27.4 Escalation MSHS

| Escalation Level | Name | Email |
| --- | --- | --- |
| L1 | Joseph Brittelli | Joseph.Brittelli@mountsinai.org |
| L2 | Joseph Gimigliano | Joseph.Gimigliano@mountsinai.org |
|  |  |  |

29. SOP

**Please refer below link for the SOP:**

Adding server to domain click here

Post build activities click here

DR activities Fail over Fail back click here

File Recovery click here

RMT build click here

30. Vendor Case Update

* Every vendor case which CMS will raise there should be an incident logged in ServiceNow apart from incident for the issue
* Incident logged for the vendor case should follow below guidelines:

Incident Short description should follow the below format

**VENDOR CASE :** *<Vendor Name>***|** *<Vendor Case ID or Number>***-** *<Issue Description>*

Example: VENDOR CASE : NetApp | 2009655556 - CIFS Auth Problem error

* Incident priority should P4
* Incident should be documented as it progresses with the update
* Incident state should change according to the action required

(i.e., if action is waiting from CMS it should be “In Progress” if it is waiting for the response from vendor then should be “On Hold” for vendor response)

* Incident will be closed only when the vendor case is closed

Ensure it is made in effect from immediate for all new vendor cases we are logging

