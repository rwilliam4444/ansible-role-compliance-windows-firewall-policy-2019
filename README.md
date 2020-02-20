# Role Name:
- ansible-role-compliance-windows-firewall-policy-2019

# Description:
This Firewall Policy Role was based off the CIS specs for 2019 servers.   This
role covers the "Windows Firewall With Advanced Security" CIS section only. The
checks and remediation commands are for local settings only. Group Policy
settings may override these settings. When the "remediate" variable is set to
"YES", the role will try to remediate the server's setting(s) accoridng to the
CIS standards.  The defaults/main.yml file can be used to disable specific CIS
items (i.e. "execute_<cis task #>") from executing. The default value in the
defaults/main.yml for these CIS item variables (i.e. "execute_<cis task #>") is
set to "YES". The value "YES" means that the CIS item will execute at run time.
Set the value to "NO" if you want to skip this CIS item in question from
executing.

# Requirements"
Windows Ansible related pre-requisites

# Role Variables:
# Defaults file for ansible-role-compliance-windows-firewall-policy-2019

Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| variable used to determine whether or not to remedaite.
__EnableFirewall_cis__ |"1"| CIS value.
__EnableFirewall_private_cis__ |"1"| CIS value.
__EnableFirewall_public_cis__ |"1"| CIS value.
__DefaultInboundAction_cis__ |"1"| CIS value.
__DefaultInboundAction_private_cis__ |"1"| CIS value.
__DefaultInboundAction_public_cis__ |"1"| CIS value.
__DefaultOutboundAction_cis__ |"0"| CIS value.
__DefaultOutboundAction_private_cis__ |"0"| CIS value.
__DefaultOutboundAction_public_cis__ |"0"| CIS value.
__DisableNotifications_cis__ |"0"| CIS value.
__DisableNotifications_private_cis__ |"0"| CIS value.
__DisableNotifications_public_cis__ |"1"| CIS value.
__AllowLocalPolicyMerge_cis__ |"0"| CIS value.
__AllowLocalPolicyMerge_private_cis__|"0"| CIS value.
__AllowLocalPolicyMerge_public_cis__ |"1"| CIS value.
__AllowLocalIPsecPolicyMerge_cis__ |"0"| CIS value.
__AllowLocalIPsecPolicyMerge_private_cis__ |"0"| CIS value.
__AllowLocalIPsecPolicyMerge_public_cis__ |"1"| CIS value.
__LogFilePath_cis__ |C:\windows\system32\logfiles\firewall\domainfirewall.log| CIS value.
__LogFilePath_private_cis__ |C:\windows\system32\logfiles\firewall\privatefirewall.log| CIS value.
__LogFilePath_public_cis__ |C:\windows\system32\logfiles\firewall\publicfirewall.log| CIS value.
__LogFileSize_cis__ |16384| CIS value.
__LogFileSize_private_cis__ |16384| CIS value.
__LogFileSize_public_cis__ |16384| CIS value.
__LogDroppedPackets_cis__ |"1"| CIS value.
__LogDroppedPackets_private_cis__ |"1"| CIS value.
__LogDroppedPackets_public_cis__ |"1"| CIS value.
__LogSuccessfulConnections_cis__ |"1"| CIS value.
__LogSuccessfulConnections_private_cis__ |"1"| CIS value.
__LogSuccessfulConnections_public_cis__ |"1"| CIS value.



# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-firewall-policy-2019


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
