# 🛡️ Azure-Network-Security-Automation
### Automated Network Discovery & Risk Assessment

## Executive Summary
This project demonstrates the end-to-end deployment of a dual-node security auditing environment within **Microsoft Azure**. The primary goal was to engineer a custom **Bash-based** automation suite to identify internal network vulnerabilities and categorize service risks. By simulating an internal auditor role, I established a secure Virtual Network (VNet) to perform automated discovery and risk flagging of critical management ports.

## Technical Stack
* **Cloud Provider:** Microsoft Azure
* **OS:** Ubuntu 24.04 LTS (Gen2)
* **Automation:** Bash Scripting
* **Tooling:** Nmap (Network Mapper)
* **Networking:** Azure Virtual Network (VNet), Network Security Groups (NSG)

## Project Walkthrough

### 1. Infrastructure Deployment & VNet Configuration
I provisioned two Ubuntu instances—an **Auditor** node and a **Target** node—within the **South Africa North** region. To ensure internal communication, I manually configured both nodes to reside on the same Virtual Network (`vnet-southafricanorth`), simulating an enterprise internal subnet.
* [Infrastructure Setup](https://github.com/descypherr/Azure-Network-Security-Automation/blob/main/screenshots/1_auditor_vm_deployment.png)
* [Network Adjacency Configuration](https://github.com/descypherr/Azure-Network-Security-Automation/blob/main/screenshots/2_target_vm_networking.png)



### 2. Environment Hardening & CLI Operations
Using the **Linux CLI**, I prepared the Auditor node by installing Nmap and configuring the local environment. This phase involved managing file system permissions and utilizing standard administrative commands to ensure tool integrity and execution capability.
* [CLI Environment Management](https://github.com/descypherr/Azure-Network-Security-Automation/blob/main/screenshots/3_linux_command_ops.png)

### 3. Automation Engineering (The "Net-Scan-Pro" Script)
I developed a custom Bash script, `reacon_auto.sh`, to standardize the scanning process. The script’s logic utilizes Nmap for discovery and incorporates a `grep`-based risk-weighting engine that automatically flags high-impact ports like SSH (22), HTTP (80), and RDP (3389).
* [Automation Logic Implementation](https://github.com/descypherr/Azure-Network-Security-Automation/blob/main/screenshots/4_bash_script_logic.png)

### 4. Vulnerability Assessment & Final Results
The final execution was performed using elevated root privileges (`sudo`) to ensure a comprehensive scan. The automation suite successfully identified the Target node and flagged **Port 22/TCP (SSH)** as a critical security risk for potential unauthorized access.
* [Final Success Report](https://github.com/descypherr/Azure-Network-Security-Automation/blob/main/screenshots/5_final_scan_success.png)

## Professional Takeaways
* **Cloud-Native Auditing:** Demonstrated the ability to provision and secure multi-node cloud environments for security testing.
* **DevSecOps Mindset:** Applied automation to reduce manual auditing time and increase the reliability of risk identification.
* **Privilege Management:** Practiced secure administration by managing sudo-level permissions for sensitive security tools.
