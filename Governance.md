---
title: Governance - Active Directory Design
---

# Governance
The below rules define how each type of Active Directory object should be used, anything that does not match is deemed as non-compliant.
The structure is monitored using an automated script built using PowerShell, this check the below defined governing rules and send administrative alerts for any identified non-compliant object.

## Functional Groups
Functional groups should not be nested with other functional groups. So the file share for software should not be nested in a file share for development, this can lead to an increased privilege being inadvertly granted when adding indivduals to the group.
