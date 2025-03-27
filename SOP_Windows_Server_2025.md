# Standard Operating Procedure: Preparing a Windows Server 2025  

**Company Name**  
MITT-NSA-W24

**Company Street Address**  
Young street 888 

**Company or Department Phone Number**  
111-222-3333 

**Version 1.0.1**  
Written by: limusiA  
Approved by: Felix  
Date: 03/26/2025  

---

## Purpose  
This SOP outlines the standardized process for preparing a Windows Server 2025 environment to ensure consistency, security, and compliance with organizational IT policies. It covers installation, configuration, networking, and security setup. The main reason for writing this SOP is to address the issue of incomplete and inconsistent installation systems within the company. The company management has requested to strengthen the completeness, uniformity, and completeness of the operating system to meet the newly established standards of the company.

---

## Application  
This document applies to:  
- IT administrators responsible for server deployment.  
- Teams requiring a new Windows Server 2025 instance for development, testing, or production.  
- Scenarios involving fresh installations or upgrades from previous versions.  

---

## Definitions  
- **Hostname**: Unique identifier for the server on the network.  
- **Static IP**: A fixed IP address assigned to the server.  
- **Domain Join**: Integrating the server into an Active Directory domain.  
- **WSUS**: Windows Server Update Services for managing updates.  

---

## Procedure Steps  

### Step 1: Pre-Installation Preparation  
1. **Hardware Requirements**:  
   - Verify server meets minimum specs:  
     - 64-bit CPU  
     - 8 GB RAM (16 GB recommended)  
     - 128 GB storage  
   - Ensure network connectivity (e.g., Ethernet cable, NIC drivers).  
2. **Software Resources**:  
   - Obtain a valid Windows Server 2025 ISO file and license key.  
   

---

### Step 2: Install Windows Server 2025  
1. Boot from the installation media.  
2. Select **Windows Server 2025 Standard/Datacenter Edition** and accept the license terms.  
3. Choose installation type: **Custom: Install Windows only (advanced)**.  
4. Format the target drive (NTFS file system) and proceed with installation.  
5. Set a strong administrator password post-installation.
6. **Warning! When selecting the installation medium for installing the operating system, the installation files may not be activated due to a short click time. Please restart the computer and press any key at the beginning of the run to activate the installation files!**

---

### Step 3: Configure Networking  
1. Assign a **static IP address**:  
   - Open **Server Manager > Local Server > Ethernet Properties**.  
   - Configure IPv4: IP address, subnet mask, default gateway, DNS servers.
   - **Warning! When setting a static IP address, it is strongly required to set the relevant configuration according to the address provided by the IT department. Setting an IP address without authorization may cause unnecessary errors!**
2. Set the **hostname**:  
   - Navigate to **System Properties > Computer Name**.  
   - Enter a unique hostname (e.g., `SRV-01`) and restart if prompted.  

---

### Step 4: Domain Join (Optional)  
1. In **System Properties**, click **Change** under *Computer Name/Domain*.  
2. Enter the domain name (e.g., `limusiA.mitt.com`) and provide domain admin credentials.  
3. Restart the server to apply changes.
4. **Warning! It is recommended to consult the IT department for help when joining a domain, as setting up the domain may cause other errors on the computer!**

---

### Step 5: Security Configuration  
1. **Enable Windows Defender Firewall**:  
   - Configure inbound/outbound rules via **Windows Security > Firewall & Network Protection**.  
2. **Install Critical Updates**:  
   - Run `Update-Windows` in PowerShell or configure **WSUS** for enterprise environments.  
3. **Disable Unused Services**:  
   - Use `services.msc` to turn off non-essential services (e.g., Print Spooler if unused).
   - Tip: Regarding firewalls, please consult with IT department personnel when updating files to update the system.

---

### Step 6: User and Permission Management  
1. Create local/user accounts via **Computer Management > Local Users and Groups**.  
2. Assign roles using **Server Manager > Manage > Add Roles and Features** (e.g., File Server, DHCP).  
3. Apply least-privilege principles to user permissions.
4. **Warning! When setting up users, groups, security groups, and related permissions, please consult the IT department for the latest terms and conditions for company permissions.**

---

### Step 7: Backup and Monitoring  
1. Configure **Windows Server Backup**:  
   - Schedule daily backups to an external drive or network location.  
2. Install monitoring tools (e.g., Nagios, PRTG) for performance tracking.  

---

## Resources  
- **Hardware**: Compatible server hardware, USB/DVD drive.  
- **Software**: Windows Server 2025 ISO, Rufus, PowerShell.  
- **Documentation**: [Microsoft Windows Server 2025 Technical Guide](https://docs.microsoft.com).  
- **Safety**: Anti-static wristband, UPS for power stability.  

---
