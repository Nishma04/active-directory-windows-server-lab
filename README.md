# Active Directory & Windows Server 2022 Administration Lab

## Project Overview
This project documents a hands-on lab created using Oracle VirtualBox and Windows Server 2022. The objective was to practise fundamental IT support and system administration tasks in a simulated business environment.

## Technologies Used
- Windows Server 2022
- Oracle VirtualBox
- Active Directory Domain Services (AD DS)
- DNS Server
- Group Policy Management
- Active Directory Users and Computers
- PowerShell
- SMB File Sharing

## Lab Environment
- Server hostname: ABC-SERVER
- Domain: abc.local
- Domain NetBIOS name: ABC
- Server IP: 192.168.10.10
- RAM: 3 GB
- Virtual disk: 50 GB dynamically allocated
- Virtual network: NAT

## Tasks Completed

### 1. Windows Server Installation
- Installed Windows Server 2022 Desktop Experience in VirtualBox.
- Renamed the server to ABC-SERVER.
- Configured the server's network settings.

### 2. Active Directory Configuration
- Installed Active Directory Domain Services.
- Promoted the server to a Domain Controller.
- Created the domain abc.local.
- Verified Active Directory services.

### 3. Organizational Units and User Management
Created three departmental Organizational Units:
- IT
- HR
- Finance

Created user accounts:
- it.user
- hr.user
- finance.user

Created security groups:
- IT Support
- Helpdesk

Added it.user to the relevant IT security groups.

### 4. Group Policy
- Created a Group Policy Object named IT Password Policy.
- Configured a minimum password length of 8 characters.
- Enabled password complexity requirements.
- Linked the policy at the domain level.

### 5. Shared Folder Configuration
- Created a CompanyShare folder.
- Created IT, HR and Finance subfolders.
- Configured SMB sharing.
- Practised share-level permissions.

### 6. DNS Administration
- Verified the DNS service.
- Checked the abc.local DNS zone.
- Used nslookup to test domain name resolution.
- Tested DNS queries against the local DNS server.

## PowerShell Commands Practised

```powershell
Get-Service NTDS, ADWS
Get-ADDomain
Get-WindowsFeature RSAT-AD-Tools
Get-Service DNS
Get-DnsServerZone
nslookup abc.local
nslookup abc.local 127.0.0.1
Get-SmbShare
Get-ADUser -Filter *
```

## Skills Practised
- Windows Server installation and configuration
- Active Directory administration
- User and security group management
- Password resets
- Group Policy configuration
- DNS troubleshooting
- SMB shared folder configuration
- PowerShell administration
- Basic IT support troubleshooting

## Areas for Further Practice
The following tasks were not completed or fully verified in this lab:
- Joining a Windows client computer to the domain.
- Testing Group Policy application from a client.
- Configuring and testing NTFS permissions.
- Configuring DHCP.
- Testing account lockout policies.
- Further investigating the initial DNS timeout.

## Learning Outcome
This lab provided practical exposure to basic Windows Server administration and Active Directory tasks commonly encountered in entry-level IT Support, Desktop Support and Help Desk environments.
