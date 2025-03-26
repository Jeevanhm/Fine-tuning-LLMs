

![Logo, company name

Description automatically generated](data:image/jpeg;base64...)

**EXACS Run Book – Version 1.1**

**DATE: 09/30/2024**

Content

[1. Purpose 6](#_Toc109075426)

[2. Scope 6](#_Toc109075427)

[2.1 System overview 7](#_Toc109075428)

[2.2 In-Scope Services 7](#_Toc109075429)

[2.3 Out-Scope Services 7](#_Toc109075430)

[2.4 Support Hours and Language 7](#_Toc109075431)

[2.5 Access Required for SQL DBAs 7](#_Toc109075432)

[2.6 General Account (ID to access client network) 7](#_Toc109075433)

[2.7 SharePoint access 8](#_Toc109075434)

[2.8 Ticketing Tools Access 8](#_Toc109075435)

[2.9 VPN/ZScaler Access 8](#_Toc109075436)

[2.10 SQL Server Environment 8](#_Toc109075437)

[2.11 Inventory 8](#_Toc109075438)

[2.12 Authorization/Authentication 8](#_Toc109075439)

[2.13 Logins/Security 8](#_Toc109075440)

[2.14 Password management 9](#_Toc109075441)

[2.15 Backups and Restoration 9](#_Toc109075442)

[2.16 RTO/RPO 9](#_Toc109075443)

[2.17 STORAGE 9](#_Toc109075444)

[2.18 Monitoring Process 10](#_Toc109075445)

[2.19 Reboot/Restart Process 10](#_Toc109075446)

[2.20 Service Level Agreement 10](#_Toc109075447)

[2.21 Ticketing Tools 11](#_Toc109075448)

[2.22 Change management Overview 11](#_Toc109075449)

[2.23 Incident management Overview 11](#_Toc109075450)

[2.24 Problem management Overview 11](#_Toc109075451)

[2.25 Audits 11](#_Toc109075452)

[2.26 High Availability 12](#_Toc109075453)

[2.27 SSIS/SSRS/SSAS 12](#_Toc109075454)

[2.28 Patch Implementation 12](#_Toc109075455)

[2.29 DB Maintenance 13](#_Toc109075456)

[2.30 DISASTER RECOVERY 13](#_Toc109075457)

[2.31 Daily Tasks 13](#_Toc109075458)

[2.32 Monthly\Weekly 14](#_Toc109075459)

[2.33 Common or Known Issues 15](#_Toc109075460)

[2.34 Management Tools 15](#_Toc109075461)

[2.35 SOPS: 15](#_Toc109075462)

**2.40.1 Process to follow prior Upgrading CPU Cores............................................................... 22**

2.45 Process for Firewall Change ….......................................................................................24

2.5 Adding security updates on servers for Visual studio ....................................................25

2.6 Steps to retrieve DB count.............................................................................................28

Tables: Document Control

Table 1: Revision History 4

| **Version** | **Author** | **Changes** |
| --- | --- | --- |
| **0.1** |  |  |
| **0.5** |  |  |
| **1.0** |  |  |

Table 1: Revision History

Table 2: Document review and feedback 4

| **Version** | **Reviewer** | **Feedback** |
| --- | --- | --- |
| **0.1** |  |  |
| **0.5** |  |  |
| **1.0** |  |  |

Table 2: Document review and feedback

Table 3: Document accseptence and document location 4

| **Version** | **Acceptance** | **Document location** |
| --- | --- | --- |
| **0.1** |  |  |
| **0.5** |  |  |
| **1.0** |  |  |

Table 3: Document accseptence and document location

About Accenture

Our values shape the culture of our organization and define the character of our company. We live the core values through individual behaviors. They serve as the foundation for how we act and make decisions.

About <<Client Name>>

Client Sites Location and Address

# Purpose

The purpose of the SQL Server Run Booksis to provide the basic operations procedures for managing the database infrastructure.

The Accenture database group will leverage a collection of processes, tools, procedures and resources to perform day-to-day operations within the IT Infrastructure and provide world-class service to the business and end-users.  When an incident or problem occurs in the environment, an operations organization relies on its Standard Operating Procedures (SOP’s) or troubleshooting guidelines to resolve the problem.  A proactive approach to documentation is needed to support an operations organization.

This Run Book will serve to define both daily operations tasks to support the infrastructure deployed for the project and recommended troubleshooting tasks to revolve issues which may be encountered.  The Run Book also identifies task owners for specific operations tasks and estimated effort.

# Scope

This Run Book covers basic operating guidelines and procedures necessary for operating the SQL Server infrastructure.

The scope of this document and work package is to:

* Define, organize, describe and recommend proactive operational best practices and tasks for:
  + One-time actions
  + Daily operations
  + Weekly operations
  + Monthly operations
  + Quarterly operations
  + Other operations
* Document the above tasks into a consolidated Run Book
* Define lessons learned and critical knowledge transfer regarding the infrastructure environment
* Define the Roles and Responsibilities needed to complete Proactive Operations Tasks
* Define the estimated resource(s) to complete each task
* Document the appropriate escalation path
* Provide guidance on troubleshooting methodology and commonly known issue

## System overview

The SQL Server system is designed to provide a flexible, high-availability, and scalable data management solution that supports diverse deployment environments, including Azure Virtual Machines (VMs), on-premises servers, Always on Availability Groups (AG), Failover Cluster Instances (FCI), and standalone instances. This system enables efficient data storage, retrieval, and processing to support.

### Architecture

The SQL Server architecture is structured to accommodate multiple deployment models, ensuring optimal performance, reliability, and disaster recovery. Key components include:

* **Deployment Environments**:
  + **Azure Virtual Machines**: Hosted SQL Server instances in the Azure cloud, leveraging the scalability and flexibility of cloud infrastructure.
  + **On-Premises Servers**: Traditional SQL Server deployments within local data centers, ensuring control and compliance for sensitive data.
  + **Always On Availability Groups (AG)**: High availability and disaster recovery solution that allows multiple copies of a database to be hosted on different servers, ensuring minimal downtime and data redundancy.
  + **Failover Cluster Instances (FCI)**: Provides high availability by grouping multiple servers into a cluster, allowing for automatic failover in the event of server failure.
  + **Standalone Instances**: Independent SQL Server installations for less critical workloads or development environments.

### Key Components

Our infrastructure spans three distinct domains:

1. **MSH Domain** (msnyuhealth.org, mountsinai.org)
   * Total SQL Instances: **271**
     + Standalone Servers: **174**
     + AG Cluster Nodes: **15**
     + FCI Clusters: **82**
2. **MSSM Domain** (mssn.edu)
   * Total SQL Instances: **6**
     + Standalone Servers: **4**
     + FCI Clusters: **2**
3. **MSSN Domain** (snch-home.org)
   * Total SQL Instances: **102**
     + Standalone Servers: **91**
     + AG Cluster Nodes: **11**

## In-Scope Services

* SQL Server (All SQL versions except Express)
* Other cloud scope services (Azure)

## Out-Scope Services

* License management
* Network Management
* Antivirus Management
* OS Administration
* SSRS/SSIS (SSISDB and Report Server databases are not in scope)
* SQL Server system databases (Master, Model, MSDB, TempDB, Distribution)

## Support Hours and Language

* 24\*7 hours support by CMS Team and English Language

## Access Required for SQL DBAs

* Sysadmin access is required for all DBAs to perform day to day activities.
* Access to Microsoft Teams
* Access to Mount Sinai SharePoint and Teams channel –

[Cloud Operations - CMS | General | Microsoft Teams](https://teams.microsoft.com/l/team/19%3A2Rt_JGP6GqXIUw6iHadGn9TyGPsb09hfa--7E-xUPfg1%40thread.tacv2/conversations?groupId=1ee9d581-43c7-40ef-bec8-3637e34fc184&tenantId=77e89d61-570f-43b0-b9e4-634f462e34b8)

[MSSQL DBA Team | General | Microsoft Teams](https://teams.microsoft.com/l/team/19%3AJXrYDlOO8fzTgJoedZZTIKR0xTvl55aaz0p3sagw5Us1%40thread.tacv2/conversations?groupId=7c9955e1-bde8-421f-befe-0e1f7b980241&tenantId=77e89d61-570f-43b0-b9e4-634f462e34b8)

* Access to BeyondTrsut Password safe –

[https://passwordsafe.mountsinai.org/WebConsole/#!/dashboard](https://passwordsafe.mountsinai.org/WebConsole/%23%21/dashboard)

## General Account (ID to access client network)

* Every resource need Hospital AD PA and Hospital AD.
* PA account password will be managed by Beyond Trust Password safe.

## SharePoint access

* All DBAs should have access to SOPs, KBs, JOBAID’s, Runbook and reports.
* Below are the 2 SharePoint locations where all related documents are placed:

1. [https://mtsinai.sharepoint.com/:f:/r/sites/CloudOperations-CMS/Shared%20Documents/General?csf=1&web=1&e=zmVaBo](https://mtsinai.sharepoint.com/%3Af%3A/r/sites/CloudOperations-CMS/Shared%20Documents/General?csf=1&web=1&e=zmVaBo)
2. [https://mtsinai.sharepoint.com/:f:/r/sites/MSSQLDBATeam/Shared%20Documents/General?csf=1&web=1&e=J1BvQW](https://mtsinai.sharepoint.com/%3Af%3A/r/sites/MSSQLDBATeam/Shared%20Documents/General?csf=1&web=1&e=J1BvQW)

## Ticketing Tools Access

* All DBAs should have access to the Service Now ticketing tool.
* Below is the link to Service Now:

[https://mountsinaihealth.service-now.com/now/nav/ui/classic/params/target/incident\_list.do%3Fsysparm\_view%3D%26sysparm\_userpref.incident\_list.view%3D%26sysparm\_userpref.incident.view%3D%26sysparm\_query%3Dassignment\_group%253De9eac9e94f272a004a6a5efd0210c780%255Eactive%253Dtrue%255EstateIN1%252C2%252C3%26sysparm\_fixed\_query%3D](https://mountsinaihealth.service-now.com/now/nav/ui/classic/params/target/incident_list.do)

## VPN/Zscaler Access

* There is no VPN/Zscaler setup in Mount Sinai environment.

## SQL Server Environment

* Data centers information/Cloud infrastructure information
* Production/Stage/QA/Dev
* DR solutions

## Inventory

### Centralized Management Server Overview

**Server Name:** ZEUSPWAPMON001
**Database:** PMON
**Table:** dbo.Msinaiservers

This centralized management server is designed to store and manage comprehensive inventory details of our SQL Server instances. The dbo.Msinaiservers table captures the following key fields:

* **FQDN:** Fully Qualified Domain Name
* **Instance Name:** Name of the SQL Server instance
* **Port Number:** Port on which the instance is accessible
* **Environment:** Deployment type (Prod/Test/Dev/QA/DR)
* **Cluster Type:** Configuration type (Standalone/2-node/3-node)
* **OS Version:** Operating system version
* **IP Address:** Server IP address
* **SQL Version:** Version of SQL Server
* **Edition:** SQL Server edition (e.g., Standard, Enterprise)
* **Location:** Deployment location (Azure/On-prem)
* **Domain:** Domain classification (MSHS/MSSM/MSSN)
* **Platform Type:** Architecture type (x64)
* **Application Name:** Associated application name
* **Application Owner:** Owner of the application
* **Application Contact:** Contact information for the application owner
* **CU Level:** Cumulative Update level
* **SP Level:** Service Pack level

This centralized repository allows for efficient tracking and management of SQL Server instances across environments, enhancing visibility and operational efficiency.

![](data:image/png;base64...)

## Authorization/Authentication

In SQL Server, authorization and authentication are critical components for securing data and ensuring that users have the appropriate permissions to access resources. This section outlines the strategies employed in our SQL Server environment.

### 1. Authentication Modes

SQL Server supports two primary authentication modes:

* **Windows Authentication:**
  + Utilizes Active Directory credentials.
  + Provides a seamless sign-in experience for users within the domain.
  + It offers robust security, as password management is handled by Active Directory.
* **SQL Server Authentication:**
  + Allows for SQL Server-specific usernames and passwords.
  + Suitable for applications that do not operate in a Windows environment.
  + Requires additional security measures, such as password policies, to ensure strong credentials.

### 2. User Roles and Permissions

To manage access effectively, SQL Server uses a role-based security model:

* **Server Roles: In our environment we provide server roles on a temporary basis for a maximum duration of 30 days after the requester raises an access request.**
  + Temporary server roles (e.g., sysadmin, dB creator, securityadmin) grant specific administrative capabilities at the server level.
* **Database Roles:**
  + Fixed database roles (e.g., db\_owner, db\_datareader, db\_datawriter) provide permissions within a specific database context.
  + Custom database roles can be defined for granular access control.

### 3. Granting and Revoking Permissions

* **Granting Permissions:**
  + The user has to raise Access request using the SQL Access form and if the request is related to server role, then the access is temporary, and the request must be approved by MSHS Leads JoeB/Rachel/Jeevan before granting access.
  + If the request is for database role, we can grant access and close the request.
* **Revoking Permissions:**
  + All server roles will be revoked based on the revocation data entered by the requester on the access form and then the request can be closed.
* **Least Privilege Principle:**
  Always grant users the minimum permissions necessary for their roles to reduce the risk of unauthorized access.
* **Strong Password Policies:**
  Enforce strong password policies for SQL Server Authentication to enhance security.

## Logins/Security

* **The SQL Access Request Form is utilized to manage all access-related tasks. Access the form via the following link:**

[SQL Server Access Request](https://mountsinaihealth.service-now.com/mshsportal?id=sc_cat_item&sys_id=1b5ba22e1b5a8e50e5ba6461604bcb79)

* **The form differentiates two levels of access: Database level and Instance level.**
* **Approval for Instance level access must be obtained from Joe B, Rachel, or Jeevan before any access is granted.**
* **Database level access may be granted on a permanent basis, whereas Instance level access is temporary and can be authorized for a maximum duration of 30 days.**
* **The SQL Access Request Form is configured to automatically generate a new revocation task 24 hours before the scheduled access revocation date.**

## Password management

* Individual SQL logins
* Application SQL logins
* Windows logins
* SA accounts
* Service accounts
* Shared service accounts
* All these passwords are stored securely in Password Safe

## Backups and Restoration

Database backup and restore strategies and techniques

* Full back up
* Differential backup
* Log backup
* Tape backup
* Native backups or Third-party tools

**Backup process defined as per the discussion with Onshore Team:**

**On-Prem backup procedures: -**

* We take weekly full, diff and T-log backups in the production/non-production environment based on the direction from the application team
* Backups go locally in the allocated disk drive; the retention period is 1 to 3 days based on the app owner's directions.
* Backups are happening locally on all the servers, once the backup is completed the files are copied by the net-backup team that is scheduled in a way that it runs after 12 AM EST (It is setup in such a way that it doesn’t coincide with the local backup i.e. from 7 PM EST – 9PM EST and it is stored with them for 31 days. i.e., Backing up to tape backups Veritas NetBackup (Offload to the Tape backups)
* Backup strategy defined is different server by server.
* We are using ola-hallengreen backup solution and native database maintenance plans to take the backup of the databases.
* For the test server, usually, it won’t go to NetBackup. We will ask the NetBackup team to take the NetBackup and keep 31 days (about 1 month) if and only if it is required.

**Azure backup procedures: -**

* We take weekly full, diff and T-log backups in the production/non-production environment based on the direction from the application team
* Backups go locally in the allocated disk drive; the retention period is 1 to 3 days based on the app owner's directions.
* Backups are happening locally on all the servers, once the backup is completed the files are copied by the net-backup team that is scheduled in a way that it runs after 12 AM EST (It is setup in such a way that it doesn’t coincide with the local backup i.e. from 7 PM EST – 9PM EST and it is stored with them for 31 days. i.e., Backing up to tape backups Veritas NetBackup (Offload to the Tape backups)
* Backup strategy defined is different server by server.
* We are using ola-hallengreen backup solution and native database maintenance plans to take the backup of the databases.
* For the test server, usually, it won’t go to NetBackup. We will ask the NetBackup team to take the NetBackup and keep 31 days (about 1 month) if and only if it is required.
* Please note there is no plan to implement the Azure SQL VM Backups at the moment. Eventually, all the backups will be moving from SAN storage to BLOB storage taking into consideration the SQL VM Backup solution.

**Point in time recovery:**

We will put the request with the net backup team to place the required backup files locally.

We will make sure to utilize these backup files to ensure point in time recovery of these databases.

**Steps for file\drive level restore in On-prem and Azure environment.**

Based on the request from App owner\Requester the first step is to create a request with Backup team to provide the requested file\data.

1. We can create a general request using the link below and assign the task to <MSHS-Backup> assignment group.

Link: [Create a general request](https://mountsinaihealth.service-now.com/now/nav/ui/classic/params/target/com.glideapp.servicecatalog_cat_item_view.do)

1. Connect with the person who is working on the task and ask them to provide the required file\folder from the desired date. The team will work on file level restore and copy the data to our requested location.

The retention period for an on-prem environment is 30 days.

1. To follow up with them through email, below is the DL Detail for backup team-

# CMS-Backup CMS-Backup@mountsinai.org

**Retention Policy in Azure:**

**Retention of daily backup point:**

Retain backup taken every day at 11:00 PM for 60 Day's

**Retention of weekly backup point:**

Retain backup taken every week on Sunday, Wednesday, Friday, and Saturday at 11:00 PM for 8 Weeks

**Retention of yearly backup point:**

Retain backup taken every year in January on Last Sunday at 11:00 PM for 7 Year(s)

**Netback Failure issues:**

 The NetBackup team takes the backup drive and puts it in the tape and if there are any issues with NetBackup then the backup wouldn’t be taken for the given day and time, and they wouldn’t be notifying us about the same, but we can reach out to - Jeffrey.foglietta@mountsinai.org to know the status of the backup.

DL for backup team: nbusupport@mountsinai.org

Snow assignment group: MSHS-BACKUP

 For instance, if the local backup takes more time, i.e. beyond the scheduled time then we must reach out to Jeffrey.foglietta@mountsinai.org for assistance.

 To schedule a NetBackup for server wise we can reach out to Jeff or vendor to confirm at what time the backup can be scheduled.

 Configuring of the backups for express editions will be taken care of by vendor but if we receive any issues, we can work on them depending on the cases by using task scheduler. (Ola [hallen](https://mtsinai.sharepoint.com/sites/CloudOperations-CMS/_layouts/15/Doc.aspx?sourcedoc=%7BE903E059-4DF5-42C7-BCFA-95AE7EDE64BB%7D&file=Notes.docx&action=default&mobileredirect=true) green scripts)

**Difficulties encountered related to backup issues:**

* Backup strategy Issue: - Insufficient information provided for backup policies. Risks can be found from all recovery scenarios, and this would probably affect the point in time recovery of the backups.
* NetBackup Failure alerts issue: Incidents or alerts of failed backups aren’t triggered to the DBA teamwork queue in service now or through emails.

**Process flow diagram for backup:**

![](data:image/png;base64...)

![](data:image/png;base64...)

![](data:image/png;base64...)

## RTO/RPO

* Process needs to be defined as per client

## STORAGE

* Cloud storage or datacenter storage

## Monitoring Process

* My Wizard Monitoring Tool
* Email Address
* SMS\On call
* App Notifications on Mobile app.

## Reboot/Restart Process

* Wintel / Azure Team after setting blackout on My wizard monitoring tool.
* Need to give reference of SR/CR.

## Service Level Agreement

 **SERVICE MANAGEMENT RUN SERVICES (Standard Processes)**

* Incident Management
* Problem Management
* Change Management
* Request management

 **SERVICE MANAGEMENT RUN SERVICES (Non-Standard Processes)**

* Service Request Fulfilment Management
* Major Incident Management
* Knowledge Management
* Configuration Management

## Ticketing Tools

* Ticketing tool in use is Service Now.
* Link: [https://mountsinaihealth.service-now.com/](https://mountsinaihealth.service-now.com/now/nav/ui/classic/params/target/incident_list.do)

## Change management Overview

* Change Management encompasses activities that ensure that proposed changes to any aspect of the infrastructure are controlled, monitored, and implemented with minimum disruption to the service(s) being delivered.
* This can be controlling changes to any aspect of services: to the infrastructure, to an application component, to a process or document, etc. A large component of change management is configuration management, which establishes and maintains the integrity and currency of the configuration items.
* A change request must be submitted with all required documentation, including the Standard Operating Procedure (SOP), Work Plan, and email approvals for downtime or implementation time. The submission should detail proper planning, risk assessment, and a backout plan.
* The change request is subject to review and approval by the Team Lead and will subsequently be presented during the internal TAB (Technical Advisory Board) call.
* Upon TAB approval, the change request undergoes two additional phases of approval: Peer review by DBA team members and Managerial approval from Rachel, Jeevan, or Paul. All approvals must be secured by 12:00 PM every Tuesday.
* A CAB (Change Advisory Board) call is held every Wednesday at 10 AM to review and finalize the changes. Once a change is approved in the CAB meeting, it may proceed to the implementation phase.

## Change process defined for disk expansion requests

Below are the listed Steps to follow when requesting disk space expansion: -

* + We will drop an email to the Wintel team with the necessary findings and request Wintel team to create the change request.
  + Once the CR is created, the SQL team will review the change request.
  + Once the CR is created and reviewed, Wintel team will reach out to the app owner for approval and to decide the time and the downtime requirement.

## Change process defined for patching requests

For any changes with regards to the performing of patching activity below points needs to be confirmed before we proceed to action on the CHG or CTASK assigned to DBA (Database Administrator) team:

* + Do these changes require a reboot? If yes, downtime would be required.
  + Were they tested in a non-production environment?
  + Will an app owner be available to test after the changes are complete?
  + To get confirmation on what KB is required to be patched on the servers?

## Process to decommission the alerts on monitoring tools

Whenever there is a need of disabling the alerts from My wizard below steps needs to be followed:

* Login to the Splunk tool using your PA account and password, below is the link to be used:

<https://mywizard.msnyuhealth.org/en-US/account/login?return_to=%2Fen-US%2F>

* Follow these actions: My Wizard AiOps Stack Monitoring Suite > ConfigWizard Blackout > Create Blackout > Enter Key (Server name), Metric and Instance > Enter timeline > Submit

## Request management Overview

**Overview:**

* + A user submits a service request from your service management portal.

Link to open SR for DBA Team: [Open a service request](https://mountsinaihealth.service-now.com/mshsportal?id=sc_cat_item&sys_id=9fab823d1bb0ac10a921a977b04bcbda&sysparm_category=null&catalog_id=-1&referrer=popular_items)

* + The service request is assigned to a service desk agent from the IT service team.
  + The agent assesses the request based on the standard qualification and approval processes.

**Below is the list of a few use case instances:**

* + For any of the requests pertaining to the granting of access, an SR needs to be created.
  + For Installation of SQL server components on SQL server, SR needs to be created.
  + For Patching of the Non-PROD SQL server, SR needs to be created.
  + For the execution of the scripts on SQL server, SR needs to be created.
  + For new builds, the SR needs to be open to perform ORC.

## Incident management Overview

* Need to define Incident response SLA, resolution SLA

SLA response and resolution time followed for incidents:

Incident Response SLA time: P1 - 20 mins, P2 - 20 mins, P3 - 8 Hours, P4 - 18 hours
 Incident Resolution SLA time: P1 - 2 hours, P2 - 4 hours, P3 - 3 business days, P4 - 5 business days
 CPI - High Impact, KPI - Medium Impact, GPI - Low Impact

Process to be followed if there any critical alerts received at DBA end from SCOM Monitoring:

* + Make sure to acknowledge every issue received from our end.
  + We will make sure that an incident is created for every alert email or any issue we receive at our end.

## Problem management Overview

* Problem Record Ticket (PRB) is created by SM Team and is assigned to DBA Team.
* The PRB have 5 states – Access> Root Cause Analysis > Fix in Progress > Resolved > Closed
* All the PRBs are discussed every week with MSHS Leads and CMS Leads in Tuesday’s weekly call.
* DBA Team has to take appropriate actions to work on the problem statement and look for a permanent resolution, the resolution idea is approved by MSHS Leads and only then implemented.
* PRB will be closed only after getting closure approval by MSHS Leads – Joe b/Rachel/Paul.
* **Below is the list of a few use case instances:**

Multiple incidents received for Database Status for 1 MSSQL DB server

High number of Active Session alert from 11 SQL servers

Threshold breached for INFRA Host Disk for Logical Disk: % Space Used

MSHS-DBA-SQL Server - (INC14065081) software / password Safe / application down

## Audits

* Define Sox Audit, Internal and external audits

## High Availability

* Log shipping – Database level – One Primary multiple secondary’s
* Mirroring – Database level – One to one – Principal and mirror
* Replication – Object level – One direction or by directional
* Clustering – Active\Passive
* Always on high availability – Synchronous commit or asynchronous commit – 2 to 8 Replicas

## SSIS/SSRS

Not in scope of work.

## Patch Implementation

### Patching SQL server Standalone

1. **Copy the Patch**:
   Copy the required SQL Server patch from the software library to the designated patching directory on the server.
2. **Get Approval**:
   Obtain approval from MSH leads to proceed with the patching of the servers.
3. **Create Requests**:
   * For non-production environments, create a Request for Information (RITM).
   * For production environments, create a Change Request (CR).
4. **Downtime Approval**:
   Secure downtime approval from the application owner before proceeding with the patching.
5. **Backup Databases**:
   Take a fresh backup of all databases to ensure you can restore them if needed:
   * Open SQL Server Management Studio (SSMS).
   * Right-click on each database > Tasks > Back Up.
   * Choose the backup destination and start the backup process.
6. **Apply the Patch**:
   Follow these steps to apply the patch:
   * **Pre-Checks**:
     + Open the SQL Server Configuration Manager and check SQL Service status
     + Open SSMS and check DB status
   * **Run the Patch Installer**:
     + Navigate to the directory where the patch was copied.
     + Right-click on the installer file and select "Run as administrator."
   * **Follow the Installer Prompts**:
     + Accept the license terms.
     + Choose the appropriate SQL Server instance to patch.
     + Complete the installation process, following any additional prompts.
   * **Restart SQL Server**:
     + Go back command prompt and execute shutdown –r to restart the server.
7. **Post-Implementation Validation**:
   * Verify that the SQL Server instance is running by checking the SQL Server Management Studio.
   * Run DBCC CHECKDB on all databases to validate integrity:
     + Open a new query window in SSMS.
     + Execute the command: 'DBCC CHECKDB (''DB name'') WITH NO\_INFOMSGS'
8. **Document and Communicate**:
   * Document the patching process and any issues encountered.
   * Notify stakeholders that the patching is complete and share any relevant findings.
9. **Monitor**:
   * Monitor the SQL Server performance and application functionality post-patching for any anomalies.

### Patching SQL Server for Availability Groups (AG) and Failover Cluster Instances (FCI)

### 2.32.1 Patching an Availability Group (AG)

1. **Copy the Patch**:
   Copy the required SQL Server patch from the software library to a designated patching directory on all nodes in the AG.
2. **Get Approval**:
   Obtain approval from MSH leads to proceed with patching the servers.
3. **Create Requests**:
   * For non-production environments, create a Request for Information (RITM).
   * For production environments, create a Change Request (CR).
4. **Downtime Approval**:
   Secure downtime approval from the application owner before proceeding with the patching.
5. **Pre-checks:**

**Capture relevant screenshots from the server for reference, SQL Server services, DB state, AG state, AG settings.**

1. **Backup Databases**:
   Take a fresh backup of all databases in the AG:
   * Open SQL Server Management Studio (SSMS).
   * Right-click on each database > Tasks > Back Up.
   * Choose the backup destination and start the backup process.
2. **Patch the Secondary Replica**:
   Follow these steps to apply the patch:
   * **Run the Patch Installer**:
     + Navigate to the patch directory.
     + Right-click on the installer file and select "Run as administrator."
   * **Follow the Installer Prompts**:
     + Accept the license terms.
     + Choose the appropriate SQL Server instance to patch.
     + Complete the installation process.
   * **Restart SQL Server**:
     + Go back command prompt and execute shutdown –r to restart the server.
3. **Patch the Primary Replica**:
   * **Failover**: Initiate a manual failover to promote the secondary replica to primary.
   * **Run the Patch Installer**: Repeat the patching steps as done for the secondary replica.
   * **Restart SQL Server** and failback.
4. **Post-Implementation Validation**:
   * Validate that all replicas are online and synchronized.
   * Run DBCC CHECKDB on all databases in the AG: 'DBCC CHECKDB (''DB name'') WITH NO\_INFOMSGS'
5. **Document and Communicate**:
   * Document the patching process and any issues encountered.
   * Notify stakeholders that the patching is complete and share any relevant findings.
6. **Monitor**:
   * Monitor the SQL Server performance and application functionality post-patching for any anomalies.

### Patching a Failover Cluster Instance (FCI)

1. **Copy the Patch**:
   Copy the required SQL Server patch from the software library to a designated patching directory on all nodes in the FCI.
2. **Get Approval**:
   Obtain approval from MSH leads to proceed with patching the servers.
3. **Create Requests**:
   * For non-production environments, create a Request for Information (RITM).
   * For production environments, create a Change Request (CR).
4. **Downtime Approval**:
   Secure downtime approval from the application owner before proceeding with the patching.
5. **Backup Databases**:
   Take a fresh backup of all databases:
   * Open SQL Server Management Studio (SSMS).
   * Right-click on each database > Tasks > Back Up.
   * Choose the backup destination and start the backup process.
6. **Patch the Active Node**:
   Follow these steps to apply the patch:
   * **Initiate Failover**: Manually failover to a passive node to make it the active node.
   * **Run the Patch Installer**:
     + Navigate to the patch directory.
     + Right-click on the installer file and select "Run as administrator."
   * **Follow the Installer Prompts**:
     + Accept the license terms.
     + Choose the appropriate SQL Server instance to patch.
     + Complete the installation process.
   * **Restart SQL Server**:
     + Go back command prompt and execute shutdown –r to restart the server.
7. **Patch the Passive Node**:
   * **Failover Back**: After patching the active node, failover back to the original node.
   * **Repeat the Patch Process**: For the newly active node, repeat the steps to stop services, run the installer, and restart services.
8. **Post-Implementation Validation**:
   * Ensure that all nodes are online and the FCI is operational.
   * Run DBCC CHECKDB on all databases:
9. **Document and Communicate**:
   * Document the patching process and any issues encountered.
   * Notify stakeholders that the patching is complete and share any relevant findings.
10. **Monitor**:
    * Monitor the SQL Server performance and application functionality post-patching for any anomalies.

![](data:image/png;base64...)

## DB Maintenance

Database maintenance jobs are essential for ensuring the health, performance, and reliability of SQL Server databases. These jobs help automate routine tasks and can prevent data corruption, improve performance, and ensure data integrity.

### Common Database Maintenance Tasks

* **Backups**
* **Full Backups:** Complete backup of the entire database. Recommended on a regular schedule (e.g., daily).
* **Differential Backups:** Backup of changes since the last full backup. Useful for faster recovery.
* **Transaction Log Backups:** Capture changes since the last transaction log backup. Important for point-in-time recovery.
  + **Index Maintenance**
* **Rebuilding Indexes:** Eliminates fragmentation and optimizes index performance. Recommended during off-peak hours.
* **Reorganizing Indexes:** A less resource-intensive option to reduce fragmentation.
  + **Update Statistics**
* Regularly update statistics to help the SQL Server query optimizer make informed decisions about query plans.
* **Database Integrity Checks**
* **DBCC CHECKDB:** Run this command to check for corruption and integrity issues in the database. Typically scheduled weekly.
* **Cleanup Tasks**
* **Removing Old Backup Files:** Regularly delete outdated backup files to free up disk space.
* **Truncating Transaction Logs:** For databases in simple recovery mode, truncate logs to reclaim space.

## DISASTER RECOVERY

* DR strategies, design, implementation and support.

## Daily Tasks

* Backups - Check your backups to validate that they were successfully created per your process.
* Nightly Processing - Review the nightly or early morning processes.
* SQL Server Error Log - Review the SQL Server error log for any errors or security issues (successful or failed logins) that are unexpected.
* Windows Event Log - Review the Application Event Log at a minimum to find out if any Windows or hardware related errors or warnings are being written.
* Some of the hardware vendors write warnings to the Windows Event Log when they anticipate an error is going to occur, so this gives you the opportunity to be proactive and correct the problem during a scheduled down time, rather than having a mid-day emergency.
* SQL Server Agent Jobs - Review for failed SQL Server Agent Jobs.
* Finding SQL Server Agent Job Failures
* HA or DR Logs - Check your high availability and/or disaster recovery process logs. Depending on the solution (Log Shipping, Clustering, Replication, Database Mirroring, CDP, etc.) that you are using dictates what needs to be checked.
* Performance Logs - Review the performance metrics to determine if your baseline was exceeded or if you had slow points during the day that need to be reviewed.
* Security Logs - Review the security logs from a third-party solution or from the SQL Server Error Logs to determine if you had a breach or a violation in one of your policies.
* Centralized error handling - If you have an application, per SQL Server or enterprise level logging, then review those logs for any unexpected errors.
* Standardized Error Handling and Centralized Logging
* Storage - Validate you have sufficient storage on your drives to support your databases, backups, batch processes, etc. in the short term.
* Service Broker - Check the transmission and user-defined queues to make sure data is properly being processed in your applications.
* Corrective Actions - Take corrective actions based on the issues and/or errors that you found.

## Monthly\Weekly

* Backup Verification (Comprehensive) - Verify your backups and test on a regular basis to ensure the overall process works as expected.  What is meant by this is to:
  + Contact your off-site tape vendor to obtain a tape
  + Validate that the tape goes to the correct office
  + Validate that the vendor delivers the correct tape
  + Validate that the vendor delivers the tape in the correct time period
  + Validate that the software version you use to perform the restore is compatible with the version from the tape
  + Validate that the tape does not have any restore errors
  + Validate that sufficient storage is available to move the backup to the needed SQL Server
  + Validate that the SQL Server versions are compatible to restore the database
  + Validate that no error messages are generated during the restore process
  + Validate that the database is accurately restored, and the application will function properly
* Backup Verification (Simple) - Verify your backups on a regular basis.
  + [Verifying Backups with the RESTORE VERIFYONLY Statement](http://www.mssqltips.com/tip.asp?tip=1093)/ Restore test database on lab/DBA server.
* Windows, SQL Server or Application Updates - Check for service packs/patches that need to be installed on your SQL Server from either a hardware, OS, DBMS or application perspective
* Capacity Planning - Perform capacity planning to ensure you will have sufficient storage for a specific period of time such as for 6, 12 or 18 months.
  + [Easing the Capacity Planning Burden](http://www.mssqltips.com/tip.asp?tip=1128)
* Fragmentation - Review the fragmentation of your databases to determine if your particular indexes must be rebuilt based on analysis from a backup SQL Server.
* Maintenance - Perform database maintenance on a weekly or monthly basis.
* Security - Remove unneeded logins and users for individuals that have left the organization, had a change in position, etc.

## Common or Known Issues

* SQL Performance
* Hardware Performance (CPU, Memory, etc.)
* Database backups/recoverability
* Database/User security
* Login/User Issues
* Capacity Planning
* Software Upgrades (Patches, Hotfixes, Service Packs)
* Development->Productions object migration
* Troubleshooting/On-Call support
* Documentation

## Management Tools

* Provide a description of any Management tools that the platform uses:
* SQL Server Management Studio (SSMS) – Query editor for executing T-SQL commands.
* SQL Server Agent - Scheduling and executing jobs.
* SQL Server Profiler – Trace and analyze SQL Server Activity.
* SQL Server Data Tools (SSDT) – Schema and data comparison tool.
* Azure Data Studio – Interface for querying and managing SQL Server
* SQL Server Configuration Manager – Start, Stop and Configure SQL Server instances.
* Performance Monitor (PerfMon) – Track performance counters like CPU/Memory and Disk IO.
* Database Engine Tuning Advisor (DTA) - Analyze workloads and suggest indexes, partitioning, and statistics.
* Third-Party Tools

## SOPs

* Standard operation procedures documents.

SOP documents are uploaded in the share point:

[https://mtsinai.sharepoint.com/:f:/r/sites/MSSQLDBATeam/Shared%20Documents/General/SOP?csf=1&web=1&e=tbQmtA](https://mtsinai.sharepoint.com/%3Af%3A/r/sites/MSSQLDBATeam/Shared%20Documents/General/SOP?csf=1&web=1&e=tbQmtA)

### Process to Remediate OLE DB, ODBC, and Azure Data Studio Version Upgrade

### 1. ****OLE DB/ODBC Version Upgrade****

1. **Identify Required Version**:
   Determine the necessary OLE DB/ODBC version based on the tenable scan report.
2. **Copy the Installer**:
   Download the latest OLE DB/ODBC driver from the official Microsoft website and copy it to a designated directory on the server.
3. **Get Approval**:
   Obtain approval from MSH leads for the upgrade.
4. **Create Requests**:
   * For non-production environments, create a Request for Information (RITM).
   * For production environments, create a Change Request (CR).
5. **Change Implementation Approval**:
   Secure implementation date and time approval from the application owner before proceeding with the upgrade.
6. **Backup Configuration**:
   Backup any configuration settings related to the current OLE DB/ODBC setup.
7. **Install New Version**:
   * Run the downloaded installer as an administrator.
   * Follow the prompts to complete the installation.
8. **Post-Installation Validation**:
   * Verify the installation by checking the version via the Windows registry or control panel.
   * Ask application team to Test connectivity and functionality with the applications using OLE DB.
9. **Document and Communicate**:
   * Document the upgrade process and any issues encountered.
   * Notify stakeholders that the upgrade is complete and share any relevant findings.

### Steps to Upgrade Azure Data Studio

1. **Identify Required Version**:
   Determine the necessary Azure data studio version based on the tenable scan report.
2. **Get Approval**:
   Obtain approval from MSH leads for the upgrade.
3. **Create Requests**:
   * For non-production environments, create a Request for Information (RITM).
   * For production environments, create a Change Request (CR).
4. **Change Implementation Approval**:
   Secure implementation date and time approval from the application owner before proceeding with the upgrade.
5. **Open Azure Data Studio**:
   Launch Azure Data Studio on your machine.
6. **Check for Updates**:
   * In the top menu, click on **Help**.
   * From the dropdown, select **Check for Updates**.
7. **View Available Updates**:
   * a notification will appear indicating the new version and prompting you to update.
8. **Apply the Update**:
   * Click on the **Update Now** button in the notification.
   * Azure Data Studio will download the update.
9. **Restart Azure Data Studio**:
   * Once the download is complete, you may be prompted to restart Azure Data Studio to apply the update.
   * Click **Restart Now** to proceed.
10. **Verify the Update**:
    * After Azure Data Studio restarts, go back to **Help** > **About** to confirm that the version has been updated successfully.
11. **Post-Update Validation**:
    * Check the connectivity to your databases and ensure all extensions and settings are intact.
12. **Document and Communicate**:
    * Document the update process and any issues encountered.
    * Notify stakeholders that the update is complete.

### Steps to Decommission a SQL Server Database

### 1. ****Identify Database for Decommissioning****

* Review database usage and confirm that it is no longer required.
* Ensure there are no active connections or dependencies.

### 2. ****Get MSH Leads Approval****

* Obtaining approval from MSH leads to proceeding with the decommissioning process.

### 3. ****Create Change Request****

* Create a Change Request (CR) to keep the database offline for a period of 30 days before final decommissioning.
* Specify the reason for decommissioning and the intended timeline.

### 4. ****Get Application Owner Approval****

* Secure approval from the application owner to perform the change, informing them of the downtime and impact.

### 5. ****Backup the Database and Logins****

* Take a fresh backup of the database:
  + Open SQL Server Management Studio (SSMS).
  + Right-click on the database > Tasks > Back Up.
  + Choose the backup destination and start the backup process.
* Backup logins associated with the database:
* Store the backup files in a secure location.

### 6. ****Set Database Offline****

* Execute the following steps to take the database offline:
  + Right-click on the database in SSMS.
  + Select **Tasks** > **Take Offline**.
  + Confirm the action.

### 7. ****Blackout Database Status in Monitoring****

* Update your monitoring tool (My Wizard) to set the database status to "blackout" to prevent alerts during the 30-day offline period.

### 8. ****Change Request Implementation State****

* Ensure the CR remains in the implementation state for the full 30 days to monitor any potential issues.

### 9. ****Monitor for Issues****

* During the 30-day period, check for any user-reported issues related to the database.

### 10. ****Delete the Database****

* If no issues are reported, proceed to delete the database:
* Right-click on the database in SSMS.
* Select **Delete**.
* Confirm the deletion.

### 11. ****Close the Change Request****

* Notify the application owner that the database has been successfully decommissioned.

### 12. ****Backup Retention****

* Store the backup files for 3 months unless otherwise specified by the application owner.
* Ensure the backup retention policy is communicated and adhered to.

### 13. ****Document the Process****

* Document the entire decommissioning process, including approvals, backup details, and any issues encountered.

### Memory allocation in SQL server

Configuring memory settings in SQL Server is essential for optimizing performance and ensuring that the server has sufficient resources to handle workload demands. This guide outlines the steps to change the memory configuration.

**1. Assess Current Memory Configuration**

Before making changes, assess the current memory settings:

* SQL Server Management Studio (SSMS):
* Open SSMS and connect to the SQL Server instance.
* Right-click the server instance and select Properties.
* Go to the Memory page to view current settings.

**2. Determine New Memory Settings**

Decide on the new memory configuration based on workload requirements, available physical memory, and server resources. This should be reviewed by MSHS Leads Scott/Paul, and the final decision should come from them.

Consider factors such as:

* Total physical memory on the server.
* Other applications and services running on the same server.
* Expected workload and performance goals.

**3. Change Memory Configuration in SSMS**

If the server is Production, open a CR to make memory changes, if it is non-prod, open RITM to make changes. The below steps re to be followed for implementation:

* Open SQL Server Management Studio and connect to the instance.
* Right-click on the server instance in Object Explorer and select Properties.
* Click on the Memory tab.
* Adjust the following settings:
* Minimum server memory (MB): Set the minimum amount of memory that SQL Server can use. This value should be 0.
* Maximum server memory (MB): Set the maximum amount of memory that SQL Server can utilize.
* Click OK to apply the changes.

**4. Monitor and Validate Changes**

After making changes, monitor SQL Server performance to ensure the new memory configuration meets workload requirements.

Use the following T-SQL query to check the updated memory settings:

* EXEC sys.sp\_configure 'min server memory';
* EXEC sys.sp\_configure 'max server memory';

Also, keep an eye on performance metrics, including query performance and system resource utilization.

## Process to adhere:

* 1. **With regards to the alerts received from My Wizard/DB mail, below process needs to be followed:**
  + If the CMS team receives an email alert that says “Error” or “Critical” they are to open a ticket in ServiceNow.
  + As a matter of process, they will respond to the alert with “Received by xyz <ex - DBA>, incident ticket <INC123> in ServiceNow has been created and assigned to group xyz.”
  + These should be treated as P2s and tracked as such
  + Please confirm receipt of this email and when it has been formally communicated as a process to the CMS teams

 **2) When the server isn't present in the inventory:**

- SQL installed + DBAdmins AD group = assumption is within EDBA scope - add to inventory, onboard for My Wizard if not already

- SQL installed + no DBAdmins AD group = assumption is not within EDBA scope

- check CMDB owner, add to "not supported inventory list"

- confirm where alerts are sent, update if needed

FYI: CMS DBA working with CMS Wintel to pull a list of servers with SQL installed and what AD groups are applied

 **3) When we receive a SQL server installation request, Pre-requisites to be checked:**

When you receive a request for a fresh SQL installation the assumption is that this is a net-new SQL server and therefore would not be on our inventory list. In this same context you can assume that when the VMs/servers in question were built with the intention of being used for SQL the DB Admin group was not added.

**4) Whenever the user requests for SA account access**

Please make sure to get the approval from Joe/Rachel/Jeevan before responding to tasks where SA access is being requested.

**5) When we log off from the server, we have to make sure it is done on the command console instead of the windows start button.**

Steps: Press Windows + R

Type Logoff

**NOTE: DO NOT USE THE WINDOWS START BUTTON TO LOG OFF FROM THE SERVER, IT WILL LEAD TO SERVER GETTING POWERED OFF.**

**For these situations, please do the following:**

Reach out to app owner and confirm if this is a net new server

If net new, is it to replace an old server? If so when is the migration?

If not replacing an older server does the app owner have licenses purchased?

If no licenses purchased and a non-prod environment developer edition

If no licenses purchased and production environment, they need to be referred to # Software Asset Management SoftwareAssetManagement@mountsinai.org for appropriate scoping and licensing purchases

If replacing an older server AND that server is production what is the timeline for migration

If greater than six months refer to # Software Asset Management SoftwareAssetManagement@mountsinai.org for licensing questions as this span beyond allowed timeframe for migrations

Additionally, obtain current server host name that new server is to replace, ensure inventory is appropriately updated to indicate current server target decom date

We need to keep track of these and review them to make sure they are appropriately decommissioned, and we remove them from our inventory counts

If not, net new server confirms if net-new SQL install (i.e., was this previously only an app server but now SQL is being added?)

Refer to above licensing questions in this case

Refer to dev ops team for appropriate sizing

If net new server and no access reach out to Wintel to have our AD group added

Ravi, we discussed this previously, want to work with our dev ops partners to ensure such items are captured prior to server hand-off

There are likely other items we want to include here (drive letter info, Net installation, etc.)

**2.40.1: Process to follow prior Upgrading CPU Cores:**

The procedure for adding SKU (CPU cores) on the server:

CPU core Addition will be done by Azure/ Windows Team. Below were the steps to be followed from SQL and prior addition of CPU cores.

1. Stopping Services prior Wintel/ Azure proceed with CPU addition

2. In this step, post stopping the services from SQL end, Wintel will proceed with CPU core addition

3. Wintel will reboot the server once the addition of CPU cores is done.

4. We need to start the services once the server is up and validate the health checks.

## DBA CMS Support information:

M’sinai CMS DL - Mt.Sinai.CMS.SQLDBA@accenture.com

DBA Teams DL - DatabaseSupport-MSSQL@mountsinai.org

## Epic Servers Consolidation:

The below mentioned are the EPIC servers in our support-

zeuspwdbsql004     10.113.17.144    Multiple purpose SQL servers

zeuspwdbsql005     10.113.17.143    Multiple purpose SQL servers

zeuspwdbsql006     10.113.17.145    Multiple purpose SQL servers

zeusnwapcbl001     10.113.74.134    TST Caboodle

zeuspwapcbd001       10.113.17.9      PRD Caboodle

zeusnwapcub001     10.113.74.139    TST Cubes

zeuspwapccb001       10.113.17.8    PRD Cubes

SDPHSQLP01A001

SEPICUBP01A001

**Scope of work for CMS DBA:**

Any incidents\SRs related to Epic DBs are assigned to on-site DBAs.

Any modifications to be done on epic servers are done by on-site DBAs.

## SQL Installation pre-requisites:

When you receive a request for a fresh SQL installation the assumption is that this is a net-new SQL server and therefore would not be on our inventory list. In this same context you can assume that when the VMs/servers in question were built with the intention of being used for SQL the DB Admin group was not added.

For these situations, please do the following:

Reach out to app owner and confirm if this is a net new server

If net new, is it to replace an old server? If so when is the migration

If not replacing an older server does the app owner have licenses purchased?

If no licenses purchased and a non-prod environment developer edition

If no licenses purchased and production environment, they need to be referred to # Software Asset Management SoftwareAssetManagement@mountsinai.org for appropriate scoping and licensing purchases

If replacing an older server AND that server is production what is the timeline for migration

If greater than six months refer to # Software Asset Management SoftwareAssetManagement@mountsinai.org for licensing questions as this spans beyond allowed timeframe for migrations

Additionally, obtain current server host name that new server is to replace, ensure inventory is appropriately updated to indicate current server target decom date

We need to keep track of these and review them to make sure they are appropriately decommissioned, and we remove them from our inventory counts

If not, net new server confirms if net-new SQL install (i.e., was this previously only an app server but now SQL is being added?)

Refer to above licensing questions in this case

Refer to dev ops team for appropriate sizing

If net new server and no access reach out to Wintel to have our AD group added

Work with the dev ops partners to ensure such items are captured prior to server hand-off

There are likely other items we want to include here (drive letter info, .NET installation, etc.)

Team, please review and let me know if you have any questions or updates needed here.

**SQL server binaries placed in the server and directory:**

**ssptsqlp01a003** - H:\SQL SERVER SOFTWARE LIBRARY

## SQL Server certificate update

Please make sure that FQDN internal certificate is available on the server. If it is not available, request application owner to reach out to romil.chaurasia@mountsinai.org and the snow assignment group should be - **MSHS-ARCH-ENG-ACTIVE DIRECTORY** to create a FQDN internal cert and push it to the server. Once the certificate is available, SQL Team will apply the certificate to SQL server.

**Server certificate can be checked using below steps:**

* Open the MMC (Microsoft Management Console) by entering MMC on Command Prompt.
* Go to file, and then select Add/remove Snap-in.
* You will be shown a list of snap-ins. Choose Certificates from the list, then click Add.

![](data:image/png;base64...)

* On the next dialog prompt window, select Computer Account and click Next.
* Select your Local Computer on the next prompt and then click Finish.
* Next, click OK, and you will be redirected back to the snap-ins page.

**Steps to update certificate to SQL Server:**

1. In SQL Server Configuration Manager, in the console pane, expand **SQL Server Network Configuration**.
2. Right-click **Protocols for** *<MSSQLSERVER>*, and then select **Properties**.
3. Choose the **Certificate** tab, and then select the certificate and click on apply.
4. And restart SQL Server to apply the changes.

(Before restarting make sure change is in place for PROD and is approved by CAB).

![image](data:image/png;base64...)

**2.45 Process for Firewall Change Implementation:**

1. Weekly Standard Change

* No Firewall changes will be made outside normal change windows, without an emergency or expedited change being approved.
* Standard Firewall change windows are Tues, Wed, and Thurs from 00:00 to 08:00 and 17:00 to 23:59.

1.Requests (Firewall)

Application owners requesting a firewall change should follow one of the methods below for submitting a request. [Firewall-Site to Site VPN Request | ServiceNow (service-now.com)](https://mountsinaihealth.service-now.com/nav_to.do?uri=%2Fcom.glideapp.servicecatalog_cat_item_view.do%3Fv%3D1%26sysparm_id%3D40db401897245110d0aab398c253af8c%26sysparm_link_parent%3Da6e1f95b1ba8a4102c072139b04bcb6d%26sysparm_catalog%3De0d08b13c3330100c8b837659bba8fb4%26sysparm_catalog_view%3Dcatalog_default%26sysparm_view%3Dcatalog_default)

1. Normal (within 1 week)

1. User submits firewall request using link above as a normal firewall request.

2. Firewall request goes through Wed firewall change meeting for approval.

3. After approval, firewall request is then ready to be implemented during normal firewall change windows.

4. Expedited (within 1-3 days)

1. User submits firewall request using link above as an expedited firewall request.

2. Firewall request goes through approval process via email or team’s chat.

3. After approval, firewall request is then ready to be implemented during normal firewall change windows.

5. Emergency (outside normal firewall change windows – ex. Friday to Monday)

1. User submits P2 incident to Unix Engineering team.

2. Unix Engineering team creates Emergency change from the P2 incident.

3. Unix Engineering team completes firewall change, then closes Emergency change and P2 incident.

**2.5 Adding security updates on server zeuspwepsidb001 for Visual Studio 2019**

Ref: CHG0076167

Step 1: Pre checks: Need to disable the operator alerts on both the nodes before performing the Visual Studio Update

Step 2: Open the Visual Studio Installer and resume installing the Visual Studio Update, once done take the snip of the Visual studio Version and attach it to the CHG.

![image](data:image/png;base64...)

Step 3: Once it is installed and updated, reboot the SIDB01 node and do the health checks post the reboot. (Make sure primary is as per PMON)

Step 4: Once health checks are completed, enable the email alerts for the same on both the nodes.

**2.46 Vendor Support Escalation Documentation:**

[Cloud Operations - CMS - Vendor Support Document - All Documents (sharepoint.com)](https://mtsinai.sharepoint.com/sites/CloudOperations-CMS/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FCloudOperations%2DCMS%2FShared%20Documents%2FGeneral%2FRunbook%2FVendor%20Support%20Document&viewid=98ee747f%2D3337%2D4c20%2Da48f%2D5086f684be2f)

**2.47 MSHS Vendor Support Documentation**

![](data:image/png;base64...)

**2.48: Subscription to Microsoft Articles to receive the latest updates**

![](data:image/png;base64...)

**2.49: Patching Escalation Process**

Below is the escalation process to be followed in events of delay to patching.

**Emergency or Ad hoc Patching Process**

In the event a system must be patched outside of the patching (zero-tolerance critical patch release by vendor), following process should be followed.

| Responsible Role | Activity |
| --- | --- |
| CMS | An emergency change request will be raised and seek approval as per - IT Service Management (ITSM) - Change Management. |
| Application Owner | Reviews and approves the emergency patching change request. |
| MSHS Cloud Operations Lead | Reviews and approves the emergency patching change request. |
| CAB Approver | Reviews and approves the emergency patching change request. |
| CMS | Following approval, the email notification will be sent to the stakeholders and patching would be executed for any specific reason or to remediate a patching failure at appropriate maintenance window. |

**Patching Exception**

| Responsible Role | Activity |
| --- | --- |
| CMS | All servers which are part of “unscheduled server", "Vendor app owner managed”, “Do not Patch” will be excluded from patching |
| Application Owner | * Any existing or newly introduced system in Landing Zone, which deviates from the patching guidelines in this Runbook must gain exception approval. * Any system owner who requires their servers to be excluded from the patching guidelines in this Runbook will gain exception approval before that server is excluded from patching.   All exceptions will be submitted and approved via ServiceNow.  The ServiceNow catalog item to be submitted.   * If the app owner wants to reschedule the server and the new schedule exceeds more than 5 business days has to get exception.   Note: The server needs to be excluded from the update deployment schedule. |
| Application Owner | Any ad-hoc exceptions that cannot adhere to the Patching Exception process will need email approval from MSHS Cloud Operations, which will lead to being excluded from scheduled patching. The Application Owner will be required to formally request exception approval through the Patching Exception process as defined above. |
| Cloud Operations Engineer | Systems that received Ad hoc exception approval will be re-added to the patch schedule after the exception period agreed to by the MSHS Cloud Operations lead.  Any system that has formal patching exception approval and needs to be re-introduced into the patching schedule will require approved RITM submitted by Application Owner. |
| Rescheduled Exception | If any server is requested for reschedule for more than 5 business days has to get patching exception. |

The process also includes a task to raise risks with the client

Work with the CDP account manager and assess the CDP Security exception process: - Reach out to

SDM in order to get the Security Exception Raised in events of Inherited Vulnerabilities.

**Escalation Matrix to be followed:**

CMS and Client Escalation Matrix:

| Level | Escalation Contact | Escalation Email |
| --- | --- | --- |
| 1 | Ajaysingh Raichurkar | ajaysingh.raichurkar@mountsinai.org |
| 2 | Raviraj Chelluri | Raviraj.chelluri@mountsinai.org |
| 3 | Suprovat Sinha | Suprovat.Sinha@mountsinai.org |
|  |  |  |
| Level | Escalation Contact | Escalation Email |
| 1 | Jeevan Mahesh | jeevan.mahesh@mountsinai.org |
| 2 | Rachel Roddy | rachel.roddy@mountsinai.org |
| 3 | Joseph Brittelli | joseph.brittelli@mountsinai.org |
| 4 | Paul Di Talia | paul.ditalia@mountsinai.org |

**2.50: Total number of dBs in scope**

Below is the list of dBs to be supported by Offshore CMS.

Any issues related to the excluded dBs should be taken care of by the Onshore, any incidents related to them should be assigned to the Onshore Team.

[Infrastructure Volumetrics - MS SQL.xlsx](https://mtsinai.sharepoint.com/%3Ax%3A/r/sites/CloudOperations-CMS/Shared%20Documents/General/Inventory/Infrastructure%20Volumetrics/Weekly/2024/January/Week%202/Infrastructure%20Volumetrics%20-%20MS%20SQL.xlsx?d=w463170f58ca74e27a7abda86aa6d255f&csf=1&web=1&e=iIXevX)

**2.6** **STEPS TO RETRIEVE DB COUNT**

**Step 1:** Establishing connection to the Centralized Management Server – **ZEUSPWAPMON001**.

We RDP the server using our PA credentials.

![](data:image/png;base64...)

**Step 2:** All the server related data is stored in **PMON** Database. In order to onboard a new server into our CMS Support list, we execute the attached insert query against the table **Msinaiservers**.

![](data:image/png;base64...)

![](data:image/png;base64...)

**Step 3:** To get Database related information, we run power-shell script **get-Databases\_New** that fetches all the active database list running under all the servers present in CMS and loads it into the **Server\_Database\_Info** table.

![](data:image/png;base64...)

**Step 4:** We retrieve the database count and info by running the below mentioned select query against **Server\_Database\_**Info table, we only consider database with normal running status (excluding the offline\restoring state dB's), and we also exclude the databases asked by client to ignore (like master, msdb, tempdb, etc.)

![](data:image/png;base64...)

