<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

Implementing an on-premises Active Directory within Azure Virtual Machines involves several steps. Here's an outline of the process:

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. **Design and Planning:**
   - Define the requirements for your Active Directory (AD) environment, including domain structure, forest, and domain names.
   - Determine the number of domain controllers needed and their hardware specifications.
   - Plan the network connectivity between your on-premises environment and Azure, considering VPN or ExpressRoute options.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. **Azure Virtual Network (VNet) Setup:**
   - Create a new Virtual Network in Azure to host your virtual machines (VMs) that will serve as domain controllers.
   - Define the address space and subnets for the VNet.
   - Configure network security groups (NSGs) to control inbound and outbound traffic.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. **Azure Virtual Machine Deployment:**
   - Deploy the first virtual machine that will act as the primary domain controller (DC).
   - Choose an appropriate VM size, operating system, and disk configuration.
   - Configure networking settings, including the virtual network, subnet, and public IP address.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. **AD DS Installation and Configuration:**
   - Install the Active Directory Domain Services (AD DS) role on the primary domain controller.
   - Promote the VM to a domain controller using the Directory Service Installation Wizard.
   - Configure the forest and domain functional levels, DNS, and site information.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. **Additional Domain Controllers:**
   - Deploy additional virtual machines in Azure to act as additional domain controllers for redundancy and fault tolerance.
   - Join these VMs to the domain and promote them to domain controllers.
   - Ensure proper replication between the domain controllers.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. **Networking and DNS Configuration:**
   - Configure DNS settings on the virtual machines to use the primary domain controller as the preferred DNS server.
   - Ensure proper name resolution between the on-premises environment and Azure VMs by configuring DNS forwarders and/or conditional forwarding.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. **Connectivity between On-Premises and Azure:**
   - Establish a secure connection between your on-premises network and the Azure VNet.
   - Configure a site-to-site VPN or set up an ExpressRoute circuit.
   - Ensure that the required ports and protocols are allowed through firewalls and NSGs.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. **Security and Access Control:**
   - Implement security measures, such as Azure Network Security Groups and Azure Firewall, to protect your Azure environment.
   - Configure appropriate access control for administrative accounts and group policies.
   - Implement Multi-Factor Authentication (MFA) for additional security.
   
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. **Monitoring and Maintenance:**
   - Set up monitoring and logging solutions to monitor the health and performance of your AD environment.
   - Regularly monitor replication, event logs, and domain controller status.
   - Apply regular updates and patches to keep the virtual machines and Active Directory up to date.

Remember that this is just an outline, and each step involves specific configuration details and considerations. It is recommended to refer to Azure documentation and best practices for detailed instructions and guidance during the implementation process.
