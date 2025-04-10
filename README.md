# Microsoft Entra ID - User Provisioning Script

This PowerShell script automates the creation of a new user in Microsoft Entra ID (formerly Azure Active Directory) and assigns the user to multiple predefined groups via the Microsoft Graph API using the **Microsoft Graph PowerShell SDK**.

## Prerequisites

Before running this script, make sure you have the following:

- PowerShell 7.x or later (recommended)
- Microsoft Graph PowerShell SDK installed
  ```bash
  Install-Module Microsoft.Graph -Scope CurrentUser
  
# An Azure AD account with the necessary permissions:

User Administrator role or higher to create users

Groups Administrator role or higher to assign users to groups

# Permissions Required
The script requires the following Microsoft Graph permissions:

User.ReadWrite.All

Directory.ReadWrite.All

Group.ReadWrite.All

Ensure that your account has been granted these permissions.

# Script Overview
Purpose
This script will:

Prompt the user for a secure password for the new user.

Check if a user with the specified UserPrincipalName already exists.

Create a new user in Microsoft Entra ID with the provided password.

Add the newly created user to several predefined Microsoft Entra ID groups.

# Groups Included
The user will be added to the following groups by default:

# Group Name	Group ID

M365-LICENCE-ALLSTAFF-E5	751262e4-d71b-4e50-88c1-7e653be34fd0

All Users	ee72e8a6-5d08-44cd-81a0-a46c15256ba2

Purus - Standard EMEA - SIG	7393c845-a979-479c-bd00-5ebb4c073a6d

Purus Group	09c5f1d4-1bde-40ac-a6a1-8dfa5306d17d

Purus Swansea	d276e455-c556-4cdb-b63b-1ce869ce22dd

# How to Use

1. Clone the Repository

git clone https://github.com/your-username/entra-user-provisioning.git
cd entra-user-provisioning

2. Run the Script
.\Create-EntraUser.ps1

# Provide Password
You will be prompted to enter a password for the new user. The password will be entered securely, and it will not be displayed in plain text.

# Review Output
If the user already exists, the script will exit and notify you.

If the user does not exist, it will be created and added to the specified groups.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# Support
For any issues or feature requests, please open an issue on this repository, and we will get back to you as soon as possible.

# About
This script is intended for managing user provisioning and group assignments in Microsoft Entra ID using the Microsoft Graph API. It simplifies and automates the user creation and group assignment process to save time for administrators.
