
# Basic Linux Vi Commands

## Modes & Controls

| Command             | Description                                 |
| ------------------- | ------------------------------------------- |
| vi *filename*       | Edit *filename*                             |
| vi -r *filename*    | Edit last version of *filename* after crash |
| vi + n *filename*   | Edit *filename* at end of file              |
| vi + *filename*     | Edit *filename* at end of file              |
| vi +/str *filename* | Edit *filename* at first occurance of str   |

## Allowing Users to Connect via SSH
cat /etc/ssh/sshd_config
To find a character string, type / followed by the string you want to search for, and then press Return. 
vi positions the cursor at the next occurrence of the string. For example, to find the string “meta,” type /meta followed by Return.


# Microsoft Azure PowerShell

This repository contains PowerShell cmdlets for developers and administrators to develop, deploy,
administer, and manage Microsoft Azure resources.

The Az PowerShell module is preinstalled in [Azure Cloud Shell][AzureCloudShell].


```powershell
Update-Module -Name Az -Scope CurrentUser -Force
```

`Update-Module` installs the new version side-by-side with previous versions. It does not uninstall
the previous versions.

For more information on installing Azure PowerShell, see the
[installation guide][InstallationGuide].

## Usage

### Log into Azure

To connect to Azure, use the [`Connect-AzAccount`][ConnectAzAccount] cmdlet:

```powershell
# Opens a new browser window to log into your Azure account.
Connect-AzAccount

# Log in with a previously created service principal. Use the application ID as the username, and the secret as password.
$Credential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $Credential -TenantId $TenantId
```
