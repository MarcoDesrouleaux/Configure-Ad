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
<img src="https://i.imgur.com/Du8f3Wc.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/yBjCZXs.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/2pDAVZj.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

## Step 5: Configure Active Directory

### Create Users and Groups
1. Open Active Directory Administrative Center.
2. Navigate to the user and groups OU.
3. Create users and groups as needed.
<table>
<tr>
<td>
<img src="https://i.imgur.com/fq77FBU.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/mteE0ot.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/tORpWWH.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/LPlNLoz.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/mY05MQE.png".png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/oU0tKqc.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/unYO1XW.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/IGcYaGl.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/WZGLRw3.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/KAA6Zqo.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/R7cpHAL.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/g4hNqyC.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/3bTKrvj.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/QmAljnK.jpg" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>

### Step 6: Join Client-1 to Your Domain (mydomain.com)
<table>
<tr>
<td>
<img src="https://i.imgur.com/qmfw6zw.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/bJaLjTX.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/gekWh9q.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/yaMSF2a.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/Cjz5ae4.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/fJBXQvT.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/zvVJeUP.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/05OKIyZ.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<img src="https://i.imgur.com/82KQxk1.png" alt="Image 1 Description" width="100%"/>

### Step 7: Setup Remote Desktop for Non-Administrative Users on Client-1
<table>
<tr>
<td>
<img src="https://i.imgur.com/L5nRURZ.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/DfOREAg.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/RjAjCgl.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/4trgkPB.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
   
## Step 8: Create a Bunch of Additional Users and Attempt to Log Into Client-1 With One of the Users
Script: https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1
<table>
<tr>
<td>
<img src="https://i.imgur.com/2RwoWYg.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/rrhlEAm.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/7Cat0f0.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/cTet72U.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/goMj9h1.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/0wUkH3J.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<table>
<tr>
<td>
<img src="https://i.imgur.com/jxLlqMi.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/opr5X9j.jpg" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<img src="https://i.imgur.com/Uxefv5a.png"" alt="Image 1 Description" width="100%"/>

## Conclusion
Congratulations! You've successfully deployed an on-premises Active Directory environment in Azure. This allows for centralized identity and access management within your cloud resources.
