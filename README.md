<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

1. Prepare Networking & Infrastructure

Set up your Azure Virtual Network (VNet) and Resource Group. This creates the secure foundation where your AD will live just like setting up the land before you build a house.

2. Extend or Sync Your AD to Azure

Use Azure AD Connect to synchronize your on premises AD with Azure AD. This keeps users, passwords, and groups consistent across environments.<p>

3. Deploy AD Domain Services or Virtual DCs

Decide whether to deploy Azure AD Domain Services (managed) or a full Domain Controller VM in Azure. This gives Azure based servers access to domain functions like login and group policy.

4. Test and Secure the Setup

Join Azure VMs to the domain, verify authentication (like login), and lock down DNS, VPNs, and firewall settings for security and reliability.

<h2>Deployment and Configuration Steps

</h2><img src="https://i.imgur.com/tKudual.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Launch Azure AD Domain Services
Action: In the Azure Portal, search for Azure AD Domain Services, then click Create.

Why it matters: This starts the setup wizard for creating a managed domain in Azure.</p>
<br />

<p>
<img src="https://i.imgur.com/H0CFU3E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Connect Your On-Premises AD via Azure AD Connect
Action: Run the Azure AD Connect wizard to link your on‑prem AD forests to your Azure AD tenant.

Why it matters: This syncs user identities and credentials securely between local and cloud environments.</p>
<br />

<p>
<img src="https://i.imgur.com/Q9teleE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Visual Architecture of AD Integration
Action: A diagram showing how on‑premises AD, Azure AD Domain Services, and Azure VM based Domain Controllers all connect via VNet/VPN.

Why it matters: It helps visualize how the infrastructure pieces including syncing, connectivity, and domain control fit together.</p>
<br />
