

**Cloud Ops - Citrix Runbook**

**Document Control**

| Version | Status | Date | Author | Summary of Change |
| --- | --- | --- | --- | --- |
| V1.1 | Initial Draft | 18-Jul-2022 | Citrix Team | Initial Draft |
| V1.2 | Update Draft | 27-Jul-2022 | Citrix Team | Citrix Cloud Portal, Citrix License, Citrix Policy and Citrix Studio |
| V1.3 | Update Draft | 16-Aug-2022 | Citrix Team | Application Publishing,  Master Image and Troubleshooting steps |
| V1.4 | Update Draft | 29-Aug-2022 | Citrix Team | Citrix Director, VDA, Monitoring |
| V1.5 | Update Draft | 08-Sept-2022 | Citrix Team | Post servers build steps, Patching, Link Update |
| V1.6 | Update Draft | 25-Oct-2022 | Citrix Team | Section 11.19 and Section 22. |
| V1.7 | Updated Draft | 09-Jan-2023 | Citrix Team | Citrix URL`s |
| V1.8 | Updated Draft | 01-Jun-2023 | Citrix Team | SCOM Alerting Procedure |
| V1.9 | Updated Draft | 13-Jul-2023 | Citrix Team | Epic Information |
| V2.0 | Updated Draft | 14-Jul-2023 | Citrix Team | NetScaler |
| V2.1 | Updated Draft | 10-Aug-2023 | Citrix Team | MSHS,MSSN |
| V2.2 | Updated Draft | 23-Sep-2023 | Citrix Team | Certificate update,timezone |
| V2.3 | Updated Draft | 07-OCT-2023 | Citrix Team | Post reboot activity. |

**Document Approval**

| Date | Version | Approver | Comments |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

**Document Reviews**

| Date | Company | Reviewer | Notes |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Table Of Contents

PAGEREF \_Toc140263612 \h

 [1](#_Toc176320614)

[**Document Control** 2](#_Toc176320615)

[**Document Approval** 3](#_Toc176320616)

[**Document Reviews** 3](#_Toc176320617)

[1. Introduction 8](#_Toc176320618)

[2. About MSHS 9](#_Toc176320619)

[3. About Accenture 10](#_Toc176320620)

[4. Acronyms, Terminology & Appendix 11](#_Toc176320621)

[5. Document call outs 12](#_Toc176320622)

[6. RACI 13](#_Toc176320623)

[7. Common URLS 15](#_Toc176320624)

[8. Scope 16](#_Toc176320625)

[8.0 In scope of services 16](#_Toc176320626)

[8.1 Out of Scope of Services 16](#_Toc176320627)

[8.2 Decisions, Important Notes and Recommendations Reference 17](#_Toc176320628)

[9. System Information 18](#_Toc176320629)

[9.0 Citrix Server Naming Convention 18](#_Toc176320633)

[9.1 Delivery Group/Machine Catalog Naming Convention 18](#_Toc176320634)

[9.2 System Inventory 18](#_Toc176320635)

[9.3 Citrix Configurations 19](#_Toc176320636)

[10. Access 20](#_Toc176320637)

[10.0 Citrix VDI Access 20](#_Toc176320638)

[10.1 Azure Portal Access 20](#_Toc176320639)

[10.2 Citrix Cloud Access 20](#_Toc176320640)

[11. Citrix Operations 21](#_Toc176320641)

[11.0 Citrix URL for Prod, QA & Dev 21](#_Toc176320642)

[11.1 Citrix On Prem URL for Prod, QA & Dev Vcenter 21](#_Toc176320643)

[11.2 Log on to Citrix Cloud 21](#_Toc176320644)

[11.3 Citrix Cloud Connector 22](#_Toc176320645)

[11.4 Adding an Administrator in Citrix Cloud 23](#_Toc176320646)

[11.5 Change Administrator Permissions in Citrix cloud 24](#_Toc176320647)

[11.6 Create a Hosting Connection 26](#_Toc176320648)

[11.7 Install Server OS VDA 28](#_Toc176320649)

[11.8 Create a Server OS Machine Catalog 32](#_Toc176320650)

[11.9 Create Server OS Delivery Group for MCS Created Machines 37](#_Toc176320651)

[11.10 Verify Citrix Cloud Connector are online or not. 41](#_Toc176320652)

[11.11 Cloud Connector Session failover 42](#_Toc176320668)

[11.12 Cloud Connector CDF tracing 42](#_Toc176320669)

[11.13 Monitor the Site with Cloud Director and Application Analytics. 46](#_Toc176320670)

[11.14 Determine hourly usage of VDAs 54](#_Toc176320671)

[11.15 Citrix License Status 60](#_Toc176320672)

[11.16 Configure Citrix policy 60](#_Toc176320673)

[11.17 How to create an Application Group. 64](#_Toc176320674)

[11.18 How to delete an application group /application. 67](#_Toc176320675)

[11.19 How to create a Master Image 67](#_Toc176320676)

[11.20 Master Image Update 68](#_Toc176320677)

[11.21 Troubleshooting and providing solution for application issue 75](#_Toc176320678)

[11.22 Monitoring of the Storefront server and its services. 75](#_Toc176320679)

[11.23 Managing User and VM’s Session in Citrix Studio. 76](#_Toc176320680)

[11.24 How to install Virtual delivery agent. 77](#_Toc176320681)

[11.25 Monitoring of Real User sessions and Citrix Connections failures 83](#_Toc176320682)

[11.26 Monitoring of application failure from Citrix director 83](#_Toc176320683)

[11.27 Provide application access to end user 85](#_Toc176320684)

[11.28 Pull custom report of End user from Citrix Director 86](#_Toc176320685)

[11.29 Management of Citrix URL Certificate 86](#_Toc176320686)

[11.30 How to install an application in Session Host server and publish it to End User? 86](#_Toc176320687)

[11.31 How to access Azure File Share. 88](#_Toc176320688)

[11.32 Configuring TLS 1.0 for TRAC applications VDA server 90](#_Toc176320689)

[11.33 License clean up 91](#_Toc176320690)

[11.34 Check .Net Framework Path 92](#_Toc176320691)

[11.35 Renewal of Citrix Storefront Certificate 92](#_Toc176320692)

[11.36 Time Zone of newly created Virtual Machine 93](#_Toc176320693)

[11.37 Post reboot activity if any error occurs need to follow the steps. 93](#_Toc176320694)

[11.38 Citrix Core Servers Patching 94](#_Toc176320695)

[11.39 Standalone OS Citrix VDA Patching 94](#_Toc176320696)

[11.40 MCS Managed Citrix VDA Patching 94](#_Toc176320697)

[11.41 How to Publish an application icon 95](#_Toc176320698)

[11.42 Install Server OS VDA 97](#_Toc176320699)

[11.43 Master image sealing 128](#_Toc176320700)

[11.43 How to access Citrix Director 129](#_Toc176320701)

[11.44 How to Generate reports from Citrix Director 132](#_Toc176320702)

[12 Post Server Build Steps 135](#_Toc176320703)

[12.1 Citrix Server Configuration Check 135](#_Toc176320704)

[12.2 Citrix Core Server Component Checks 137](#_Toc176320705)

[12.3 Citrix Master Image and VDA Check 138](#_Toc176320706)

[12.4 Citrix Antivirus Exclusion Check 138](#_Toc176320707)

[13 Backups 140](#_Toc176320708)

[13.1 Snapshots 140](#_Toc176320709)

[14 EPIC 141](#_Toc176320710)

[14.1 Epic Environment Configurations 141](#_Toc176320711)

[14.2 Issues and Troubleshoot 141](#_Toc176320712)

[14.2.1 Epic Error 3500 Issue 141](#_Toc176320713)

[14.2.2. Epic Prod Icon is not Launching 142](#_Toc176320714)

[14.2.3 Epic Prod Icon is missing 142](#_Toc176320715)

[14.3 Important checks for P2 Incident. 143](#_Toc176320716)

[14.4 Epic Applications and Contact Details. 143](#_Toc176320717)

[14.5 Call Tree 145](#_Toc176320718)

[15 Net Scaler 146](#_Toc176320719)

[15.1 Components 146](#_Toc176320720)

[15.2 ADC Configuration 146](#_Toc176320721)

[15.3 NetScaler upgrade using GUI and CLI 159](#_Toc176320722)

[15.4 Netscalar VAR folder cleanup 167](#_Toc176320723)

[16 Disaster Recovery 176](#_Toc176320724)

[16.1 Disaster recovery of Citrix Cloud Published Non-EPIC APPS Availability during Planned DR TESTING 176](#_Toc176320725)

[16.2 Disaster recovery of Citrix Cloud Published for EPIC APPS 178](#_Toc176320726)

[17 MSSN Environment 179](#_Toc176320727)

[17.1 How to RDP to a MSSN Server 179](#_Toc176320728)

[17.2 How to Access Vmware and Virtual machine 179](#_Toc176320729)

[17.3 How to Access Production and test Citrix 180](#_Toc176320730)

[17.4 Access Xenapp6.5 181](#_Toc176320731)

[18 Vendor Management 183](#_Toc176320732)

[19 Storage Management 184](#_Toc176320733)

[20 Software Management & Licensing 185](#_Toc176320734)

[20.1 Citrix Licensing 185](#_Toc176320735)

[21 Profile Management 186](#_Toc176320736)

[22 Vulnerability Management 187](#_Toc176320737)

[22.1 Vulnerability Management Process 187](#_Toc176320738)

[22.2 Vulnerability Management Risk Rating 187](#_Toc176320739)

[23 Disaster Recovery 188](#_Toc176320740)

[24 SOP 189](#_Toc176320741)

[25 Monitoring 190](#_Toc176320742)

[25.1 Server Level monitoring 190](#_Toc176320743)

[25.2 Citrix Services Monitoring 190](#_Toc176320744)

[25.2 Citrix Cloud Health Monitoring 192](#_Toc176320745)

[25.3 Citrix DaaS Monitoring 193](#_Toc176320746)

[25.4 Server On boarding to My Wizard 194](#_Toc176320747)

[25.5 Server off boarding from My Wizard 194](#_Toc176320748)

[25.6 Blackout Server in My Wizard 194](#_Toc176320749)

[25.7 Email Alerts coming to Citrix DL 194](#_Toc176320750)

[26 Contacts 195](#_Toc176320751)

[26.1 CMS contacts 195](#_Toc176320752)

[26.2 Build contacts 195](#_Toc176320753)

[26.3 Escalation Matrix Internal CMS 196](#_Toc176320754)

[26.4 Escalation Client 196](#_Toc176320755)

[27 SCOM Alerting Procedure 197](#_Toc176320756)

1. Introduction

This document will act as a handbook which consists of all the technical procedures and processes that are required to support the Citrix Server. The Accenture Citrix team will leverage this document for all the processes, tools, procedures, and resources to perform day-to-day operations within the IT Infrastructure and provide world-class service to the business and end-users.

When an incident or problem occurs in the environment, an operations organization relies on its Standard Operating Procedures (SOP’s) or troubleshooting guidelines to resolve the problem. A proactive approach to documentation is needed to support database operations within an organization.

This Run Book will serve to define both daily operations tasks to support the infrastructure deployed for MSHS recommended troubleshooting tasks to revolve issues which may be encountered. The Run Book also identifies task owners for specific operations tasks and estimated effort.

Any updates in the document should be reviewed & approved.

1. About MSHS

Mount Sinai Health System (MSHS) is New York City's largest academic medical system, encompassing eight hospitals, a leading medical school, and a network of ambulatory practices. Mount Sinai is an international source of unrivaled education, translational research and discovery, and clinical delivery outcomes.

MSHS is among the top research and clinical institutions providing response to COVID-19, leveraging numerous artificial intelligence algorithms and machine learning models developed in-house. The current pandemic has accelerated the need and urgency for speed and innovation, including rapid access to data and collaboration. However, MSHS is constrained by a legacy technology environment that is costly to maintain, and in some instances, with components beyond end of life. The culmination of technical debt has created an environment that is costly to maintain and prohibitive to research advancement and clinical outcomes.

Given the demands placed on the clinical and research teams; there exists an enterprise imperative to enable a landscape of technology services that are up to date, always available, inexpensive to implement / maintain, and readily available on a self-service basis.

1. About Accenture

Accenture is a global management consulting, technology services and outsourcing company. Combining unparalleled experience, comprehensive capabilities across all industries and business functions, and extensive research on the world's most successful companies, Accenture collaborates with clients to help them become high-performance businesses and governments.

1. Acronyms, Terminology & Appendix

| Term | Description |
| --- | --- |
| VDA | Virtual Delivery Agent |
| IP | Internet Protocol |
| ITSM | Information Technology Service Management |
| KB | Knowledge Base |
| MCS | Machine Creation Services |
| MS | Microsoft |
| DaaS | Desktop as a Service |
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
| NFS | Network File System |
| DR | Disaster Recovery |
| AD | Active Directory |
|  |  |
|  |  |

1. Document call outs

This section covers all the references to other documents

|  |  |
| --- | --- |
| CMS Windows Runbook | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ef7ro_AgHS1Lgzw_j08z2JEBSbx0Ev1bRuXnlyj7FvNp7A?e=eCEBJR) |
| CMS Linux Runbook | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EQBJHW2c-vtEgeOnqf3V_jkB9zqrXKaa2jq81dw5Iple4w?e=Kp3hDT) |
| CMS Azure Fundamentals | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/EUG0YaatWwtDn-_bVG3Rgf4B0J2Q5bcQKN3n1O5ar7XsjQ?e=MSC9Hh) |
| CMS Backup Runbook | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/CloudOperations-CMS/Ed-8DGYuGGVCgf8_U9Goc3UBEYI_5mNCAuXMgA-7_NWlag?e=rZA9J2) |
| CMS DR Runbook | Click Here |
| HLD Document | [Click Here](https://mtsinai.sharepoint.com/sites/BusinessCaseValidation/Shared%20Documents/Forms/AllItems.aspx?cid=abc6debd%2D53b2%2D4c63%2Da3f9%2D93ee4f2b623e&FolderCTID=0x0120000AD53B2894B0AA48AF2E0F98676FB541&id=%2Fsites%2FBusinessCaseValidation%2FShared%20Documents%2FGeneral%2FDeliverables%2FCloud%20Foundations&viewid=458ee074%2D644d%2D49f9%2Da0cc%2D2b2b80271076) |
| LLD Document | [Click Here](https://mtsinai.sharepoint.com/sites/BusinessCaseValidation/Shared%20Documents/Forms/AllItems.aspx?cid=abc6debd%2D53b2%2D4c63%2Da3f9%2D93ee4f2b623e&FolderCTID=0x0120000AD53B2894B0AA48AF2E0F98676FB541&id=%2Fsites%2FBusinessCaseValidation%2FShared%20Documents%2FGeneral%2FDeliverables%2FCloud%20Foundations&viewid=458ee074%2D644d%2D49f9%2Da0cc%2D2b2b80271076) |
| Citrix Design Document | [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/BusinessCaseValidation/_layouts/15/Doc.aspx?sourcedoc=%7B7512C4EF-372D-4166-823F-5FD35FE55BF0%7D&file=MSHS%20Citrix%20Design%20Document%20V9.docx&action=default&mobileredirect=true) |

1. RACI

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For RACI, kindly refer to SOW. Link to SOW - [SOW](https://mtsinai.sharepoint.com/%3Af%3A/s/BusinessCaseValidation/EhmZJp209rBJlEELgncTmtcBuUctylKgu7lcF05sfn_EaQ?e=JSxZF5) | | |

![](data:image/png;base64...)

1. Common URLS

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

1. Scope

In scope of services

This Run Book covers basic operating guidelines and procedures necessary for administering and maintaining databases in the MSHS infrastructure. The scope of this document and work package is to:

|  |  | | |
| --- | --- | --- | --- |
|  |  |  |  |
| IS 1 | Systems Management (Citrix Scope)   * Operating System Patch Management (MCS managed OS) * System Security Maintenance * Citrix Environment manage | | |
| IS 2 | Infrastructure monitoring and incident management   * Infrastructure monitoring and alert verification * Incident management and resolution | | |
| IS 3 | Service Request Fulfillment   * Provisioning, decommissioning and Modification Citrix Infra | | |

Out of Scope of Services

|  |  |
| --- | --- |
| OOS 1 | Procurement\Renewal of the licenses in the environment |
| OOS 2 | Administer user policies through GPO. |
| OOS 3 | Review and approve schedule for distribution of Patches and Hot Fixes following the approved change management processes. |
| OOS 4 | Conduct Application Regression Tests, as possible and appropriate. |
| OOS 5 | Anything that is not mentioned in Scope (Section 8.1) |

Decisions, Important Notes and Recommendations Reference

Throughout this document decisions, important notes or recommendations are highlighted using the following:

|  | Important note | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Important note | | |

|  | Architecture Decision | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | Architecture Decision | | |

|  | Decision required | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ? | Decision required | | |

|  | Recommendation | | |
| --- | --- | --- | --- |
|  |  |  |  |
|  | Recommendation by Build and/or MSHS. | | |

|  | Infrormation Pending | | |
| --- | --- | --- | --- |
|  |  |  |  |
|  | Dependency on HLD/LLD, KT or Deployment | | |

1. System Information

Citrix Server Naming Convention

Citrix server will follow the naming convention as mentioned in below HLD/LLD.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer to HLD/LLD mentioned in the link.  [Click Here](https://mtsinai.sharepoint.com/sites/CloudOperations-CMS/Shared%20Documents/Forms/AllItems.aspx?FolderCTID=0x0120008B01720AE04C8345A8DB2E9D6FEA8BE7&OR=Teams%2DHL&CT=1662492391170&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjA3MzEwMTAwNSIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D&id=%2Fsites%2FCloudOperations%2DCMS%2FShared%20Documents%2FGeneral%2FReference%20Documents&viewid=98ee747f%2D3337%2D4c20%2Da48f%2D5086f684be2f) | | |

Delivery Group/Machine Catalog Naming Convention

Citrix Delivery Group and Machine Catalog Naming standard will follow the same as per the existing On-Prem naming standard only adding suffix or prefix of environment.

![](data:image/x-emf;base64...)

System Inventory

Citrix Inventory are maintaining on the below SharePoint site location.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the link for Citrix Server Inventory.  [Click here](https://mtsinai.sharepoint.com/%3Ax%3A/s/CloudOperations-CMS/EZ2rGWoPilVBupZlJnk_Rx0B0-oOm5SB9TucHWIiDPoqJA?e=QdKvEY) | | |

Citrix Configurations

Citrix environment build and configuration details are mentioned in [Citrix Design Document](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/BusinessCaseValidation/_layouts/15/Doc.aspx?sourcedoc=%7B1C64C080-BE90-4648-B337-89AED145B6E3%7D&file=MSHS%20Citrix%20Design%20Document%20V4.docx&action=default&mobileredirect=true). Kindly refer this document for in depth information.

1. Access

Citrix VDI Access

First level of the access to Mount Sinai is via Citrix VDI using msnyuhealth.org domain and VIP Symantec MFA.

Link to access the Citrix VDI URL: <https://mountsinai.cloud.com/Citrix/StoreWeb/#/home>

Azure Portal Access

Post the access to Citrix VDI, Azure portal access is made using privilege account (PA) as per the Mount Sinai access guideline. No access to MSHS will be allowed through non-PA account.

CMS Cloud Foundation access to the Azure Portal is provided through the Active Directory MSH-Cloud Foundation-ACN group membership on the PA account.

Citrix Cloud Access

The Citrix cloud portal will be accessed for administrators to manage the required Citrix cloud services.

* [Citrix DaaS](https://www.citrix.com/products/citrix-daas/) (formerly Citrix Virtual Apps and Desktops service) will be used for MSHS environment.
* Access to Citrix cloud portal will be granted via “Identity and Access Management”.
* Appropriate permissions for the administrators will be configured as per their work role (Role Based Access for Citrix):

1. Full access: allows control of all Citrix Cloud functions. Full access will be granted to Citrix L2, L3 admins.
2. Read-Only access: this is to grant read-only access to Citrix environment configuration view purpose.

3) Custom access: allows control of the functions and services that you select. It can be used for Helpdesk team.

To Provide Administrator access in Citrix cloud please refer to Section 11.3.

1. Citrix Operations

Citrix URL for Prod, QA & Dev

Please find the Production Environment URL

* <https://storefront.mountsinai.org>
* <https://storefrontvpn.mountsinai.org>
* <https://Portal.moutsinai.org>

Please find the QA Environment URL

* <https://storefrontqa.mountsinai.org>

Please find Dev Environment URL

* <https://strorefrontdev.mountsinai.org>

11.1 Citrix On Prem URL for Prod, QA & Dev Vcenter

Please find the Production and QA Environment Vcenter

* <https://svmwvcip018001.msnyuhealth.org>   - Manual Build Prod servers

* <https://vcenterctxs.msnyuhealth.org>  - Non EPIC Prod & QA servers
* <https://vcenterepic.msnyuhealth.org> – EPIC Prod & QA servers

Please find the Dev Environment URL

* <https://vcenterepicdev.mountsinai.org/> -EPIC Dev
* <https://vcenterctxsdev.msnyuhealth.org>  - Non EPIC Dev

11.2 Log on to Citrix Cloud

1. Open https://us.cloud.com from your internet browser.
2. Type your Citrix Cloud Credentials.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Type your Authenticator verification code provided by Authenticator app.
2. The first-time logon to a Citrix Cloud account requires you to accept the Terms of Service. Select the checkbox I have read, understand, and agree to the Terms of Service and click Continue.
3. On the Welcome to Citrix Cloud window, click X.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

* 1. Citrix Cloud Connector

Citrix Cloud connector Installation, testing and disabling cloud connector to verify service outage.

![](data:image/x-emf;base64...)

* 1. Adding an Administrator in Citrix Cloud

1. Login into Citrix cloud portal with a full administrative account.
2. At the top left of the Citrix Cloud page, click the Fly-out menu and Select Identity and Access Management.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Click the Administrators tab on the Identity and Access Management page and select Citrix Identity to choose Manage administrators

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Type any email ID in the Email Address box and click Invite.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the dialog box that appears, verify the type of access the user needs to be given i:e Full access or Custom access based on their role. Click on Send invite.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. The user will receive an invite Link on the email provided. They need to accept the invitation and they will be able to access the Citrix Cloud Console with administrative privileged.
   1. Change Administrator Permissions in Citrix cloud

1. Click the Fly-out menu in Citrix Cloud console and Select Identity and Access Management.
2. Click the Administrators tab on the Identity and Access Management page.

![Diagram

Description automatically generated](data:image/png;base64...)

1. Locate the administrator account you want to change the Administrative privileged, click the three dots on the right side in the row correlating to your email address.
2. Click Edit Access on the drop-down to change the administrator’s privileges.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the Edit Access page, select the Custom access radio button to change the administrator from a Full administrator.

In the General Management section, select Resource Location to provide access to only this service for this administrator. Leave the other items in this section un-selected.

In the Virtual Apps and Desktops section, select Delivery Group Administrator, All, Host Administrator, All, and Machine Catalog Administrator, All to provide access to these services for this administrator.

![Graphical user interface, text, application, email, Teams

Description automatically generated](data:image/png;base64...)

1. At the top of the page, click Save to accept the changes. Confirm that Admin access was successfully updated, then click the back arrow to exit the page.
2. On the Identity and Access Management page, navigate to the Administrators tab and verify that the changes done is successful or not.
   1. Create a Hosting Connection
3. In the left pane of Citrix Studio, click Hosting, select Add Connection and Resources.

![](data:image/png;base64...)

1. On Add Connection and Resources screen, select to use an existing connection or to create a new one.

![](data:image/png;base64...)

1. On the Connection Details page, provide the subscription ID and connection name then Click Next.

![](data:image/png;base64...)

1. On the Region page, choose region as required and click Next.

Screenshot will be provided once we have access.

1. On the Network page, specify the name and the network that the future machine catalog machines will use.
2. Scopes: Accept the defaults of All objects and click Next.
3. On the Summary page, verify that the configuration information is correct.
   1. Install Server OS VDA
4. Verify that the machine is joined to the domain and Windows is activated and the date and time are correct.
5. Modify the power plan for Machine. Right-click Start and click Power Options. Under Choose or customize a power plan, select High performance.
6. Now that we have verified configurations for this VM, we will install the Virtual Delivery Agent so that it can communicate and register with the Delivery Controller. Launch the Citrix Virtual App and Desktop ISO.
7. On the Deliver applications and desktops to any user, anywhere, on any device screen, click Start next to the Virtual Apps and Desktops option.

![Graphical user interface, website

Description automatically generated](data:image/png;base64...)

1. The wizard will now display all possible installation options that are compatible with the Operating System of the machine running the installer. Select Virtual Delivery Agent for Windows Server OS.

![](data:image/png;base64...)

1. Verify Create a master MCS image is selected and click Next.

![Graphical user interface, text

Description automatically generated](data:image/png;base64...)

1. On the Core Components page, the Virtual Delivery Agent is marked as Required. This software was deployed from the main Virtual App and Desktops installer menu. Click Next to continue the Virtual Delivery Agent installation wizard.
2. In the additional components window, select from the option as required.
3. On the Delivery Controller page, under Configuration, confirm the drop-down menu is set to Do it manually. In the Controller address box, type the delivery controller address and Click Test connection. If the test is successful, as indicated by a green checkmark to the right of the Controller address box, click Add.

![](data:image/png;base64...)

1. Click Next to continue the Virtual Delivery Agent installation wizard.
2. On the Features page, verify the features you want to install and check the required feature.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the Firewall page, verify that the Automatically option is selected for configuring the firewall rules. Click Next.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the Summary page, review and confirm the configurations. Click Install.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. The installation will take a few minutes and will require the machine to be restarted.
2. After the Machine is up, On the Diagnostics screen, select clear the checkmark on collect diagnostic information and click Next.
3. Verify that the prerequisites, core components, and post-install items were completed successfully. Verify that the Restart machine option is enabled (default) and click Finish.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. The Machine will restart again and VDA will be installed.
   1. Create a Server OS Machine Catalog
2. In DaaS , Click Machine Catalogs on the left . Click Create Machine Catalog.

![](data:image/png;base64...)

1. On the Introduction page, click next to continue the Machine Catalog Setup wizard.
2. On the Operating System page, verify that Multi-session OS is selected and click next.

![](data:image/png;base64...)

1. On the Machine Management page, verify that the following two options are selected:

• Machines that are power managed (for example, virtual machines or blade PCs)

• Citrix Machine Creation Services (MCS) Click Next to continue the Machine Catalog creation wizard.

![](data:image/png;base64...)

1. On the Master Image page, select the Master machine. Select the minimum functional level for this catalog: 1811 (or newer). Click Next to continue the Machine Catalog Setup wizard.

![](data:image/png;base64...)

1. On the storage and license type page, select the storage and license. Click next.

![](data:image/png;base64...)

1. On the Virtual machines page, select the number of virtual machine to be created and its size .

![](data:image/png;base64...)

1. On the NICs page, verify the NICs on which VM will be created.

![](data:image/png;base64...)

1. On the Disk Settings page, use the setting as required and click next.

![](data:image/png;base64...)

1. On the resource group page select to create a new resource group or select an existing one.
2. On the Machine identities page, select the OU path where the VM needs to be created and also the VM name.

![](data:image/png;base64...)

1. On domain credentials page, provide the domain credentials and click next.
2. On the Scope page, accept the default for scope and click next.
3. Workspace environment Management (optional) click next.
4. On the summary page, review the configuration and enter the required information. Click Finish.
   1. Create Server OS Delivery Group for MCS Created Machines
5. Open Citrix Studio (cloudxdsite) in Citrix cloud and click Delivery Groups. In the Actions pane on the right, click Create Delivery Group.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the Introduction page, click Next to continue the Delivery Group creation wizard.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. On the Machines page, verify that the previously created Machine Catalog is listed. Select that Machine catalogue.

Scroll down to find the Number of Machines for the delivery group and choose the number of Machine you required to add in the delivery group.

![](data:image/png;base64...)

1. Choose Leave user management to the Citrix Cloud this makes the Delivery Group available as a Library offering you can assign to users. Click Next.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the Applications page, click Add and select from start menu. You can add application from the server start menu or you can manually add the application. Click ok after selecting the application. Click Next to continue with Delivery Group creation.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. Scope: Choose the default and Click Next.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. Select the use site License option.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. On the Summary page, verify the previously configured information. Click Finish and delivery group will be created.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

* 1. Verify Citrix Cloud Connector are online or not.

1. Login into Citrix cloud Portal.
2. Click on Resource locations on the home page or click on the menu option on the top left hand corner.

![](data:image/png;base64...)

1. Verify the location for which you need to see the cloud connector. Click on Cloud Connectors.

![](data:image/png;base64...)

1. Green indicates the Cloud connector are online. Click on 3 dots for more option.

![](data:image/png;base64...)

1. We can run health check for the cloud connectors and also see the Connector data for past 24 days.

![](data:image/png;base64...)

6. 10. Cloud Connector Session failover

![](data:image/x-emf;base64...)

* 1. Cloud Connector CDF tracing

1. Login to Citrix cloud connector and navigate to file explorer.
2. In File Explorer, navigate to C:\Logs. Within the C:\Logs folder, double-click Rotate CDF.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

Note: Running Rotate CDF does not start an interactive application; however, a .zip file is generated in a separate folder.

1. In the File Explorer, navigate to C:\Logs\CDF.Right-click the most recently generated CdfCapture.2xxxx.zip file and select Extract All.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Right-click the folder destination path, within the Files will be extracted to this folder: box and select Copy. On the Select, a Destination and Extract Files dialog box, click Extract.

![Table

Description automatically generated with medium confidence](data:image/png;base64...)

1. ![Graphical user interface, text, application

   Description automatically generated](data:image/png;base64...)Using File Explorer, navigate to C:\CDFControl and double-click CDFControl.exe.
2. Click File and select Load CSV (CDF) File.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. In the Address bar, paste the previously copied destination folder and double-click the CdfCapture.2xxxx.csv file.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. The results of the CDF Trace are displayed within the CDFControl Application. Select the Class column, and click Error

![Graphical user interface

Description automatically generated](data:image/png;base64...)

Interact with the results and verify that you can see messages about a service outage

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

Note: You can use View > Find to do a keyword search for specific terms.

1. Click X in the top-right corner to close the CDFControl application.
2. Right-click Start and click Command Prompt (Admin).

In the Command Prompt Type: netsh interface ip set address "Ethernet" static <IP>. Press Enter

1. Close the Command Prompt and any open applications or folders, then sign out of the VM.
2. Sign in using your cloud credentials. Click the Fly-out menu and select Resource Locations.
3. On the New York Data Center Resource Location card, click 2 Cloud Connectors

![Table

Description automatically generated with low confidence](data:image/png;base64...)

1. Click the three dots menu to the right of domain and select Run Health Check.
2. Wait for the health check to complete and verify that the connector has established communication with the Citrix Cloud Site.
   1. Monitor the Site with Cloud Director and Application Analytics.
3. At the top left of the Citrix Cloud page, click the Fly-out menu. Select My Services > Virtual Apps and Desktops.

![Graphical user interface, text, application, chat or text message

Description automatically generated](data:image/png;base64...)

1. Click the Monitor tab.

![Graphical user interface, text, application, chat or text message

Description automatically generated](data:image/png;base64...)

1. After a few seconds, you are automatically logged into Citrix Director.
2. From the Desktop, start Chrome and browse to <https://storefront.workspacelab.com>. Log on.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Click the DESKTOPS tab. Click to start Windows 2016 Server Desktop.
2. Once the Server Desktop is launched, click Start and select Paint within the ICA session.
3. Return to the Citrix Cloud tab in Chrome, you can expand the menu for graph view.

![Graphical user interface

Description automatically generated](data:image/png;base64...)

1. Validate that it now shows 1 session is now connected.

![Graphical user interface, application, Word

Description automatically generated](data:image/png;base64...)

Click the numeric 1 above Sessions Connected to view the session details.

1. Under the Sessions node, click HR1 to view the details of this session.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. ![Graphical user interface

   Description automatically generated](data:image/png;base64...)Click the Shadow button on the left. This will download invite.msrcinsident.
2. Click invite.msrcindent at the bottom-left of the Chrome browser and select Open.
3. A Windows Remote Assistance window opens up, indicating that it is waiting on a response from the remote user.

![Shape

Description automatically generated](data:image/png;base64...)

1. Switch back to the Windows 2016 Server Desktop launched as the HR1 user. Click Yes on the Windows Remote Assistance prompt.

![Graphical user interface, application, Word

Description automatically generated](data:image/png;base64...)

1. ![A picture containing text, screenshot, monitor, indoor

   Description automatically generated](data:image/png;base64...)Return to Windows Remote Assistance – Helping HR1 window and validate that you can shadow the desktop session of the HR1 user. Click Request Control on top of the Windows Remote Assistance window.
2. Switch back to Windows 2016 Server Desktop launched as HR1 user. Click Yes on the Windows Remote Assistance prompt inside the Windows 2016 Server Desktop.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. Return to Windows Remote Assistance – Helping HR1 window and validate that you can control the HR1 user’s session.

![A picture containing text, monitor, screenshot, computer

Description automatically generated](data:image/png;base64...)

1. Click X to close the Windows Remote Assistance-Helping HR1 window and release the control on the HR1 user’s session.
2. ![Graphical user interface, text, application

   Description automatically generated](data:image/png;base64...) Switch back to the Google Chrome browser, on the top-right corner click the Details button\ . Note: If your screen resolution is limited, you may need to scroll sideways in the browser to see the Details button.
3. Within the Details view, click Processes. Navigate to find mspaint.exe and click to select it.
4. ![A picture containing table

   Description automatically generated](data:image/png;base64...)After selecting mspaint.exe, the End Process button becomes active. Click End Process to stop the Paint application running inside HR1 Server Desktop.

![Graphical user interface, website

Description automatically generated](data:image/png;base64...)

Click Yes on the End Process Confirmation.

1. Switch back to the Windows 2016 Server Desktop and verify that Paint was successfully terminated by the Cloud Director.
2. On the Google Chrome browser, click the Session Control button under Session Details right side of the browser window and select Log Off.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Wait for the log off to complete. Verify the information message: User is currently not connected.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. ![A screenshot of a computer

   Description automatically generated](data:image/png;base64...)In Cloud Director, click the Applications tab to open Application Analytics.
2. ![Graphical user interface

   Description automatically generated with medium confidence](data:image/png;base64...)Scroll down to Review the Application Analytics page.

Note: Application Analytics is a new feature that allows you to validate the health of your published applications in real-time

* 1. Determine hourly usage of VDAs

1. At the top left of the Citrix Cloud page, click the Fly-out menu. Select My Services > Virtual Apps and Desktops.
2. Click the Monitor tab.

![Graphical user interface, website

Description automatically generated](data:image/png;base64...)

1. ![Graphical user interface, application

   Description automatically generated](data:image/png;base64...)Select the Trends tab.
2. Click Custom Reports and select Create Reports.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. Verify that Custom Query is selected, and enter the following information:

• Report Name: VDA Usage

• Type: Sessions

• Conditions: Custom; From: Month-Start-Date; To: Month-End-Date

• Output Columns: Session State, Machine Name, Session Start Time, Session End Time, Catalog Name Note.

Click the + button to add Output Columns

![Graphical user interface, text, email

Description automatically generated](data:image/png;base64...)

1. ![Graphical user interface, application

   Description automatically generated](data:image/png;base64...)Scroll down and select Preview to view the output of the above query.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

Click X at the top after you see the preview.

1. Click the Save button at the bottom to save the custom report.

On the saved query page, then click Run and Download to download the data in a CSV file.

![A picture containing graphical user interface

Description automatically generated](data:image/png;base64...)

1. Wait for the file to download. Click the VDA Usage.csv file at the bottom-left corner to open the file using MS Excel.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Click the Select All button on the top left of the worksheet.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. ![Graphical user interface, application, table, Excel

   Description automatically generated](data:image/png;base64...)Within the Home menu, click the Sort and Filter drop-down menu and select Filter.
2. In the Session State column select Terminated sessions.In the Machine Name column select WORKSPACELAB\NYC-SRV-002. In the Catalog Name column select NYC-CAT-ServerOS.

The filtered output looks like

![Graphical user interface, table

Description automatically generated](data:image/png;base64...)

1. Type the following information in Cells F1, G1, and H1

• F1: Start Time

• G1: End Time

![](data:image/png;base64...) • H1: Time Difference

1. ![Graphical user interface, application, Word

   Description automatically generated](data:image/png;base64...)Select Columns F and G. Change the Number format to Time. Click the Number format drop-down menu and select Time.
2. Select column H, right-click and select Format Cells.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Select Custom under category and select h:mm:ss under type: Click OK.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. Type formulas for calculation in each of the cells.

In cell F2 type: =TIMEVALUE(C2)

In cell G2 type: =TIMEVALUE(D2)

In cell H2 type: =G2-F2

Note: =TIMEVALUE converts string data type to time. =G2-F2 is used to calculate the difference between the two time values.

1. Double-click on the bottom right corner of F2, G2, H2 to apply the formula to the entire column and get the respective output for each column.

![Graphical user interface, application, table, Excel

Description automatically generated](data:image/png;base64...)

1. Select all values in the Time Difference column and click AutoSum.

![Table

Description automatically generated](data:image/png;base64...)

Note: Do not select the entire Time Difference column but only the values. 295 AutoSum will add all the selected values and show the result at the bottom. The AutoSum result shows the actual usage of the machine (NYC-SVR-001) for the entire month. You could also use pivot tables to view the usage data for each machine or create graphs.

1. Close the VDA usage.csv file by clicking X on the top-right corner. Click Don’t Save, when prompted.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

* 1. Citrix License Status

![cid:image001.png@01D90FCB.5F76A8D0](data:image/png;base64...)To view Citrix License Server usage insights, select Licensing from the console menu and then select Licensed Deployments.

![](data:image/png;base64...)

* 1. Configure Citrix policy

1. Login into Citrix Cloud portal and click on DaaS.
2. Under Manage tab click on Policies from left menu.
3. Click on Create Policy.
4. Add and configure Policy settings
5. Specify how to apply the policy by choosing one of the following:
   1. Assign to selected user and machine objects and then select the user and machine objects to which the policy will apply.
   2. Assign to all objects in a site to apply the policy to all user and machine objects in the Site.
6. Enter the policy name and description and click on Finish.

![C:\Users\yadavu01\Downloads\1.png](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/png;base64...)

* 1. How to create an Application Group.

In Daas Portal, right-click Applications under Manage Tab, and click Create Application Group.

![](data:image/png;base64...)

1. In the Getting Started page, click Next.

![](data:image/png;base64...)

1. In the *Delivery Groups* page, select the delivery groups you want these apps published from.

![](data:image/png;base64...)

1. In the Users page, select the users that can see the apps in this app group.
2. Note: there are three levels of authorization. An app is only visible to a user if the user is assigned to all of the following:

Delivery Group

Application Group

Individual Published Apps in the Application Group

1. Click Next.![](data:image/png;base64...)
2. In the *Applications* page, publish applications like normal. The Existing option lets you select an app that’s already been published to a different Application Group or Delivery Group. Click Next.

![cid:image001.png@01D90C51.ACCADAC0](data:image/png;base64...)

1. In the Summary page, give the Application Group a name, and click Finish.

![](data:image/png;base64...)

* 1. How to delete an application group /application.

Deleting an application does not delete it from its original source, but if you want to make it available again, you must add it again.

1. Select Applications in the Studio navigation pane.
2. Select an Application Group in the middle pane and then select Delete Group in the Actions pane.
3. Confirm the deletion when prompted.
   1. How to create a Master Image

The MCS Master Image will be created using the Windows 2016 D series instance from Azure.

The following is a step-by-step of the image creation process:

* Install Windows 2016 Server on Azure Cloud.
* Update Windows with all hotfixes and patches from Microsoft
* Join the domain, with Citrix Administrators as part of local administrator’s group
* Configure DNS settings, Network Settings
* Install core applications.
* Agents for Management, Monitoring, and Operation
* Install Citrix VDA.
* Create string value List of Delivery Controller (Cloud connectors) and point it at the appropriate Delivery Controllers under
* HKEY\_LOCAL\_MACHINE\SOFTWARE\Citrix\VirtualDesktopAgent
  1. Master Image Update

1. Login to Azure Portal and navigate to virtual machine.

![Graphical user interface, application, table

Description automatically generated](data:image/png;base64...)

1. ![Graphical user interface, text, application, email

   Description automatically generated](data:image/png;base64...)Select the required Master Image machine and go to disk option of the Virtual Machine. Click on the VM Disk name.
2. Select create Snapshot for taking a snapshot of the Virtual Machine.

![Graphical user interface, application

Description automatically generated](data:image/png;base64...)

1. Provide the information required on the Basic page of Snapshot creation process. (Naming convention of snapshot yet to be decided). Select the required option from Encryption, Networking, Advanced and Tag option.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. After selecting the required details review the change and then Click on Review+create.

![](data:image/png;base64...)

1. Perform the required Update in existing application or Add new application in the Master Image.
2. Then go to Azure Portal select the master image (Particular Image which we need to update).

![Graphical user interface, text, application, Word, email

Description automatically generated](data:image/png;base64...)

1. Under the overview select capture and select the appropriate gallery (for particular gallery created by environment).

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. OS should be specialized then we need to provide latest version name. If OS is generalized, all installed applications need to be tested/validated by application owner.

![](data:image/png;base64...)

1. Then Click on Review + Create then Image will be captured.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. Then login to Citrix cloud and navigate to machine Catalog. Select the machine catalog which needs to be updated and then right click on it and select update the machines.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. Click on Next, Under Master Image click on Select an image.

![Graphical user interface, text, application, email

Description automatically generated](data:image/png;base64...)

1. We need to select the latest version under citrix master image gallery.

![](data:image/png;base64...)

1. Select the Rollout Strategy as Immediately Restart.

![](data:image/png;base64...)

1. Click on next and finish.

![](data:image/png;base64...)

* 1. Troubleshooting and providing solution for application issue

1. Application launch issue

* From user end,we will check Citrix workspace version on user base machine and if its not the latest version then will ask user to get reset the citrix workspace or will update it to latest version.
* From Citrix end, we will check user session on director whether it is in hung or disconnected state. If there is no hung/disconnected session then we will check status of server which user session is trying to connect.

1. Login/Access issue

* We will check user account status whether it is locked.
* Will check whether user is part of application group or not.
* We will check status of server whether it is up and running.

1. Performance issue

* We will check utilization (CPU, RAM, Memory, disk space) of server.
* We will check session status of the server (it should be load balance within all the server)
* In case of high latency issue, we need to check internet speed (Limited bandwidth).
  1. Monitoring of the Storefront server and its services.

Citrix StoreFront is an enterprise app store for users that aggregates and presents virtual app and desktop resources from on-premises and hybrid deployments—delivering a near-native user experience across Citrix Workspace app (formerly Citrix Receiver) on any platform.

The below task should be done to check if the storefront server is running fine.

* Citrix Storefront server should be up and running and its Storefront services.
* Citrix Storefront console should be accessible.
* If the environment has more than 1 Citrix storefront server then after doing any change on any of the server, it should be propagated to other server by clicking Propagate changes from the action pane.

![Graphical user interface, text, application

Description automatically generated](data:image/jpeg;base64...)

* 1. Managing User and VM’s Session in Citrix Studio.

**Virtual Machine**

1. Select Delivery Groups in the Studio navigation pane.
2. Select a group and then select View Machines in the Actions pane.
3. Select the machine and then select one of the following in the Actions pane (some options may not be available, depending on the machine state):
   * Force shut down. Forcibly powers off the machine and refreshes the list of machines.
   * Restart. Requests the operating system to shut down and then start the machine again. If the operating system cannot comply, the machine remains in its current state.
   * Force restart. Forcibly shuts down the operating system and then restarts the machine.
   * Suspend. Pauses the machine without shutting it down, and refreshes the list of machines.
   * Shut down. Requests the operating system to shut down.

**End user Session /Access in Citrix Studio.**

Change user settings in a Delivery Group

* + Select Delivery Groups in the Studio navigation pane.
  + Select a group and then select Edit Delivery Group in the Actions pane.
  + On the User Settings (or Basic Settings) page, change any of the settings in the following table.
  + Click Apply to apply any changes you made and keep the window open or click OK to apply changes and close the window.

Add or remove users in a Delivery Group

* + Select Delivery Groups in the Studio navigation pane.
  + Select a group and then select Edit Delivery Group in the Actions pane.
  + On the Users page, to add users, click Add, and then specify the users you want to add. To remove users, select one or more users and then click Remove. You can also select/clear the check box that enables or disables access by unauthenticated users.
  + Click Apply to apply any changes you made and keep the window open or click OK to apply changes and close the window.

Log off or disconnect a session

* + In the Studio navigation pane, select Delivery Groups.
  + Select a delivery group and then select View Machines in the Actions pane.
  + In the middle pane, select the machine, select View Sessions in the Actions pane, and then select a session. Alternatively, in the middle pane, select the Session tab and then select a session.
  + To log off a user from a session, select Log off in the Actions pane. The session closes and the user is logged out. The machine becomes available to other users unless it is allocated to a specific user.
  + To disconnect a session, select Disconnect in the Actions pane. Applications continue to run in the session and the machine remains allocated to that user. The user can reconnect to the same machine.
  1. How to install Virtual delivery agent.

Citrix periodically releases Cumulative Updates for LTSR versions of VDA. Download the latest Cumulative Update from Citrix website.

1. Mount the downloaded [XenDesktop ISO](https://www.citrix.com/downloads/citrix-virtual-apps-and-desktops/product-software/xenapp-and-xendesktop-715-ltsr-cu9-all-editions1.html).
2. Run AutoSelect.exe from the ISO.
3. Click Start next to either XenApp or XenDesktop. The only difference is the product name displayed in the installation wizard.

![](data:image/png;base64...)

1. On the top right, click Virtual Delivery Agent for Windows Server OS.

![Graphical user interface

Description automatically generated](data:image/png;base64...)

1. In the Environment page, select Create a Master Image, and click Next.

![](data:image/png;base64...)

1. In the Core Components page, if you don’t need Citrix Workspace App (formerly known as Receiver) installed on your VDA, then uncheck the box. Workspace app is usually only needed for double-hop ICA connections (connect to the first VDA, and then from there, connect to the second VDA). Click Next.

![](data:image/png;base64...)

1. In the Additional Components page select option as per requirement and click on Next

![](data:image/png;base64...)

1. In the Delivery Controller page, select Do it manually. Enter the FQDN of each Delivery Controller (at least two). Click Test connection. And then make sure you click Add. Click Next when done.

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

![](data:image/png;base64...)

1. In the Features page, if you want to use the features, then check the boxes. Remote Assistance is for Director. Then click Next.

![](data:image/png;base64...)

1. In the Firewall page, VDA 2112 and newer have ports 52525 – 52625 for [Screen Sharing](https://docs.citrix.com/en-us/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/graphics-policy-settings.html#screen-sharing). Click Next.
2. In the Summary page, VDA 2109 and newer have an optional Enable restore on failure checkbox. click Install.

![](data:image/png;base64...)

1. Click Close if you are prompted to restart.

![](data:image/png;base64...)

1. After the machine reboots twice, login and installation should continue automatically
2. In the Diagnostics page, you can optionally check the box next to Collect diagnostic information, click Connect, enter your Citrix account credentials, and then click Next.

![](data:image/png;base64...)

1. In the Finish page, click Finish to restart the machine again.

![](data:image/png;base64...)

* 1. Monitoring of Real User sessions and Citrix Connections failures

To access Monitor, sign in to [Citrix Cloud](https://citrix.cloud.com/). In the upper left menu, select My Services > DaaS. Click Monitor.

![](data:image/png;base64...)

Monitor provides:

* Real-time data from the Broker Agent using a unified console integrated with Analytics and Performance Manager.
* Analytics includes performance management for health and capacity assurance, and historical trending to identify bottlenecks in your Citrix DaaS environment.
* Historical data stored in the Monitor database to access the Configuration Logging database.
* Gain visibility into the end-user experience for virtual applications, desktops, and users for Citrix DaaS.
* Monitor uses a troubleshooting dashboard that provides real-time and historical health monitoring of Citrix DaaS. This feature allows you to see failures in real time, providing a better idea of what the end users are experiencing.
  1. Monitoring of application failure from Citrix director

Log in to Director -> Click Trends -> Click Application Failures

![](data:image/png;base64...)

The Director console queries failures from the Monitor service and displays them in a tabular format.
The following filters are supported for Faults and Errors:

* Application Name (Name given for Admin on Studio)
* Process Name (Ex: outlook.exe)
* Delivery Group
* Time range: Last 2 hours, Last 24 hours, Last 7 days, Last month, Custom Time Period

**Application Faults**

![](data:image/png;base64...)

**Application Errors**

![](data:image/png;base64...)

* 1. Provide application access to end user

1. We can use the published app’s Limit Visibility page to provide/restrict user access to an application.
2. In Daas, select application menu on the left hand side. Click on the application in which access is to be provided or revoked. Click on properties.

![](data:image/png;base64...)

1. ![](data:image/png;base64...)In application settings menu click on Limit Visibility and then click on add option to add the user.
2. Click on save and the application access will be provided to the use.
   1. Pull custom report of End user from Citrix Director
3. In Citrix cloud click on Monitor-> Click on Trend-> Click on Custom Reports.
4. Fill all the required details and customize report as per your requirement.

![](data:image/png;base64...)

* 1. Management of Citrix URL Certificate

![](data:image/x-emf;base64...)

* 1. How to install an application in Session Host server and publish it to End User?

We will install required application in a session host server (Windows 2016) with the help of Windows team and the requestor/requestor’s team.

Once application will be installed in the server and its running successfully, we will publish it.

* Select Applications under Manage Tab and then select Add Applications in the Right Side pane.
* The Add Applications wizard launches with an Introduction page, which you can remove from future launches of this wizard.
* In Add Application window Click on Add->Click on Manually

![cid:image001.png@01D90B96.9C61DF00](data:image/png;base64...)

Manually defined: Applications located in the site or elsewhere in your network. When you select this source, a new page launch. Enter the path to the executable, working directory, optional command line arguments, and display names for administrators and users. After entering this information, click OK.

![](data:image/png;base64...)

* 1. How to access Azure File Share.

1. ![](data:image/png;base64...)On the Azure portal homepage, Select storage accounts. In order to build a Azure file share we need a storage account.
2. Please select the required storage accounts from the list on the Storage page. stctxnprodeus01 is Non-prod storage and stctxprodeus01 is the Prod storage. Both are in SUB-MSHS-CORE Subscription.

![](data:image/png;base64...)

1. Click on File shares option(stctxnprodeus01) on the left pane.

![](data:image/png;base64...)

1. We will get the below screen after we click on file share. Click on Ctx-xenapp-nonprod to access the Non-Prod Azure file share.

![](data:image/png;base64...)

1. We will get the folder for Dev and QA (Non-prod) as given below.

![](data:image/png;base64...)

1. Click on Dev folder. We will be able to see the content of the Dev folder where Mandatory profile and Scripts have been kept.

![](data:image/png;base64...)

Note: In Azure File share we are keeping Citrix Mandatory Profile and also the application and startup script in this Files share.

* 1. Configuring TLS 1.0 for TRAC applications VDA server

1. We have a separate delivery group for Trac application because they require TLS 1.0. We have kept the Trac server in different delivery group. The TLS 1.0 has been enabled through remote Startup script which has been kept on AFS share.
2. The server needs to be part of CTX-SRV-TLS1.0-Enable AD group for TLS 1.0 to enable on that server.
3. To check if the TLS1.0 has been enabled on the server we need to navigate to registry.
4. To open registry setting go to start menu and search regedit. Navigate to path HKEY\_LOCAL\_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols in registry.

![](data:image/png;base64...)

* 1. License clean up

* 1. Check .Net Framework Path
  2. Click on Start and open Run. Open regedit.
  3. Navigate to Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full. Select Version to see the latest version.

![](data:image/png;base64...)

* 1. Renewal of Citrix Storefront Certificate

1. Once we receive the certificate from the respected team we need to download it and import it on the server.

![](data:image/png;base64...)

1. Browse the certificate path where it is stored/downloaded.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. It will ask for password where we need to provide the password which we downloaded during the certificate export.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Select the Automatic option.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Click on Finish option once done.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Finish certificate import pop-up will come.

![A screenshot of a computer error

Description automatically generated](data:image/png;base64...)

1. Go to the server IIS console.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Check the certificate which you recently onboarded is reflecting or not.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Now come to Default website option to Bind the certificate with https store. Select the Bindings option on the right hand side corner.

![](data:image/png;base64...)

1. Select the https option and click on EDIT.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Click on the SSL Certificate dropdown option and select the latest renewed certificate. Post selecting click on the VIEW option to validate the cert. Click on OK to finish the process.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

* 1. Time Zone of newly created Virtual Machine

1. When a new Virtual Machine is hand over, we need to check the time zone of the server.
2. Basically the time zone is in UTC time zone.
3. If the time zone is in UTC. Open PowerShell as admin and run the following command: Set-TimeZone -Id "Eastern Standard Time"
4. The above command will set the time zone to EST. it doesn’t require a reboot.
   1. Post reboot activity if any error occurs need to follow the steps.

On the AIRS VDA server there was an startup script error found which caused this issue. All the users who launched the application they were also got the below error while application launched.

![](data:image/png;base64...)

Logged in to the server SCTXAIRP019002 and open the Task Scheduler to run the task once again. Post running the task the pop-up went away and the issue got resolved.

Post every server restart/reboot, login to the server and check the start up task Job status on Task Scheduler. The Task scheduler Job status should be Ready and no error pop-up on the screen. Patching

* 1. Citrix Core Servers Patching

Windows Team will do the OS patching of Citrix core server and once the servers are patched Citrix team will reboot the server sequentially.

Please refer to section 19 in Windows Runbook.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the link for Windows patching details.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/BusinessCaseValidation/Ee4jJcc1xxFFmexN4rpnz6sBnWtrjw_qmABFbGLl8PCcbw?e=M7Unqx) | | |

* 1. Standalone OS Citrix VDA Patching

Windows Team will do the Standalone Server patching of Citrix Standalone server and once the servers are patched Citrix team will reboot the server sequentially.

Please refer to section 19 in Windows Runbook.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the link for Windows patching details.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/BusinessCaseValidation/Ee4jJcc1xxFFmexN4rpnz6sBnWtrjw_qmABFbGLl8PCcbw?e=M7Unqx) | | |

* 1. MCS Managed Citrix VDA Patching

Please find below document for patching process

![](data:image/x-emf;base64...)

Note: For both the Onprem and azure environment we should raise separte changes for the non prod environment. Once the signoffs are received for the environment then Prod change request should be raised.

* 1. How to Publish an application icon

1. Login to Citrix Studio Server and open Citrix Studio Console.
2. Navigate to Application option on the left side as shown below.

![](data:image/png;base64...)

1. Click on Add Application.
2. Introduction page will appear. Click on next.
3. Select the application group where the new application will be placed and the delivery group from which the application will be published.

![](data:image/png;base64...)

1. Add the application from the Start menu or from a specified path as per the requirement.

![](data:image/png;base64...)

1. Check the details on summary page and click finish. The application will be published.
   1. Install Server OS VDA
2. Login to server go to CVAD iso file location **Path: C:\Windows\temp \Citrix.**

![](data:image/png;base64...)

1. Right click on it and click on Mount.

![](data:image/png;base64...)

1. The mount file will be reflect on This PC .Open file by using double click ,next Right click on the Auto select and select Run as administrator

![](data:image/png;base64...)

1. It will pop up below window. Allow it by Clicking on Yes.

![](data:image/png;base64...)

1. Start the Virtual apps and desktops

![](data:image/png;base64...)

1. On the top right, Click on Virtual delivery agent for windows Multisession OS

![](data:image/png;base64...)

1. In the Environment page, Snect Enable Brokered Connection to a Server ,and click Next

![](data:image/png;base64...)

1. In the core components page, keep the fields as it is ,click Next

![](data:image/png;base64...)

1. In the Additional components page, No changes keep all the fields as it is and click Next

![](data:image/png;base64...)

1. In the Delivery controller,Dropdown and select Do it later(Advanced) (because it is already having in GPO),Click Next

![](data:image/png;base64...)

Se

1. Pop window will come, Click on Yes

![](data:image/png;base64...)

1. In features,Keep the fields as it is and click Next

![](data:image/png;base64...)

1. In Firewall page ,Keep the fields as it is and click Next.

![](data:image/png;base64...)

1. In the summary page Check all things and click on Install .The Machine will restart before installation ,click on Close. Machine will restart

![](data:image/png;base64...)

1. Once the Server is up .Repeat the steps from 1 to 6.

![](data:image/png;base64...)

1. In the Install page, wait until all required prerequisites and core components& post install steps to be completed.

![](data:image/png;base64...)

1. Uncheck the Diagonstic collect information , click Next

![](data:image/png;base64...)

18.In the finish page, click on finish to restart machine again.

![](data:image/png;base64...)

19.Login the serveronce server came up ,Check the CVAD installed on the server

![](data:image/png;base64...)

**Creating Machine Catalog in Citrix Cloud**

1. In DaaS , Click Machine Catalogs on the left . Click Create Machine Catalog.
2. On the Operating System page, verify that Multi-session OS is selected and click next.

![](data:image/png;base64...)

1. On the Operating System page, verify that Multi-session OS is selected and click next.

![](data:image/png;base64...)

1. On the Machine Management page, verify that the below two options are selected:

• Machines that are power managed

• Citrix Machine Creation Services (MCS) Click Next to continue the Machine Catalog creation wizard.

![](data:image/png;base64...)

1. Add VM’s on the virtual machine page by selecting appropriate location and click Ok.

![](data:image/png;base64...)

1. On virtual machine page click on Browse and enter the server name and click on check names and click on done.

![](data:image/png;base64...)

1. Select the Zone as Prod East us and click Next

![](data:image/png;base64...)

1. In Scope ,Select the CMS Access,Click Next

![](data:image/png;base64...)

1. Keep the fields as it is in WEM page ,Click Next

![](data:image/png;base64...)

1. Keep the fields as it is On VDA upgrade page ,Click Next

![](data:image/png;base64...)

1. In Summary page ,Provide the Machine catalog name and Click Finish. Machine catalog has created and will reflect in Machinecatalog.

![](data:image/png;base64...)

**Creating Delivery Group for Server**

1. In DaaS , Click Delivery Group on the left . Click Create Delivery Group.
2. On the Introduction page, click next to continue the Delivery group Setup wizard.

![](data:image/png;base64...)

1. On the Machines page, verify that the previously created Machine Catalog is listed. Select that Machine catalogue.

Scroll down to find the Number of Machines for the delivery group and choose the number of Machine you required to add in the delivery group

![](data:image/png;base64...)

1. No changes in Load balancing page Click Next

![](data:image/png;base64...)

1. In Users, Select authenticated users and session roam with users as shown below and click next

![](data:image/png;base64...)

1. In Application page no apps as of now so ,Click next
2. In Desktop page, No changes, click Next

![](data:image/png;base64...)

1. In Application Page,No changes click Next

![](data:image/png;base64...)

1. In Scope ,Select CMS Access and click Next

![](data:image/png;base64...)

1. Select the Use the site license in License agreement page ,Click Next

![](data:image/png;base64...)

1. On the Summary page, verify the previously configured information and provide the DG name . Click Finish and delivery group will be created.

![](data:image/png;base64...)

1. Click on Yes if below window pop up and delivery group will be created

![](data:image/png;base64...)

1. You can check the newly created delivery group and machines in Citrix Daas.

![](data:image/png;base64...)

* 1. Master image sealing

1. Once the server is up and running. Login to master image and download the latest Security patch released by Microsoft on every Tuesday and save in temp.
2. Need to enable Windows update Service and install the KB`s and don`t restart the machine and disable Windows update service.
3. Open command Prompt and update latest Edge Version from mentioned Path([\\ctx18\XenAppEng\Dev\IMS\MicrosoftEdge\x64\Install.vbs](file://ctx18/XenAppEng/Dev/IMS/MicrosoftEdge/x64/Install.vbs)).
4. Open command Prompt and update latest Acrobat Reader from mentioned path([\\ctx18\XenAppEng\Dev\IMS\AcrobatReader\DC\Install.vbs](file://ctx18/XenAppEng/Dev/IMS/AcrobatReader/DC/Install.vbs)).
5. We need to Delete below registry values for Crowd strike:
   1. HKEY\_LOCAL\_MACHINE\SYSTEM\CrowdStrike\{9b03c1d9-3138-44ed-9fae-d9f4c034b88d}\{16e0423f-7058-48c9-a204-725362b67639}\Default\AG
   2. HKEY\_LOCAL\_MACHINE\SYSTEM\CurrentControlSet\Services\CSAgent\Sim\AG

6. Need to follow below step for Tenable.

1.Stop the Tenable Nessus Agent service.

2.Run below command in command PromZEUSpt:

cd C:\Program Files\Tenable\Nessus Agent >nessuscli.exe prepare- image

3.Start the Tenable Nessus Agent service.![](data:image/png;base64...)

7. Open Command Prompt and update Splunk by using below command.

c:\program files\SplunkUniversalForwarder\bin\splunk.exe clone-prep-clear-config

1. Check All Automatic services are up and running.
2. Open Control panel and check whether NXLog has been installed or not.
3. Need to Clean up C drive Temp and Recycle bin.
4. Logout and login with Local account to perform Profile Clean up, Except system account need to clean up individual ID`s.
5. Once Done Restart the Master Image.

11.43 How to access Citrix Director

* 1. Login to the below URL for access EPIC Director

<https://epicdir.mountsinai.org>

![](data:image/png;base64...)

![](data:image/png;base64...)

* 1. Login to the below URL for access Non-EPIC Director

<https://ctxdir.mountsinai.org>

![](data:image/jpeg;base64...)

![](data:image/png;base64...)![](data:image/png;base64...)

11.44 How to Generate reports from Citrix Director

* 1. Login to the Citrix Director as shown below with pa credentials.

![](data:image/png;base64...)

* 1. Navigate to Trends and you can show custom reports as sown below

![](data:image/png;base64...)

* 1. Need to click and create Report and fill the required fields and save the report for next use and directly we can click the report and it will automatically generate the report.

![](data:image/png;base64...)

1. Post Server Build Steps

12.1 Citrix Server Configuration Check

12.1.1 Check resource group name, Status of VM, Subscription name, Operating system, Instance,

Vnet/Subnet.

* 1. Login into Azure portal <https://portal.azure.com> with your MSHS PA ID.
  2. In home page click on Virtual machine then select respective azure VM.
  3. Click on Overview tab, in right pane you can validate Resource group name, Status of VM, Subscription name, Operating system, Instance, Vnet/Subnet.

![](data:image/png;base64...)

12.1.2 Check Storage size of a VM.

* 1. In home page click on Virtual machine then select respective azure VM.
  2. Select disk and in right pane you can validate size of storage.

![](data:image/png;base64...)

12.1.3 Check the OU Path of a VM.

* 1. In home page click on Virtual machine then select respective azure VM.
  2. Select Run command then select RunPowerShellScript and execute the below command to check the OU details of VM

([adsisearcher]"(&(name=$env:computername)(objectClass=computer))").findall().path

![](data:image/png;base64...)

12.2 Citrix Core Server Component Checks

12.2.1 Cloud Connector Checks

1. We will check the server running status.

![](data:image/png;base64...) 2. All the Citrix Services of cloud connector needs to be checked.

3. Refer to Section 11.2 for Cloud connector testing and to verify service outage if one of the cloud connector

Is down.

12.2.2 Storefront Server Checks

1. We will check the server running status.

2. Checking the Citrix Services of Storefront server.

3. Verify the changes done in one storefront server are propagated to another storefront server.

4. Checking the URL configured on the storefront.

5. Installed certificate validity check on the storefront server.

12.2.2 Machine Catalog and Delivery group Checks.

1. Check the machine catalog status.

2. Application Launching from each delivery group.

3. Application performance check.

4. Citrix VDA server or Worker server registration check for each Machine catalog and delivery group.

12.3 Citrix Master Image and VDA Check

1. Citrix Master image running status.
2. Snapshot of the master images.
3. Types of master images and installed application
4. Epic Master image with office.
5. Epic Master image without office.
6. Non-Epic Master image with office.
7. Non-Epic Master image without office.

12.4 Citrix Antivirus Exclusion Check

We need to Check with MSHS security/AV team for the below exclusion are placed for Citrix environment.

Following AV exclusions will be required for Citrix products:

| **Cloud Connector** | |
| --- | --- |
|  |  |
| Files | %SystemRoot%\ServiceProfiles\NetworkService\HaDatabaseName.mdf |
| %SystemRoot%\ServiceProfiles\NetworkService\HaImportDatabaseName.mdf |
| %SystemRoot%\ServiceProfiles\NetworkService\HaDatabaseName\_log.ldf |
| %SystemRoot%\ServiceProfiles\NetworkService\HaImportDatabaseName\_log.ldf |
|  |  |
| Folders | %SystemDrive%\Logs\CDF |
| %ProgramData%\Citrix\WorkspaceCloud\Logs |
|  |  |
| Processes |  |
| %ProgramFiles%\Citrix\XaXdCloudProxy\XaXdCloudProxy.exe |
| %ProgramFiles%\Citrix\Broker\Service\HighAvailabilityService.exe |
| %ProgramFiles%\Citrix\ConfigSync\ConfigSyncService.exe |
|  |  |
| **Virtual Delivery Agent** | |
|  |  |
| Files | %SystemRoot%\System32\drivers\CtxUvi.sys |
| %UserProfile%\AppData\Local\Temp\Citrix\HDXRTConnector\\*\\*.txt |
|  |  |
| Processes | %ProgramFiles%\Citrix\HDX\bin\CtxSvcHost.exe |
| %ProgramFiles%\Citrix\Virtual Desktop Agent\BrokerAgent.exe |
| %SystemRoot%\System32\spoolsv.exe |
| %SystemRoot%\System32\winlogon.exe |
|  |  |
| **Storefront** | |
|  |  |
| Files | %SystemRoot%\ServiceProfiles\NetworkService\AppData\Roaming\Citrix\SubscriptionsStore\\*\*\PersistentDictionary.edb |
|  |  |
| Processes | %ProgramFiles%\Citrix\Receiver StoreFront\Services\SubscriptionsStoreService\Citrix.DeliveryServices.SubscriptionsStore.ServiceHost.exe%ProgramFiles%\Citrix\Receiver StoreFront\Services\CredentialWallet\Citrix.DeliveryServices.CredentialWallet.ServiceHost.exe |

1. Backups

Azure backup Service will be utilized for backup solution. Azure backup performs snapshots of VM disks using volume shadow copy service (VSS).  Backups are stored in a Recovery Vault that is region-specific.  Each Azure VM should be backed up using the Azure Backup Service as a minimum solution. This ensures that the VM itself will be recoverable in the event of a failure.

All Citrix servers will comply with MSHS standards for backup policy regarding frequency and retention of backup.

| Server Role | Backup Content |
| --- | --- |
| File Share | Complete Drive Backup |
| Storefront | System level and IIS Configuration |

For more information on Backup design please refer below.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the link for Backup Runbook.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7B660CBCDF-182E-4265-81FF-3F53D1A87375%7D&file=CMS_Backup_Operations_Runbook_v2.2.docx&action=default&mobileredirect=true) | | |

* 1. Snapshots

The XenApp master images are required to be backed up each month and before each image update activity image update activity. The Snapshots of MCS Master image files can be cleaned up at N-2 level.

1. EPIC

14.1 Epic Environment Configurations

* EPIC Solution EPIC – Please refer Citrix Design Document Section 4.2
* Azure Subscription for EPIC – Please refer Citrix Design Document Section 4.2
* EPIC Session Host Server Details
  + **Prod** - Please refer Citrix Design Document Section 5.2.3
  + **QA** - Please refer Citrix Design Document Section 6.3
  + **Dev** - Please refer Citrix Design Document Section 6.6
  + **DR** - Please refer Citrix Design Document Section 7.2.3
* Epic Master Image Details - Please refer Citrix Design Document Section 9.1
* EPIC Compute Gallery- Please refer Citrix Design Document Section 9.2
* EPIC Machine catalog details - Please refer Citrix Design Document Section 9.4
* Epic Delivery Group details- Please refer Citrix Design Document Section 9.5
* OU Structure Details - Please refer Citrix Design Document Section 13.2

14.2 Issues and Troubleshoot

14.2.1 Epic Error 3500 Issue

1. Please refer below screenshots to refresh Apps if you receive below error or need to access a newly added Citrix icon immediately on your Citrix workspace app:

![](data:image/png;base64...)

1. Go to the Citrix workspace icons from system tray:

![](data:image/png;base64...)

1. Click on the settings icon & select “Refresh Apps.

![](data:image/png;base64...)

1. Then launch the required application icon, the application should launch fine.

14.2.2. Epic Prod Icon is not Launching

1. Refresh application from Settings Icon as mentioned in 15.2.1.
2. Check whether user is using latest Citrix workspace or not.
3. If user is using older version try to uninstall older version and install latest version or if it is latest version try to reset Citrix workspace.
4. Open task manager, and end any Citrix tasks.
5. Check from the EPIC delivery group whether the server on which user has logged in is unregistered or not.
6. If user session is in disconnected state in the delivery group, we need to end the user session and ask the user to launch the application again.
7. If server is unregistered, we need to find the cause and register the server.

14.2.3 Epic Prod Icon is missing

1. Verify if the user is the part of EPIC Ad group which has been added into Citrix Daas portal for EPIC application.
2. Need to check when user has last connected to the application for past few weeks.
3. If user did not use or launch application for more than 30 days then user account will be disabled that may cause user this type of issue.
4. If user is not part of AD user won`t able to view the application, we need to ask user to raise request to view the application.

14.3 Important checks for P2 Incident.

1. We need to check if it is single user issue or multiple user issue.
2. If it is single user incident we can drop mail to Service management team and decrease the priority.
3. If it is multiple user issue we need to check from Server end whether it servers are up and fine and having user sessions.
4. Need to verify if there is any machine catalogue update is done and causing the issues and servers are in unregistered due to update.
5. Need to troubleshoot and fix the issues from our end and try to verify if there is user sessions are active or not.
6. If there are more active sessions and still few users are facing same issue we need to initiate a bridge call with help of SMOC team.

14.4 Epic Applications and Contact Details.

 **Prod-Epic Applications:**

| **Application Name** | **Delivery group** | **Application Owner** |
| --- | --- | --- |
| EPIC Playground | prod-epic | epicinfrastructure@mountsinai.org |
| EPIC Training- Ambulatory | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| EPIC Training- Clinical Documentation ONE | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| Epic TRAINING - Clinical Documentation TWO | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| Epic TRAINING - Master Train | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| Epic TRAINING – CPOE | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| Epic TRAINING – Stage | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| AZ-Test command prompt(disabled) | Prod-EPIC-Training | epicinfrastructure@mountsinai.org |
| Azure prdsmoke | Prod-Epic-Standard | epicinfrastructure@mountsinai.org |
| EPIC-PROD | Prod-Epic-Standard | epicinfrastructure@mountsinai.org |
| Obix Patient Manager | Prod-Epic-Standard | epicinfrastructure@mountsinai.org |
| EPIC-PROD-BI | Prod-EPIC-Office | epicinfrastructure@mountsinai.org |
| Epic Playground\_MSSN | Prod-Epic-MSSN | epicinfrastructure@mountsinai.org |
| Az-Notepad | DR-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Microsoft Edge | DR-EPIC-Standard | epicinfrastructure@mountsinai.org |

 **NonProd-Epic Applications:**

| **Application Name** | **Delivery group** | **Application Owner** |
| --- | --- | --- |
| Epic Playground | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic TRAINING - Ambulatory | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic TRAINING - Clinical Documentation ONE | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic TRAINING - Clinical Documentation TWO | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic TRAINING - Master Train | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic TRAINING – CPOE | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic TRAINING – Stage | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Az-EPIC Training | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic POC | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| EPIC-REL | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic-TST | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic-TSTSAC | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic-TSTVS | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| EPIC-UPG2015 | QA-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic 3M TST | QA-EPIC-3M | epicinfrastructure@mountsinai.org |
| Epic 3M TSTSAC | QA-EPIC-3M | epicinfrastructure@mountsinai.org |
| Epic Bi\_Excel TST | QA-EPIC-OFC | epicinfrastructure@mountsinai.org |
| Epic Bi\_Excel TSTVS | QA-EPIC-OFC | epicinfrastructure@mountsinai.org |
| AZ-Epic-TST | Dev-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic Playground | Dev-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic POC | Dev-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic-TSTSAC | Dev-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Epic-TSTVS | Dev-EPIC-Standard | epicinfrastructure@mountsinai.org |
| Obix Patient Manager V8 | Dev-EPIC-Standard | epicinfrastructure@mountsinai.org |

14.5 Call Tree

* + Please find the below escalation metrics of MSHS.

![image](data:image/png;base64...)

* Escalation metrics of CMS Accenture – Please refer section 24.3

1. Net Scaler

15.1 Components

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer to Net scaler design document mentioned in the link.  [Click Here](https://urldefense.proofpoint.com/v2/url?u=https-3A__ts.accenture.com_sites_MSHSCloudOpsDelivery_Shared-2520Documents_Forms_AllItems.aspx-3Fid-3D-252Fsites-252FMSHSCloudOpsDelivery-252FShared-2520Documents-252FGeneral-252FADM-2520Folder-2520Structure-252F02-252E-2520Transition-252F42-252E-2520Citrix-252FCCS-255FMSHS-255FNetScaler-255Fto-255FAzure-255FDesign-255FRequirements-255FPresentation-255Fv1-252E0-252Epdf-26viewid-3D6b4ae12b-252Df971-252D4bd3-252D8596-252D7029aadc1fa9-26parent-3D-252Fsites-252FMSHSCloudOpsDelivery-252FShared-2520Documents-252FGeneral-252FADM-2520Folder-2520Structure-252F02-252E-2520Transition-252F42-252E-2520Citrix&d=DwMFAg&c=shNJtf5dKgNcPZ6Yh64b-ALLUrcfR-4CCQkZVKC8w3o&r=qgRsCbq-5JOPFg5KNfHFej21-0JmBJkgqw4-S-0pm9IESBaBs-_RUpthQbnEtTku&m=IZ8kKV3dUgbqHkNlENk4EqiN46myNPMwVCcp42InHbISnm5W151DoJ-wAlawrn20&s=XpWwYMkLU4A0WysvIc0ZqcNKeJzlaVGhQ4gbHXNav7c&e=) | | |

15.2 ADC Configuration

1. Check NetScaler version:-

![](data:image/png;base64...)

1. Change Time zone:-

![](data:image/png;base64...)

![](data:image/png;base64...)

1. Verify the IPs with the Azure Portal:-

![](data:image/png;base64...)

1. Delete the Virtual IP and Create SNIP in place of it:-

![](data:image/png;base64...)

1. Verify the ARP table for traffic on 0/1 interface:-

![](data:image/png;base64...)

1. Add License:-

![](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/png;base64...)

1. ![A picture containing text, screenshot, font, line

   Description automatically generated](data:image/png;base64...)Configure HA Pair: -

![](data:image/png;base64...)

1. Create ADC VPX Instance from ADM Portal;
2. Infrastructure > Instances > Citrix ADC

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. Gateway Configuration

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. ![A screenshot of a computer

   Description automatically generated with medium confidence](data:image/png;base64...)Traffic Management > SSL > Import PKCS, Under

![](data:image/png;base64...)

1. We will Install Certificate.CA Certificate:

![A screenshot of a computer

Description automatically generated with low confidence](data:image/png;base64...)

![](data:image/png;base64...)

1. Server Certificate:

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. Link Server Certificate to CA Certificate: -

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. Create VLAN and Bind with IP and Interface: -

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with low confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with low confidence](data:image/png;base64...)

1. Configure RPC Node: - (Not Required for Standalone ADCs)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. System > Settings> Config basic feature then advance features.

![A screenshot of a computer

Description automatically generated with low confidence](data:image/png;base64...)

![Graphical user interface, text, application

Description automatically generated](data:image/png;base64...)

1. Load balance Storefront > Traffic management > Servers

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

![](data:image/png;base64...)

1. Create Monitor: -

Traffic Management > Load Balancing > Monitor

![](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. Select Storefront in Type:-

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Check the highlighted options: -

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. Create Load Balance Service Group: -

Traffic Management > Load Balancing > Service Group

![A screenshot of a computer

Description automatically generated with low confidence](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated with medium confidence](data:image/png;base64...)

1. Bind the Service Group :-

![A screenshot of a service group

Description automatically generated](data:image/png;base64...)

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

15.3 NetScaler upgrade using GUI and CLI

**1. Prerequisite**

1. NetScaler appliance backup should be done before the upgrade.

1.1 To back up a NetScaler appliance, navigate to Backup and restore under System menu.

![](data:image/png;base64...)

1.2 Click on Backup/Import. Provide the desired file name and select “full” in level field. Click on backup.

![](data:image/png;base64...)

1.3 A backup file will be created on the NetScaler.

1.4 Select the backup file which was created. Click on select action and download the backup file.

![](data:image/png;base64...)

2.NetScaler upgrade file should be downloaded and kept at the desired local location before upgrade.

**1.2 NetScaler Upgrade using GUI mode**

1. Login to NetScaler and check the current version of the NetScaler.

![](data:image/png;base64...)

2. Navigate to system. Click on system upgrade.

![](data:image/png;base64...)

3. Under the Firmware option, choose the NetScaler upgrade file from the Local drive.

![](data:image/png;base64...)

4 .Under upgrade options select the checkbox of Reboot after successful installation to reboot the NetScaler appliance after the upgrade.

5 .After the file has been selected, check all the options and click on Upgrade to start the upgrade process.

6. While the upgrade process is underway, please initiate a continuous ping for the NetScaler appliance in which upgrade has been initiated.

7. Once the upgrade is successful, Login to NetScaler and perform the health check.

8. Check the NetScaler version after upgrade has been performed.

**1.3 NetScaler Upgrade using CLI mode**

1. Login to NetScaler and check the current version of the NetScaler.

![](data:image/png;base64...)

1. Keep the Upgrade NetScaler file in the NetScaler appliance.
2. Login into NetScaler via WinSCP to keep the upgrade package in NetScaler. Navigate to /var/install in the NetScaler and drag the file from the local drive to NetScaler.

![](data:image/png;base64...)

1. Once the upgrade file has been kept in NetScaler, SSH to the NetScaler appliance via putty.

5 Login into NetScaler. Run **shell** command and press enter.

![](data:image/png;base64...)

6 . Navigate to the path where the upgrade file has been kept. Run the following command “**CD /var/nsinstall** “ and Press enter. After run ls command to see the file in the folder.

![](data:image/png;base64...)

7. Before you run the install script, the files must be extracted and placed on the appliance. Use the following command to uncompress the bundle downloaded “**tar -zxvf build-xx.x-xx.xx\_nc.tgz”.**

8. While the upgrade process is underway, please initiate a continuous ping for the NetScaler appliance in which upgrade has been initiated.

9. Run the following command to install the downloaded software : **./installns**

10. After the installation process is complete, the process prompts to restart the appliance. Press **y** to restart the appliance.

11. Once the upgrade is successful, Login to NetScaler and perform the health check.

12. Check the NetScaler version after upgrade has been performed.

**1.4 HA Pair Upgrade**

1. Log in to Primary NetScaler and navigate to System >High Availability >Nodes.

![](data:image/png;base64...)

1. Take the screenshot of the nodes in the Primary Netscaler.
2. Login to secondary netscaler and do the upgrade as mentioned in steps 1.2 or 1.3.
3. Once the secondary netscaler is up and running fine login to primary netscaler.

5. Select the secondary netscaler and click on Select Action.Select Force failover . Now the secondary node will have all the roles and features of the primary node.

![](data:image/png;base64...)

6. Once the primary node is also upgraded , do the same process of Force failover and make the node as primary as before.

15.4 Netscalar VAR folder cleanup

1. Open ADM console

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Click on the left side and select infrastructure.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. In infrastructure, open upgrade jobs.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. In upgrade jobs page click on create job.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. In the create maintenance job keep the default option and click on proceed.

![A screenshot of a computer

Description automatically generated](data:image/jpeg;base64...)

1. In the upgrade NetScaler page provide any job name and click on add instances.

![A screenshot of a computer

Description automatically generated](data:image/jpeg;base64...)

1. Select all instances except epic loadbalances, click on OK.

![](data:image/jpeg;base64...)

1. Click on next.

![](data:image/jpeg;base64...)

9. In the select image page click on ADC software image arrow and select any one of the image.

![](data:image/jpeg;base64...)

10. Then click next.

![A screenshot of a computer

Description automatically generated](data:image/jpeg;base64...)

11. Then pre-update validation will be in progress.

![](data:image/jpeg;base64...)

12. Once we get in to the pre-upgrade validation page like below we need to cleanup only instances blocked from update(We will cleanup only which are showing in instances blocked from upgrade).

![A screenshot of a computer

Description automatically generated](data:image/jpeg;base64...)

13. Select one of the instances which you want to cleanup and click on quick cleanup.

![](data:image/jpeg;base64...)

14. The confirm popup will come, Select all and click on YES to proceed cleanup on VAR folder only.

![A screenshot of a computer

Description automatically generated](data:image/jpeg;base64...)

15. Cleanup will take place and just need to wait for some time to be done.

![](data:image/jpeg;base64...)

16. Once the cleanup is done the instance will be visible in the instances ready for upgrade field (That means, they are readily available for upgrade).

![A screenshot of a computer

Description automatically generated](data:image/jpeg;base64...)

17. Once cleanup done for all instances click on CANCEL.

![](data:image/jpeg;base64...)

1. Disaster Recovery

16.1 Disaster recovery of Citrix Cloud Published Non-EPIC APPS Availability during Planned DR TESTING

The instructions listed in the document must be utilized during planned DR testing exercises for Non-epic App availability (as per MSHS DR Manager’s decision).

 **Step 1**: Already completed - **PCA** keyword is added in DR (internal/external) storefronts.

![](data:image/png;base64...)

 **Step 2**: Need to be done during DR testing exercise (When the DR manager shares the list of Non-Epic apps

part of DR testing): **PCA** keyword needs to be added in Application publishing as shown below:

Syntax- KEYWORDS:keyword2<space>keyword2

![image](data:image/png;base64...)

 **Step 3**: After DR testing is completed, remove the PCA keyword from Nonepic icon publishing.

 **\*NOTE**: **On onset of actual DR event only Epic Production application will be available from USSC (DR)**

 **region as none of the Nonepic application available from Citrix cloud+Azure are relevant**

 **candidate of DR.**

Please refer the below screenshot for the testing which is done for Non-Epic Apps enumeration and launch

from USSC Storefront.

![image](data:image/png;base64...)

16.2 Disaster recovery of Citrix Cloud Published for EPIC APPS

Disaster recovery region for EPIC application will be USSC. 450 VDAs have been built in DR region which will be running with the same image as production region VDAs.

We will follow the below steps for planned DR testing of EPIC application.

| **Pre-Failover Citrix Tasks** | |
| --- | --- |
| 1. Send message from Citrix monitor to user connected on Epic Production icon to save work & log off the session | |
| 1. Log off users on agreed timelines from EUS VDAs | |
| 1. Turn On maintenance mode on "Prod-EPIC-Standard" delivery group | |
| **Steps During Failover USSC (From EUS to USSC/DR region)** | |
| 1. Disable GSLB services in EUS ADC (tier 1 - HA pair) - this will failover gateway & storefront to USSC region | |
| 1. Login to Internal EUS HA Pair primary ADC (internal & external) & browser to GSLB<services<Disable East US GSLB services | |
| 1. Login to External EUS HA Pair primary ADC (internal & external) & browser to GSLB<services<Disable East US GSLB services | |
| 1. Login Citrix cloud portal to enable Epic-Production Icon from DR VDAs | |
| 1. Turn Off maintenance mode on "DR-EPIC-Standard" delivery group | |
| **Pre- Failback Citrix Tasks** | |
| 1. Send message from Citrix monitor to user connected on Epic Production icon to save work & log off the session | |
| 1. Log off users on agreed timelines from EUS VDAs | |
| 1. Turn On maintenance mode on "DR-EPIC-Standard" delivery group | |
| **Steps During Failback to EUS (Primary region)** | |
| 1. Enable GSLB services in EUS ADC (tier 1 - HA pair) - this will failback gateway & storefront to EUS region | |
| 1. Login to Internal EUS HA Pair primary ADC (internal & external) & browser to GSLB<services<Enable East US GSLB services | |
| 1. Login to External EUS HA Pair primary ADC (internal & external) & browser to GSLB<services<Enable East US GSLB services | |
| 1. Login Citrix cloud portal to enable Epic-Production Icon from EUS VDAs | |
| 1. Turn Off maintenance mode on "Prod-EPIC-Standard" delivery group |

1. MSSN Environment
   1. How to RDP to a MSSN Server

1. Change the Default RDP port number to :4389 and change the Domain to snchhome.

![cid:image003.png@01D9CA5E.70335850](data:image/png;base64...)

1. Provide the snchhome domain credentials.
2. Click on connect and login into the server.
   1. How to Access Vmware and Virtual machine
3. Login to below Vcenter with PA credentials. Please find the VMware URL below.

<https://opv-vctr-001.snch-home.org/> -OVP MSSN Citrix

<https://hpv-vctr-001.snch-home.org/> - HVP MSSN Citrix

![](data:image/png;base64...)

1. Navigate to Virtual Machine in the VMware console.

![](data:image/png;base64...)

* 1. How to Access Production and test Citrix

1. Login below Production URL with snch.org credentials

<https://vportal.snch.org/Citrix/CTXWeb/>

![](data:image/png;base64...)

1. Login to below Test URL with snch.org credentials.

<https://vportal-test.snch.org/Citrix/CTXTESTWeb/>

![](data:image/png;base64...)

* 1. Access Xenapp6.5

1. Login to the jump server [10.100.27.127](https://urldefense.proofpoint.com/v2/url?u=http-3A__10.100.27.127&d=DwQGaQ&c=shNJtf5dKgNcPZ6Yh64b-ALLUrcfR-4CCQkZVKC8w3o&r=g2QgrkZ8s7K8U-Gp4SyICXBUu-pVs8JUJaeOs2pZrtM&m=n7luwfSNN0t7VAxwZW_NMCfqEDmDmFGhq5wVRtgBJJiXXXGTuixT9wp1WC5uX6Oy&s=-XB7zz9-Yg4jrXcJWY79Wl3DUEDi9UGB4KxRCklyXM0&e=):4389  runt the app center and uses the                                                    snchhome\flexpodadmin acct for access.
2. Search for the Citrix App center

![C:\Users\murugk01\AppData\Local\Microsoft\Windows\INetCache\Content.MSO\88B2F115.tmp](data:image/png;base64...)

Note :We will perform monthly maintenance only  for XenApp 6.5farm 2012 and 2016 VDA Servers.

Note: All security exception like no patching for XenApp 6.5farm, 2008VDA servers

1. Vendor Management

Citrix Vendor support can be availed in case of any requirement. Below are the details required to raise a Support Ticket with Citrix Support team.

| Category | Details |
| --- | --- |
| Cloud Portal URL | <https://us.cloud.com> |
| Organization ID | 52646614 |
| Citrix Cloud Customer Name | The Mount Sinai Health System |
| Citrix Cloud Customer ID | cr141y8yxhg3 |

To raise ticket with Citrix vendor, Click on side menu and click on Support tickets.

![](data:image/png;base64...)

A new webpage opens and we need to raise a new case or we can check the status of the old case.

Also, we can call on the Citrix support numbers.

USA -Toll Free: +1 800 424 8749

India –Toll Free:  1800 102 2489

Mobile: +91 80 4179 6650

1. Storage Management

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the link for Storage Runbook.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7B5EC98952-3DE6-48DC-8B2D-C83E46627732%7D&file=CMS_Storage_Operations_Runbook_v2.1.docx&action=default&mobileredirect=true) | | |

1. Software Management & Licensing

20.1 Citrix Licensing

Please refer Citrix Design Document Sec 12.4 for License information.

1. Profile Management

In MSHS Citrix environment Mandatory Profiles will be used for all EPIC users.

* As per application vendor roaming profiles are not required since all customized settings are stored within the Epic application framework.
* Folder redirection settings will be implemented via GPO for non-EPIC app users.

1. Vulnerability Management
   1. Vulnerability Management Process

\*\*We are yet to get information from Build team\*\*

* 1. Vulnerability Management Risk Rating

\*\*We are yet to get information from Build team\*\*

1. Disaster Recovery

Please refer to Section 8 of Citrix Design document for Disaster Recovery.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the link for Citrix Design document.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/r/sites/BusinessCaseValidation/_layouts/15/Doc.aspx?sourcedoc=%7B1C64C080-BE90-4648-B337-89AED145B6E3%7D&file=MSHS%20Citrix%20Design%20Document%20V4.docx&action=default&mobileredirect=true) | | |

1. SOP

**Please refer below link for the SOP:**

Daily Health Check-up click here

New Application add/delete click here

DR activities Fail over Fail back click here

SSL Certificate renewal click here

User session/profile reset click here

1. Monitoring
   1. Server Level monitoring

Server Level monitoring will be done by windows Team. Please refer to section 17 in Windows Runbook.

|  | **Important note** | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | Kindly refer the document for Server Level Monitoring.  [Click Here](https://mtsinai.sharepoint.com/%3Aw%3A/s/BusinessCaseValidation/Ee4jJcc1xxFFmexN4rpnz6sBnWtrjw_qmABFbGLl8PCcbw?e=M7Unqx) | | |

* 1. Citrix Services Monitoring

1. We will receive a mail alert in MSHS Email if any of the Citrix services goes down. Below is the sample email alert.

![](data:image/png;base64...)

1. After receiving the Alert, Navigate to Azure alert and check the Alert.

![](data:image/png;base64...)

1. Login into the server, Check the Service for which the alert has been generated in the server and resolve it.
2. Once the alert has been worked upon, login back to Azure alert.
3. ![](data:image/png;base64...)Click on Change alert state.
4. ![](data:image/png;base64...)After it Choose closed option from drop down menu to close the alert. Provide the steps done to remediate the alert in the comment section, then click on Save.

25.2 Citrix Cloud Health Monitoring

1. We Need to Monitor the Cloud Health Dashboard from Citrix and send communication to Broadcast / local communication based on the issue range to the infrastructure.
2. Open <https://status.cloud.com> from browser to access Citrix cloud health dashboard. If there is any outrage, we will be able to see the number of affected and down services.

![](data:image/png;base64...)

1. ![](data:image/png;base64...)We can see the current status and also if any planned activity is schedule.
2. We need to raise a Priority incident if no incident has been raised by any user.
3. We need to request SMOC Team to initiate a bridge Call.

25.3 Citrix DaaS Monitoring

1. Open Citrix DaaS Monitoring console in Citrix Cloud Portal.

![](data:image/png;base64...)

1. We can monitor the session failure, VDA Server failure and the Session count from the DaaS monitor console.

25.4 Server On boarding to My Wizard

Please find the document to on board the servers in My Wizard.

![](data:image/x-emf;base64...)

25.5 Server off boarding from My Wizard

Please find the document to on board the servers in My Wizard.

![](data:image/x-emf;base64...)

25.6 Blackout Server in My Wizard

Please find the document to Surplus the alerts from My Wizard.

![](data:image/x-emf;base64...)

25.7 Email Alerts coming to Citrix DL

Please find the below link for all the Email alerts configured on Citrix DL.

[Citrix Email alerts .xlsx](https://mtsinai.sharepoint.com/%3Ax%3A/r/sites/CloudOperations-CMS/Shared%20Documents/General/Citrix%20Email%20Alerts/Citrix%20Email%20alerts%20.xlsx?d=wa17d77513021444ca82ab45182db8293&csf=1&web=1&e=YalQ5F)

1. Contacts

26.1 CMS contacts

| Name | Role | Organization | Email |
| --- | --- | --- | --- |
| Prasant Gupta | Citrix Lead | CMS | prasant.gupta@accenture.com |
| Anand Kumar Sharma | Citrix Administrator | CMS | anand.c.kumar.sharma@accenture.com |
| Uma Yadav | Citrix Administrator | CMS | uma.brahmadev.yadav@accenture.com |
| Kousalya Murugesan | Citrix Administrator | CMS | kousalya.murugesan@accenture.com |
| Sravani Singadi | Citrix Administrator | CMS | sravani.singadi@accenture.com |
| Tanya Sharma | Citrix Administrator | CMS | tanya.l.sharma@accenture.com |
| Jubi John | Citrix Administrator | CMS | jubi.john@accenture.com |
| Singh, Gaurav | Citrix Administrator | CMS | Gaurav.Singh@accenture.com |
| Escalation Contact | | | | |
| KJ | Delivery Manager | Offshore | jayasankar.k.j@accenture.com | |
| Taha Rashidi | Delivery Manager | Onshore | Taha.rashidi@accenture.com | |
| Suprovat Sinha | Delivery Manager | Offshore | suprovat.sinha@accenture.com | |

26.2 Build contacts

| Name | Role | Organization | Email |
| --- | --- | --- | --- |
| Bharat Gulati | Build Team | CMS | bharat.gulati@accenture.com |
| Sandhya Verma | Build Team | CMS | sandhya.a.verma@accenture.com |
| Satyanarayana Muppidi | Build Team | CMS | s.muppidi@accenture.com |

26.3 Escalation Matrix Internal CMS

| Escalation Level | Name | Email |
| --- | --- | --- |
| L1 | Tower Leads | MSHS.CMS.TowerLeads@accenture.com |
| L2 | Taha  Suprovat | Taha.rashidi@accenture.com  suprovat.sinha@accenture.com |
| L3 | KJ  BG | jayasankar.k.j@accenture.com  bharathi.ganesh.ns@accenture.com |
| L4 | Shweta Gogna  Amit Gaur | shweta.gogna@accenture.com  amit.gaur@accenture.com |

 26.4 Escalation Client

| Escalation Level | Name | Email |
| --- | --- | --- |
| L1 | German Alvarez | German.Alvarez@mountsinai.org |
| L2 | Brittelli, Joseph | Joseph.Brittelli@mountsinai.org |

1. SCOM Alerting Procedure

If the CMS team receives an email alert that says “Error” or “Critical” they are to open a ticket in Service Now.

* As a matter of process, they will respond to the alert with “Received by *xyz* <ex - storage>, incident ticket *<INC123>*in service now has been created and assigned to group *xyz*.”
* These should be treated as P2s and tracked as such
* Please confirm receipt of this email and when it has been formally communicated as a process to the CMS teams

1. Citrix Daily Reboot Schedule SOP

#### **1. Procedure**

##### **1.1 Pre-Check (12:30 AM EST)**

**Maintenance Mode Setup**: At 12:30 AM EST, place the tagged servers scheduled for reboot that day into Maintenance Mode (MM) within Citrix DaaS.

**Verification**: Ensure all servers with the designated tag (e.g., "Maint-1-Monday") are in Maintenance Mode to prevent user logins during the reboot process.

##### **1.2 Reboot Monitoring (1:00 AM - 5:00 AM EST)**

**Automatic Reboot Monitoring**: From 1:00 AM to 5:00 AM EST, monitor the tagged servers as they undergo the scheduled automatic reboot.

**Manual Power-On (if needed)**: During this window, verify all tagged servers are powered on. If any server remains powered off after the scheduled reboot, manually power it on to ensure completion.

##### **1.3 Post-Check (5:00 AM - 5:30 AM EST)**

**Check Server Status**

**Server Status Verification**: Confirm that each server is back online, and all essential services are running as expected.

**Registration Verification**

**Citrix Studio Check**: Verify that all tagged servers have registered successfully in Citrix Studio by 5:30 AM EST.

**Maintenance Mode Removal**

**Exit Maintenance Mode**: At 5:30 AM EST, remove each server from Maintenance Mode within Citrix DaaS to make them available for user connections.

**Final Verification**

**Full Availability Confirmation**: Ensure that all tagged servers are no longer in Maintenance Mode and are fully operational and accessible to users.

**Peer Review (Two-Eye Process)**

**Request Review**: After completing the above steps, ask a peer team member to review the post-check actions.

**Peer Review Checklist**:

Confirm each server was removed from Maintenance Mode.

Ensure each server is registered in Citrix Studio and is available for user connections.

**Sign-Off**: The peer reviewer should document their initials and timestamp to confirm their review and sign-off on the checklist as part of the Daily task.

#### **2. Reboot Schedule**

Each day is assigned a specific tag to maintain an organized and efficient reboot process.

| **Day** | **Time** | **Tag** |
| --- | --- | --- |
| Monday | 1:00 AM - 5:00 AM EST | Maint-1-Monday |
| Tuesday | 1:00 AM - 5:00 AM EST | Maint-2-Tuesday |
| Wednesday | 1:00 AM - 5:00 AM EST | Maint-3-Wednesday |
| Thursday | 1:00 AM - 5:00 AM EST | Maint-4-Thursday |
| Friday | 1:00 AM - 5:00 AM EST | Maint-5-Friday |
| Saturday | 1:00 AM - 5:00 AM EST | Maint-6-Saturday |
| Sunday | 1:00 AM - 5:00 AM EST | Maint-7-Sunday |

#### **3. Tags**

The following tags correspond to the daily maintenance schedule for identifying which VDAs to reboot:

Maint-1-Monday

Maint-2-Tuesday

Maint-3-Wednesday

Maint-4-Thursday

Maint-5-Friday

Maint-6-Saturday

Maint-7-Sunday

### **4. Documentation**

For tracking and audit purposes, a weekly change with the following tasks should be logged each maintenance day, resulting in a total of 28 tasks per week (4 tasks per day) to cover all maintenance activities.

| Task | Description |
| --- | --- |
| **Task 1** | Place servers into Maintenance Mode based on the designated tag (e.g., "Maint-1-Monday"). |
| **Task 2** | Verify VDA registration status in Citrix Studio to ensure all VDAs tagged as "Maint-1-Monday" are registered. |
| **Task 3** | Remove servers from Maintenance Mode after reboot completion, making them available for user connections. |
| **Task 4** | Perform a peer review of post-check actions, verifying server status, registration, and availability. |

**Documentation Process**: Each task should be recorded in the ticketing system, noting:

Any issues encountered or manual interventions performed.

Peer review confirmation, including the reviewer’s initials and timestamp.

1. Decommission of Azure VDA`S

We will raise change and get in approved in CAB and perform the Decommission of Azure VDA`S

Reference change: [CHG0078552 | Change Request | ServiceNow (service-now.com)](https://mountsinaihealth.service-now.com/now/nav/ui/classic/params/target/change_request.do)

**Step-by-step instructions:**

Day 1

\*\*\*\*\*\*

* VDA should be put in Maintenance mode

![](data:image/png;base64...)

* Place VDA`s in Blackout window for 30 days.

![](data:image/png;base64...)

* Power off the VDA’s from the Citrix Console.

![](data:image/png;base64...)

Day 28

\*\*\*\*\*\*

* Off board the server from my wizard monitoring tool to avoid any INC created for these VDA.

![](data:image/png;base64...)

* Need to send mail to DNS team to perform the DNS Cleanup activity for Decommission servers.
* Login to the Citrix Cloud Portal and navigate to Machine catalog

![](data:image/png;base64...)

* Select the Machine catalog on which the servers are going to decom. Select all VDA`s and right click and select Delete.

![](data:image/png;base64...)

* Select the option which will delete all the VDA from Citrix, Azure and Active Directory.

![](data:image/png;base64...)

* Enter Domain credentials and click on done.

![](data:image/png;base64...)

* Cline on Next . On Summary page check the check box and click on delete.

![](data:image/png;base64...)

* Once VDA`s are deleted if Machine catalog is empty , we need to delete machine catalog .

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

* We will send mail to Service Management team to remove the VDA's from CMDB.

**Next steps:**

We need to validate whether VDA`S are deleted or not, Confirm whether CMBD, Mywizard and DNS all are done or not.

**Validation Process for Decommissioning request by App owner:**

Team need to elevate their approach when handling decommissioning requests. If the information is unclear, let’s seek clarification rather than making assumptions. Decommissioning is a critical process, and we must take ownership instead of merely executing requests without proper validation.

To prevent any errors, we are updating our process runbook to:

* ensure CIs in the decommissioning requests are clearly documented,
* engage the DB team for verification when database servers are involved
* Decommissioning requests be raised or approved by the respective server/DB owner

Let’s be extra cautious and ensure we have everything in black and white before proceeding with decommissioning.

