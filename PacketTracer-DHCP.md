# 🧑‍💻 Hands-On Lab: Configuring DHCP on a Wireless Router in Cisco Packet Tracer

## 🧠 Overview

In this lab exercise, I configured a **wireless router to act as a DHCP server** in Cisco Packet Tracer and connected **three client PCs** that automatically obtained IP addresses within a custom IP range.

This simulation demonstrates practical skills in:
- Basic network setup
- DHCP configuration and troubleshooting
- IP addressing and connectivity testing

---

## 🖼️ Network Topology Setup

🛠️ **Step 1: Build the Network**

- Added **three Generic PCs** in Packet Tracer
- Connected each PC to a **wireless router’s Ethernet port** using straight-through cables

📸 *Screenshot Placeholder - Network Topology*  
`![Network Topology](images/Topology.png)`

---

## 🌐 Step 2: Observe Default DHCP Settings

- Clicked on **PC0**, went to `Desktop > IP Configuration`, and selected **DHCP** to obtain an IP address.
- Noted the **default gateway** assigned by the router.

✅ **Default Gateway:** `192.168.0.1`

📸 *Screenshot Placeholder - PC0 IP Configuration*  
`![PC0 IP Config](images/pcDHCPconfig.png)`

- Opened the web browser on PC0 and accessed the router via `192.168.0.1` (login: `admin / admin`)
- Observed default DHCP settings under **Basic Setup**.

---

## 🔧 Step 3: Change Router IP Address

- Changed router IP to `192.168.5.1`  
- Saved settings and encountered a connection error (expected behavior)
- Returned to **PC0**, selected Static > DHCP to renew IP.

📸 *Screenshot Placeholder - Changed Router IP to 192.168.5.1*  
`![Changed Router IP](images/RouterConfiguration.png)`

---

## 🛠️ Step 4: Modify DHCP Settings

Updated the DHCP configuration as follows:
- **Starting IP:** `192.168.5.126`
- **Max Users:** `75`

After saving, PC0 was renewed with the new address:
✅ **PC0 IP Address:** `192.168.5.126`

📸 *Screenshot Placeholder - DHCP New Range Configuration*  
`![New DHCP Range](images/RouterConfiguration.png)`

---

## 🖥️ Step 5: Configure DHCP on Other Clients

On **PC1**:
- Selected DHCP  
- ✅ **Assigned IP:** `192.168.5.127`

On **PC2**:
- Repeated the same DHCP steps



---

## 🧪 Step 6: Verify Network Connectivity

From **PC2**:
- Ran `ipconfig` to confirm IP
- Successfully pinged the router and PC1:

```bash
ping 192.168.5.1
ping 192.168.5.127
📸 *Screenshot Placeholder - Ping Details*  
`![Ping Details](images/Ping.png)`
