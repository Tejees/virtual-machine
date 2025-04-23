# Creating a VM in Azure (via Portal) #
**Step 1:**  Sign in to the Azure Portal
Go to: https://portal.azure.com
Use your Microsoft credentials to log in.

**Step 2:** . **Navigate to Virtual Machines**

- Search for **"Virtual Machines"** in the search bar
- Click on **"Create"** > **"Azure virtual machine"**


Step 3: Configure Basics
You'll now be in the "Create a virtual machine" wizard.

Subscription: Choose your Azure subscription.

Resource Group: Select an existing one or click “Create new”.

Virtual machine name: e.g., MyVM

Region: Choose the region closest to your users (e.g., East US).

Availability options: Leave default or configure availability zones/sets.

Image: Choose the OS (e.g., Windows Server 2022, Ubuntu 22.04).

VM Architecture: Choose x64 unless you need Arm64.

Size: Click “See all sizes” to choose a VM size (e.g., Standard_B1s for basic workloads).

Administrator account:

Choose “Username” and “Password” or “SSH public key” for Linux.

Inbound ports: Select “Allow selected ports” → Choose RDP (Windows) or SSH (Linux).

Click Next: Disks >

Step 4: Disks
Choose the OS disk type (Standard HDD, SSD, or Premium SSD).

Optionally, add data disks. Click Next: Networking >

Step 5: Networking
Virtual network: Create new or select existing.

Subnet: Auto-selected if new VNet is used.

Public IP: Leave default (important if you want to access the VM remotely).

NIC network security group (NSG): Use basic, and confirm allowed ports (SSH or RDP). Click Next: Management >

Step 6: Management
Enable monitoring (Boot diagnostics, Auto-shutdown, etc.) as needed.

You can leave defaults or configure backups, identity, etc. Click Next: Advanced >

Step 7: Advanced (Optional)
Add cloud-init scripts, extensions, or custom data. Click Next: Tags >

Step 8: Tags (Optional)
Add tags to organize resources (e.g., environment: dev). Click Next: Review + create >

Step 9: Review + Create
Azure will validate your settings.

If everything looks good, click “Create”.

It may take 1–3 minutes to deploy.

✅ Access Your VM
Once deployed:

Go to the VM resource.

Note the Public IP Address.

For:

Windows: Use Remote Desktop (RDP) to connect (mstsc in Windows).

