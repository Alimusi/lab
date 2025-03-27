# Standard Operating Procedure for New VM Creation on VMware vSphere 7.0

## PURPOSE OF THE DOCUMENT
This document outlines the standardized procedures for creating new virtual machines in VMware 7.0, ensuring consistency, proper configurations, and adherence to best practices.

## AUDIENCE
This document is intended for system administrators, IT, VMware administrators' team, and other team members involved in the creation of virtual machines using VMware 7.0 within the organization.

## APPROVAL TABLE

| **Version** | **Date**   | **Name**               | **Designation** |
|-------------|------------|------------------------|-----------------|
| 1.0         | yyyy-mm-dd | Jay Dixit(jay.dixit@mitt.ca)                  | Author          | 
| 1.1         | yyyy-mm-dd | Bobbi Plante(bobbi.plante@mitt.ca)            | Reviewer        |
| 1.1         | yyyy-mm-dd | Marni Russell(marni.russell@mitt.ca)          | Approver        |

---

## SCOPE/OBJECTIVES
The SOP covers the processes and guidelines for creating virtual machines in VMware 7.0, including:
1. Pre-creation planning and assessment.
2. Configuration of virtual machine settings.
3. Installation of the guest operating system.
4. Post-creation verification and testing.
5. Documentation of virtual machine details for future reference.

---

## ACCOUNTABILITY MATRIX

| **Task/Steps**               | **Responsible Person/Team** | **Emergency Contact**       | **Non-Emergency Contact**   | **Review/Approval** |
|------------------------------|-----------------------------|------------------------------|------------------------------|---------------------|
| Pre-creation Planning        | System Administrator        | Phone: Email/Distribution List     | Phone: Email/Distribution List | IT Manager          |
| Configuration of VM          | Virtualization Team         | Email: Email/Distribution List     | Email: Email/Distribution List | IT Ops Manager      |
| Installation of Guest OS     | System Administrator        | Phone: Email/Distribution List     | Phone: Email/Distribution List | IT Manager          |
| Post-creation Verification   | Quality Assurance Team      | Email: Email/Distribution List     | Email: Email/Distribution List | QA Manager          |
| Documentation                | Documentation Team          | Phone: Email/Distribution List     | Phone: Email/Distribution List | Author              |

---

## EXECUTION STEPS

### Step 1: Pre-creation Planning and Assessment
#### Step 1.1: Identify Purpose and Requirements
- Determine the specific purpose of the virtual machine (e.g., web server, database server).
- Define resource requirements such as CPU cores, RAM, disk space, and network configurations.

#### Step 1.2: Plan Resource Allocation
- Consider the host server's capacity and availability.
- Plan for CPU and memory reservations or limits as needed.
- Estimate storage requirements and select appropriate datastores.

#### Step 1.3: Communicate with Stakeholders
- Consult with relevant stakeholders to gather additional requirements.
- Discuss and confirm the virtual machine specifications with the requesting team.

---

### Step 2: Configuration of Virtual Machine
#### Step 2.1: Access VMware vSphere Client
   - Launch the vSphere Client and connect to the vCenter Server.
   - Create a New Virtual Machine:
   - Navigate to the target host or cluster.
   - Right-click and select **"New Virtual Machine"**.
   - Choose a deployment option (e.g., OVF template or new VM).

#### Step 2.2: Configure Virtual Machine Settings
- Specify a name and location for the virtual machine.
- Select the guest operating system and version.
- Set CPU and memory allocation based on the pre-defined plan.
- Configure network settings and attach to the appropriate network.
- Allocate disk space and choose storage policies.

---

### Step 3: Installation of Guest OS
#### Step 3.1: Attach Installation ISO
- Mount the ISO file containing the guest OS installation media.
- Configure the virtual machine to boot from the attached ISO.

#### Step 3.2: Install Guest OS
- Power on the virtual machine.
- Follow the standard installation process for the selected OS.
- Configure regional settings, administrator credentials, and other parameters.

#### Step 3.3: Configure Networking
- Set up networking within the guest OS.
- Apply IP configurations and DNS settings (static or DHCP).

---

### Step 4: Post-creation Verification and Testing
#### Step 4.1: Verify Installation
- Confirm guest OS installation success.
- Check availability of essential services and applications.

#### Step 4.2: Functional Testing
- Perform functional tests to validate operations.
- Test network connectivity (internal and external).

#### Step 4.3: Security Compliance
- Validate compliance with organizational security policies.
- Apply necessary security measures (e.g., firewall rules).

---

### Step 5: Documentation of Virtual Machine
#### Step 5.1: Document Virtual Machine Details
- Record configurations, settings, and allocated resources.
- Update system documentation with new VM information.

#### Step 5.2: Knowledge Transfer
- Provide access and management details to relevant teams.
- Share documentation via shared drives or wikis.

---

## REVISION HISTORY

| **Version** | **Date**       | **Changes By**      | **Summary of Changes**              |
|-------------|----------------|---------------------|--------------------------------------|
| 1.0         | yyyy-mm-dd     | Jay Dixit           | Initial Release of Document          |
| 1.1         | yyyy-mm-dd     | Bobbi Plante        | Updated Approval Matrix              |
| 1.2         | yyyy-mm-dd     | Marni Russell       | Added Security Compliance Section    |
