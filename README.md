# Hybrid Identity with Microsoft Entra Connect

## Overview

This project demonstrates the implementation of a hybrid identity environment by integrating an on-premises Active Directory with Microsoft Entra ID (Azure AD). The solution enables seamless identity synchronization, allowing users to access both on-premises and cloud resources using a single set of credentials.

## Project Objectives

- Deploy a Windows Server virtual machine in Azure
- Configure Active Directory Domain Services (AD DS)
- Add and verify a custom domain (`arizaylab.tech`) in Microsoft Entra ID
- Install and configure Microsoft Entra Connect Sync
- Enable Password Hash Synchronization (PHS)
- Synchronize on-premises users to the cloud
- Validate hybrid identity by confirming users appear in Entra ID

## Purpose

This project was developed to gain hands-on experience with hybrid identity, a critical concept in modern cloud and enterprise environments. Many organizations operate across both on-premises and cloud infrastructures, and understanding how to securely bridge these environments is essential for roles in:

- Cloud Engineering
- Identity and Access Management (IAM)
- Cybersecurity (particularly for certifications such as SC-300)

## Technologies Used

- Microsoft Azure (Azure Virtual Machine)
- Windows Server 2022
- Active Directory Domain Services (AD DS)
- Microsoft Entra ID (Azure Active Directory)
- Microsoft Entra Connect Sync
- Remote Desktop Protocol (RDP)
- PowerShell

## Reproduction Steps

### 1. Create an Azure Virtual Machine

- Deploy a Windows Server VM in Azure
- Enable RDP (port 3389)
- Connect to the VM

### 2. Configure Active Directory

- Install the AD DS role
- Promote the server to a Domain Controller
- Create a domain (e.g., `arizaylab.local`)

### 3. Add a Custom Domain in Entra ID

- Navigate to the Microsoft Entra Admin Center
- Add and verify the custom domain (`arizaylab.tech`)

### 4. Prepare Active Directory for Synchronization

- Add the UPN suffix (`arizaylab.tech`)
- Create test users in Active Directory

### 5. Install Microsoft Entra Connect

- Download the installer from the Entra Admin Center
- Choose Custom Installation
- Select Password Hash Synchronization
- Connect to both:
  - On-premises AD
  - Entra ID (using Global Admin credentials)

### 6. Configure Synchronization

- Map the UPN suffix to the verified domain
- Select users and OUs to synchronize
- Enable optional features (e.g., Password Writeback if needed)

### 7. Verify Synchronization

- Go to the Entra Admin Center → Users
- Confirm that users display:
  - “On-premises synced” = Yes

### 8. Test Login

- Log in at https://portal.office.com
- Use a synced account (e.g., `user1@arizaylab.tech`)

## Key Learnings

- How to design and implement a hybrid identity architecture
- The role of Microsoft Entra Connect in identity synchronization
- Differences between on-premises AD accounts, cloud-only accounts, and synced identities
- How UPN suffixes affect the user sign-in experience
- How Password Hash Synchronization works for authentication
- Troubleshooting real-world issues such as:
  - Tenant authentication errors
  - Synchronization failures
  - Incorrect account usage
- The importance of identity consistency across environments

## Conclusion

This project successfully demonstrates a working hybrid identity setup in which users from an on-premises Active Directory are synchronized to Microsoft Entra ID and can authenticate in the cloud using the same credentials. The implementation reflects real-world enterprise identity infrastructure and reinforces practical cloud and IAM skills.
