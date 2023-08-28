<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

## Prerequisites
- Active Microsoft Azure account
- Familiarity with Active Directory and Azure
- PowerShell installed

## Environments and Technologies Used
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

## Operating Systems Used
- Windows Server 2022
- Windows 10 (21H2)

## Step 1: Setting Up Azure Virtual Machines
1. Log in to your Azure portal.
2. Create the 1st Virtual Machine by calling it DC-1, which stands for Domain Control.
3. Create the 2nd Virtual Machine by calling it Client-1. Make sure it's the same resource group as VM1. For example: AD-Lab will be the name of the resource group.
<table>
<tr>
<td>
<img src="https://i.imgur.com/ExNiOVz.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/jRETpct.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/iBunwAW.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/1aenMj1.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/zTVTYZJ.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/EiPp5Zo.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

## Step 2: Set Domain Controller’s NIC Private IP Address to Static
<table>
<tr>
<td>
<img src="https://i.imgur.com/mm2vDsD.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/kBmgknG.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<img src="https://i.imgur.com/CYRlCaY.png" alt="Image 1 Description" width="100%"/>

## Step 3: Ensure Connectivity Between the Client and Domain Controller
<table>
<tr>
<td>
<img src="https://i.imgur.com/Lcs4uhY.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/NC6ogFY.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/YNX10tD.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/w9aPUwc.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/t2vqxXM.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/lM6EaRE.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/CyZwo4Q.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/yjxoyCb.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

## Step 4: Install Active Directory Domain Services
1. Connect to your Azure VM via Remote Desktop.
2. Install Active Directory Domain Services (AD DS) using Server Manager.
3. Run post-installation configuration.
<table>
<tr>
<td>
<img src="https://i.imgur.com/1az49hv.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/dor2gGU.png"Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/NwUGQzC.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/mKsYFVH.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/ygwWzLj.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

## Step 4: Configure Active Directory

### 3.1 Create Users and Groups
1. Open Active Directory Administrative Center.
2. Navigate to the user and groups OU.
3. Create users and groups as needed.
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/Du8f3Wc.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

### 3.2 Set Group Policies
1. Open Group Policy Management.
2. Create and link GPOs as necessary for your organization.
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
   
## Step 4: Test the Deployment
1. On a separate Azure VM, join the domain.
2. Test logging in with the user accounts you created.
3. Verify that Group Policies are applied as expected.
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

## Conclusion
Congratulations! You've successfully deployed an on-premises Active Directory environment in Azure. This allows for centralized identity and access management within your cloud resources.

<img src="https://i.imgur.com/oixcf9e.png" alt="Image 1 Description" width="100%"/>
