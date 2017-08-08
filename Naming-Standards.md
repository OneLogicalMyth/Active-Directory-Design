--
title: Naming Standards - Active Directory Design
--

# Functional Group
A functional group is best described as a non-administrative resource group. This group would see access being granted to resources across the infrastructure.

The following naming conventions should be used:
* {TYPE}-{DESCRIPTION}-{ACCESS}

For example a department group name for the software department would be:
* DEPT-Software_Users ({TYPE}-{DESCRIPTION})

To give the software users access to the software share with Read/Write access the following group name would be used:
* FILE-Software_Users-RW ({TYPE-}-{DESCRIPTION}-{ACCESS})

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
|DEPT|Department groups, for grouping all users in a department|
