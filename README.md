# 🛡️ Azure Network Security Automation & Risk Assessment

## Executive Summary
This project demonstrates the deployment of a cloud-based security auditing environment. 
I provisioned a dedicated "Attacker" node and "Target" node within a unified Azure 
Virtual Network (VNet) to simulate internal network threats and automate vulnerability 
discovery using custom scripting.

## Technical Stack
* **Cloud Provider:** Microsoft Azure
* **OS:** Ubuntu 24.04 LTS
* **Language:** Bash Scripting
* **Security Tools:** Nmap (Network Mapper)

## Phase 1: Infrastructure Deployment
I successfully provisioned two Linux instances in the South Africa North region. 
To ensure secure management, I configured Network Security Groups (NSG) to 
permit SSH access (Port 22) for administrative tasks.

![Azure Setup](./azure_infrastructure_setup.png)
