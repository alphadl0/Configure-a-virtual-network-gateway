# Azure Virtual Network Gateway Project

## 🚀 Overview
This project demonstrates how to securely connect two Azure VNets (**CoreServicesVnet** and **ManufacturingVnet**) using VPN Gateways.  
It was completed as part of the **AZ-700 Designing and Implementing Microsoft Azure Networking Solutions** lab.

---

## 🎯 Objectives
- Deploy two VNets with subnets.
- Create VMs in each VNet.
- Configure RDP access.
- Establish VNet-to-VNet connectivity via VPN Gateways.
- Verify secure communication between VMs.

---

## 🛠️ Steps Completed

### 1. Created VNets
Deployed **CoreServicesVnet** and **ManufacturingVnet** using ARM templates.  
<img width="1406" height="310" alt="image" src="https://github.com/user-attachments/assets/5649a0bb-f04d-43c5-8e70-173f63c15ea8" />


---

### 2. Deployed Virtual Machines
Created **CoreServicesVM** and **ManufacturingVM** with admin credentials.  
<img width="1929" height="360" alt="image" src="https://github.com/user-attachments/assets/882c47b3-483a-4e35-b744-27ec8806e6c4" />


---

### 3. Connecting via RDP
Downloaded RDP files and connected to each VM. Verified IPv4 addresses.  
<img width="771" height="763" alt="image" src="https://github.com/user-attachments/assets/9e6c626b-2730-4bd0-a25b-e00526796c11" />



---

### 4. Testing Initial Connectivity
Confirmed that VMs could not connect before gateways were configured.  
<img width="1618" height="438" alt="test-netconnection-fail" src="https://github.com/user-attachments/assets/b48f7bae-b201-4e62-8254-037a1ebb9b02" />



---

### 5. Created VPN Gateways
Configured **CoreServicesVnetGateway** and **ManufacturingVnetGateway** with public IPs and SKU `VpnGw1`.  
<img width="1572" height="289" alt="image" src="https://github.com/user-attachments/assets/9fd208fe-c8fd-43e1-bab1-fcecc9032f17" />


---

### 6. Establishing VNet-to-VNet Connection
Set up connections between gateways using shared key `abc123`.  
![Screenshot of connection status](screenshots/connection-status.png)

---

### 7. Final Connectivity Test
Successfully tested RDP connectivity between CoreServicesVM and ManufacturingVM.  
![Screenshot of successful ping](screenshots/ping-success.png)

---

## 📚 Key Learnings
- Azure VPN Gateway enables secure communication between VNets across regions.
- Gateway SKUs (VpnGw1, VpnGw2, etc.) affect performance and throughput.
- VNet-to-VNet is one of the main connection types alongside Site-to-Site and Point-to-Site.

---

## 🧰 Tools & Technologies
- Azure Portal  
- ARM Templates  
- PowerShell (Cloud Shell)  
- Remote Desktop Protocol (RDP)  

---

## ✅ Outcome
This project successfully demonstrated secure cross-region connectivity between two Azure VNets using VPN Gateways. It highlights practical skills in Azure networking, resource deployment, and troubleshooting.

