---
title: Naming Standards - Active Directory Design
---

[Return to Introduction]({{ site.baseurl }})

# Naming Standards
Naming standards are a important aspect to the design, ensuring these are met help with remedial tasks or auditing; as the reasons for their use are clearly defined.

## Functional Group
A functional group is best described as a non-administrative resource group. This group would see access being granted to resources across the infrastructure.

The following naming conventions should be used:
* {TYPE}-{HOST|CLUSTER}-{RESOURCE_NAME}-{ACCESS}

To give the software testing team access to the software share on FILESERVER01 with Read/Write access the following group name would be used:
* FILE-FILESERVER01-Software-RW

When defining a resource name ensure it matches that of the host or cluster; for example as above 'Software' is used to define the resource this should equally match the share name on the host, so this case from the group name we can clearly see the fileshare would be \\\\FILESERVER01\\Software.

The types have been defined as follows:

|Type|Usage|
|---|---|
|FILE|File share access|
|WEB|Intranet web site|
|SQL|SQL Database|
|SPNT|SharePoint web site|
|DIST|Exchange Distribution Groups|
|PRNT|Access to restricted printers or manage print queues|
|CTX|Citrix application|


## Team/Department/Division Group
This group is used for organising staff across the company into their relevant roles, an indivdual staff member might be a member of a multiple teams (job share etc.) the design of the naming convention allows this to happen.

The following naming convention should be used:
* {TYPE}-{DESCRIPTION}

For example a team group name for software test engineers would be:
* TEAM-Software_Testing

The types have been defined as follows:

|Type|Usage|
|---|---|
|TEAM|Team groups, for grouping all users in a team|
|DEPT|Department groups, for grouping all TEAM groups within a department|
|DIVI|Division groups, for grouping all DEPT groups within a division|
