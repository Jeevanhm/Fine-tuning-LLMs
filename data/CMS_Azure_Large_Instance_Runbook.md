

**Document Control**

**AZURE LARGE INSTANCE Runbook**

| Version | Status | Date | Author | Summary of Change |
| --- | --- | --- | --- | --- |
| V1.1 | Initial Draft | 13July 2023 | Hema Koul | Initial Draft |
|  |  |  |  |  |

Document Approval

| Date | Version | Approver | Comments |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

Document Reviews

| Date | Company | Reviewer | Notes |
| --- | --- | --- | --- |
| 14-July-23 | Accenture | Mangesh Rane | Initial review completed |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

[1 Introduction 4](#_Toc140266368)

[2 About Client 5](#_Toc140266369)

[3 About Accenture 6](#_Toc140266370)

[4 Access 7](#_Toc140266371)

[4.1 Citrix VDI 7](#_Toc140266372)

[4.2 Azure Portal 7](#_Toc140266373)

[4.3 ServiceNow & CMS Distribution List 7](#_Toc140266374)

[5 Environment Details 8](#_Toc140266375)

[5.1 Environment Types 8](#_Toc140266376)

[5.2 Azure Regions 8](#_Toc140266377)

[6 Operation and Governance 9](#_Toc140266378)

[6.1 ITSM Function 9](#_Toc140266379)

[6.2 Governance 9](#_Toc140266380)

[7 Cloud Foundation-BMI 10](#_Toc140266381)

[7.1 What does BMI Include 10](#_Toc140266382)

[7.2 Cloud share responsibility Model 10](#_Toc140266383)

[8 BMI Overview 12](#_Toc140266384)

[8.1 BMI H/W and OS requirement SUMMARY 12](#_Toc140266385)

[8.2 BMI Agent requirements 13](#_Toc140266386)

[8.3 BMI / ALI Servers Network Connectivity 14](#_Toc140266387)

[8.4 Network Manager Service in BMI 15](#_Toc140266388)

[8.5 BMI Monitoring 17](#_Toc140266389)

[8.6 ALI/BMI Inventory 18](#_Toc140266390)

[9 Vendor Support 19](#_Toc140266391)

[10 Contacts 21](#_Toc140266392)

[10.1 CMS Contacts 21](#_Toc140266393)

[10.2 Build and Migration Contacts 21](#_Toc140266394)

[10.3 Escalation Matrix Internal Accenture 21](#_Toc140266395)

[10.4 Escalation (Mount Sinai) 21](#_Toc140266396)

Ok

1. Introduction

This document will act as a handbook which consists of all the technical procedures and processes that are required to support the Mount Sinai Azure Cloud Infrastructure. Accenture Azure team will leverage this document for all the processes, tools, procedures, and resources to perform day-to-day operations within the IT Infrastructure and provide world-class service to the business and end-users.

When an incident or problem occurs in the environment, an operations organization relies on its Standard Operating Procedures (SOP’s) or troubleshooting guidelines to resolve the problem. A proactive approach to documentation is needed to support Azure Infrastructure operations within an organization.

This Run Book will serve to define both daily operations tasks to support the infrastructure deployed for Mount Sinai recommended troubleshooting tasks to revolve issues which may be encountered. The Run Book also identifies task owners for specific operations tasks and estimated effort.

Any updates in the document should be reviewed & approved.

1. About Client

Founded in 1852, The Mount Sinai Hospital is a 1,134-bed, tertiary-care teaching facility acclaimed internationally for excellence in clinical care.

In the U.S. News & World Report 2021-22 "Best Hospitals" rankings, Mount Sinai Hospital is designated with highest recognition and our institution is nationally ranked in 11 specialties including Geriatrics, Cardiology/Heart Surgery, Diabetes/Endocrinology, Neurology/Neurosurgery, Orthopedics, Gastroenterology & GI Surgery, Rehabilitation, Urology, Pulmonology & Lung Surgery, Ear, Nose and Throat, and Cancer. Our pediatric center, Mount Sinai Kravis Children’s Hospital is also recognized on U.S. News & World Report's 2021-22 Best Children's Hospitals rankings.

Mount Sinai Health System is New York City's largest academic medical system, encompassing eight hospitals, a leading medical school, and a network of ambulatory practices. Mount Sinai is an international source of unrivalled education, translational research and discovery, and clinical delivery outcomes.

Mount Sinai is among the top research and clinical institutions providing response to COVID-19, leveraging numerous artificial intelligence algorithms and machine learning models developed in-house.  The current pandemic has accelerated the need and urgency for speed and innovation, including rapid access to data and collaboration. However, Mount Sinai is constrained by a legacy technology environment that is costly to maintain, and in some instances, with components beyond end of life. The culmination of technical debt has created an environment that is costly to maintain and prohibitive to research advancement and clinical outcomes.

Given the demands placed on the clinical and research teams; there exists an enterprise imperative to enable a landscape of technology services that are up to date, always available, inexpensive to implement / maintain, and readily available on a self-service basis.

1. About Accenture

Accenture is a global management consulting, technology services and outsourcing company. Combining unparalleled experience, comprehensive capabilities across all industries and business functions, and extensive research on the world's most successful companies, Accenture collaborates with Mount Sinai to help them become high-performance businesses and governments.

1. Access

4.1 Citrix VDI

First level of the access to Mount Sinai is via **Citrix VDI** using msnyuhealth.org domain and VIP Symantec MFA.

Link to access the Citrix VDI URL: <https://mountsinai.cloud.com/Citrix/StoreWeb/#/home>

4.2 Azure Portal

Post the access to Citrix VDI, **Azure portal** access is made using privilege account (PA) as per the Mount Sinai access guideline. No access to MSHS will be allowed through non-PA account.

CMS Cloud Foundation access to the **Azure Portal** is provided through the Active Directory **MSH-Cloud Foundation-ACN** group membership on the PA account.

4.3 ServiceNow & CMS Distribution List

In addition, CMS Support will hold the following ServiceNow Assignment & Team Distribution group for the day-to-day operation activity:

* ServiceNow Assignment group: **MSHS-Cloud Foundation**
* CMS Support team Distributions: **CMS-Cloudfoundation@mountsinai.org** & **Mt.Sinai.CMS.Azure@accenture.com**

1. Environment Details

5.1 Environment Types

Mount Sinai Azure Landscape is expanded under following environment type:

* **Production**
* **Dev**
* **Test**
* **Shared**
* ***Sandbox (temp)***

5.2 Azure Regions

Azure provides service across multiple geographic regions, each supported by multiple datacenters and availability zones. In some cases, these regions represent a resource boundary – for example, Certain Azure services, VM sizes are only available in certain regions.

|  | Architecture Decision | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ☼ | Due to the availability of virtual machines, as well as other required services, the MSHS services for the Cloud Migration project will be provisioned in the following regions:   * + Primary Region “**East US**”.   + Secondary Region “**South Central US**” for DR. | | |

1. Operation and Governance

6.1 ITSM Function

CMS Operation support is following the ServiceNow tool covering for applicable ITSM functions as part of the day-to-day deliverable to Mount Sinai.

**Applicable ITSM Process:**

* Incident Management
* Change Management
* Problem Management
* Service Request Management
* Configuration Management
* Service Introduction (ORC)

ServiceNow Link: [click here](https://mountsinaihealth.service-now.com/)

|  | Important Documents | | |
| --- | --- | --- | --- |
|  |  |  |  |
| ! | For detailed ITSM workflow, kindly refer to ITSM process runbook mentioned in the Document Call outs. [Click Here](https://mtsinai.sharepoint.com/sites/BusinessCaseValidation/Shared%20Documents/Forms/AllItems.aspx?cid=abc6debd%2D53b2%2D4c63%2Da3f9%2D93ee4f2b623e&FolderCTID=0x0120000AD53B2894B0AA48AF2E0F98676FB541&id=%2Fsites%2FBusinessCaseValidation%2FShared%20Documents%2FGeneral%2FService%20Management&viewid=458ee074%2D644d%2D49f9%2Da0cc%2D2b2b80271076&OR=Teams%2DHL&CT=1652801831473&params=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjA0MDExMTQxMyJ9)  MIM Document  Configuration Management Process  Change Management Process | | |

* 1. Governance

CMS Operation governance model cover the daily, weekly, monthly cadence on the service performance

* **Daily Meeting:** Daily service dashboard review with MSHS CMS Leadership on applicable ITSM Functions (Duration: 10 Minutes)
* **Weekly Meeting**: Weekly Service Delivery Review with MSHS CMS Leadership on overall service performance for the previous week (Every Wednesday @ 9:30 AM EST)
* **Monthly Meeting**: *(To be established)*

1. Cloud Foundation-BMI

Azure Cloud Foundation for Mt Sinai includes BareMetal as a Service (BMaaS). In Azure, BMaaS is referred to as BareMetal Infrastructure (BMI) and more recently Azure Large Instances (ALI).

BMI provides the compute, storage and network infrastructure to support non-virtualized, dedicated BareMetal servers which are used for critical workloads that require:

* High performance compute and storage
* Very low latency (<1ms)

With BareMetal servers, full root access to the operating system (OS) is provided. The OS installation (RHEL 8.X) are managed according to client needs by Microsoft BMI team.

* 1. What does BMI Include

BareMetal Infrastructure (BMI) is made up of dedicated BareMetal servers. It features:

* High-performance compute with a range of choices: 2-socket to 24-socket servers and memory ranging from 1.5 TBs up to 24 TBs.
* High-performance storage appropriate to the application (Fiber Channel)
* Storage can also be shared across BareMetal instances to enable features like scale-out clusters or high availability pairs with failed-node-fencing capability.
* Virtual LANs (VLANs) in an isolated environment that are securely accessible to VMs on one or more Virtual Networks (VNets) in your Azure subscription
* The entire BMI environment is represented as a resource group within an Azure subscription.

7.2 Cloud share responsibility Model

**Responsibilities often vary by IaaS vs PaaS vs SaaS and now BMaaS**

Standard Shared Responsibility Model

![Diagram of BareMetal Infrastructure support model.](data:image/png;base64...)

**Azure Large Instance (ALI) responsibility Model**

![Graphical user interface, application

Description automatically generated](data:image/x-emf;base64...)

1. BMI Overview

BareMetal Infrastructure (BMI):

* Each region has one cluster with two node pairs (active, passive) for hosting Epic ODB with required monitoring & security agents
* Per node pair – 16 data LUNs including 2 Journal LUNs
* Per node pair - 97 TB of usable storage. Currently, ODB is approximately 55 TB.
* Includes NetApp 800 H/A Pair
* ExpressRoute (100 Gbps) and Global Reach connectivity
* Tags are applied to the BMI instance only (not at component level)
* ![A computer screen shot of a diagram

  Description automatically generated](data:image/png;base64...)

8.1 BMI H/W and OS requirement SUMMARY

**Hardware**:

* BMI Server Cluster consisting of 2x 8 socket 2 nodes with 12TB memory
* High performance storage (16 Data LUNs with 97 TB of usable storage) that is shared between BMI servers to enable high availability pairs
* 1x HA NetApp 800 with self-encrypting drives
* 1x HA NetApp Cloud Volume On-tap (CVO) enable backup, cloning and restore of server snapshots
* BMI Tagging (constraint for BMI Instance Level only)

Network & Connectivity:

* Virtual LAN (VLAN) per region that are securely accessible to VMs on one or more Vnets
* Connectivity to Azure and On-premise via ExpressRoute (100 Gbps) and Global Reach

Operating System:

* O/S – RHEL 8.X including H/A Add-On (Pacemaker)
* Monitoring and Security Agents
* Satellite is used for updates, patching and security fixes

Microsoft support:

* Snapshot restores performed by MSFT as required
* Automated BMI O/S Backups performed by MSFT
* Firmware updates performed by MSFT

![A computer screen shot of a diagram

Description automatically generated](data:image/png;base64...)

8.2 BMI Agent requirements

MSFT Agents:

* Azure Defender for Cloud
* Microsoft Defender for Endpoint (MDE)
* Defender Log Analytics agent
* Azure Qualys
* Azure Linux monitoring agent
* Azure Monitor Agent (Arc Agent)
* Azure Update Mgmt (Does not apply)

Security / OS Agents:

* Tenable – vulnerability scanning
* CrowdStrike – endpoint protection
* NXLog – log aggregation
* SAR (Linux only) – system activity
* Splunk Universal Forwarder – My Wizard
* monitoring
* RHEL SSSD (Linux only) – AD integration

8.3 BMI / ALI Servers Network Connectivity

**![A diagram of a network

Description automatically generated](data:image/png;base64...)**

**For configuring the Network rules in network manager we should see below sheet for reference.**

| **FROM** | **TO** | **CONNECTIVITY** | **RULES** |
| --- | --- | --- | --- |
| ALI Servers | Servers in Azure (Including EPIC application servers) | Express Route à Network Manager rules | Network Manager rules (EastUS –Inbound-BMI-rule; USSC-Inbound-BMI-rule) |
| Servers in Azure (Including EPIC application servers) | ALI Servers | Express Route à Network Manager rules | Network Manager rules (EastUS –Outbound-BMI-rule; USSC-Outbound-BMI-rule) |
| Cross-region connectivity between ALI servers to Azure servers | Cross-region connectivity between ALI servers to Azure servers | Express Route à Network Manager rules | Network Manager rules (Crossregion –Outbound-BMI-rule; Crossregion-Inbound-BMI-rule) |
| EUS ALI Servers | EUS WebProxy server | Express Route à Network Manager rules | Network Manager rules (EastUS –Inbound-WebProxy-BMI-rule) |
| EUS WebProxy server | EUS ALI Servers | Express Route à Network Manager rules | Network Manager rules (EastUS –Outbound-WebProxy-BMI-rule) |
| USSC ALI Servers | USSC WebProxy server | Express Route à Network Manager rules | Network Manager rules (USSC –Inbound-WebProxy-BMI-rule) |
| USSC WebProxy server | USSC ALI Servers | Express Route à Network Manager rules | Network Manager rules (USSC –Outbound-WebProxy-BMI-rule) |
| ALI Server (EUS & USSC) | On-prem CoLo Servers | Global Reach |  |
| EUS ALI Server | USSC ALI Server | Global Reach |  |
| USSC ALI Server | EUS ALI Server | Global Reach |  |
| ALI Server | Public Network | Express Routeà WebProxyà PA Firewall | Network Manager rules (EastUS –Inbound-WebProxy-BMI-rule) |
| Exclusion list in WebProxy |
| Allowed in Firewall |

* 1. Network Manager Service in BMI

**Azure Virtual Network Manager** is a management service that enables you to group, configure, deploy, and manage virtual networks globally across subscriptions. With Virtual Network Manager, you can define network groups to identify and logically segment your virtual networks.

Below is the network manager configured in azure for BMI in Mountsinai tenant.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

Below are the set of rules configured in network manager for application workflow.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

These are the detailed listed dynamic groups for the entire BMI network on subscription level.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

Attached are the set of rules of Network manager and the Epic applications that are associated w/ each of the Epic related subnets

![](data:image/x-emf;base64...)

Attached are the NSGs cover the various standard connectivity points within the Epic application (between PROD, Training, and non-prods).

![](data:image/x-emf;base64...)

* 1. BMI Monitoring

We have created below rule in azure alerts in Monitor service in Azure which are sending all alerts to the targeted groups in Mount Sinai Outlook. Further we have integrated these alerts in SNOW to generate incidents out of it.

![](data:image/png;base64...)

* 1. ALI/BMI Inventory

Below is the list of Linux Servers belonging to EPIC that includes 2 pair of BMI Servers.

| **Environment Classification** | **Purpose** | **Hostname** | **IP** |
| --- | --- | --- | --- |
| **Production** | **Production ODB Server (BMI)** | **zeuspldbprd01** | **10.109.254.31** |
| **Production** | **Production ODB Server (BMI)** | **zeuspldbprd02** | **10.109.254.32** |
| **DR** | **DR ODB Server (BMI)** | **zusscpldbprd01** | **10.109.255.31** |
| **DR** | **DR ODB Server (BMI)** | **zusscpldbprd02** | **10.109.255.32** |

1. Vendor Support

**Creating a support request in Azure: ALI(Epic On Azure)**

[Reference Link](https://mtsinai.sharepoint.com/%3Ab%3A/r/sites/CloudOperations-CMS/Shared%20Documents/General/Microsoft%20Documentation/ALI%20support%20How%20to%20guide.pdf?csf=1&web=1&e=WW8zLr)

Notes to Remember:

All in the event of a SEV - 1 where we need immediate response from the Microsoft executive team this is the number to contact. This number should not just be used to skip the line on SEV 1's, when we have an Epic down situation, we can use it along with our case number in parallel. The two events that would qualify for reaching out to this number would be the last 2 mass Epic outages.

Mt Sinai Azure Escalations MtSinaiAzEsc@microsoft.com

Jeremy Hollett jeremyh@microsoft.com 425-614-5910 (text please)

1. Contacts

10.1 CMS Contacts

| Name | Role | Organization | Email |
| --- | --- | --- | --- |
| Hema Koul | Azure Lead | Accenture | hema.koul@accenture.com |
| CMS Cloud Foundation | Support DL | Accenture | Mt.Sinai.CMS.Azure@accenture.com  CMS-Cloudfoundation@mountsinai.org | |

10.2 Build and Migration Contacts

| Name | Role | Email |
| --- | --- | --- |
| Indhumathi Chellaswamy | Technical Architecture manager | i.a.chellaswamy@accenture.com |
| Tom McFadden | Azure Architect | thomas.mcfadden@accenture.com |
| Zach C Nemith | Azure Architect | zach.c.nemitz@accenture.com |

10.3 Escalation Matrix Internal Accenture

| Escalation Level | Name | Email |
| --- | --- | --- |
| L1 | CMS Cloud Foundation DL | MSHS.CMS.TowerLeads@accenture.com |
| L2 | Suprovat Sinha (Offshore)  Taha Rashid (Onshore) | suprovat.sinha@accenture.com  taha.rashidi@accenture.com |
| L3 | Jayasankar KJ (Offshore)  Bharathi Ganesh NS (Onshore) | jayasankar.k.j@accenture.com bharathi.ganesh.ns@accenture.com |
| L4 | Shweta Gogna (Offshore)  Gaur, Amit (Onshore) | shweta.gogna@accenture.com  amit.gaur@accenture.com |

10.4 Escalation (Mount Sinai)

| Escalation Level | Name | Email |
| --- | --- | --- |

