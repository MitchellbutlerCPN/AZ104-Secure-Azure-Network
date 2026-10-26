# Secure Azure Network Infrastructure | AZ-104 Project

## Project Overview

This project demonstrates the deployment and configuration of secure Microsoft Azure network infrastructure using Azure Resource Manager (ARM) templates and Azure PowerShell.

The objective was to gain hands-on experience with Infrastructure as Code (IaC), Azure networking, and network security controls while preparing for the Microsoft AZ-104 certification.

## Technologies Used

- Microsoft Azure
- Azure Resource Manager (ARM)
- JSON
- Azure PowerShell
- Azure Virtual Networks
- Network Security Groups (NSGs)
- Visual Studio Code

## Network Architecture

| Resource | Configuration |
|---|---|
| Resource Group | rg-az104-secure |
| Region | West US 2 |
| Virtual Network | vnet-az104-secure |
| Address Space | 10.10.0.0/16 |
| Management Subnet | snet-management |
| Subnet CIDR | 10.10.1.0/24 |
| Network Security Group | nsg-management |

## Security Configuration

Configured a Network Security Group and associated it with the management subnet.

**Inbound Security Rule**
- Name: Deny-VNet-Inbound
- Priority: 4000
- Source: VirtualNetwork
- Destination: 10.10.1.0/24
- Protocol: Any
- Action: Deny

This rule restricts inbound traffic to the management subnet from sources matched by the VirtualNetwork service tag.

## Deployment and Validation

1. Created an ARM JSON template using Microsoft's official documentation.
2. Deployed the Azure Virtual Network and management subnet.
3. Added an NSG resource with a custom inbound security rule.
4. Associated the NSG with the management subnet using ARM resource dependencies.
5. Validated the template using Azure PowerShell.
6. Previewed infrastructure changes using ARM What-If.
7. Verified the deployed resources through the Azure Portal.

## Skills Demonstrated

- Infrastructure as Code (IaC)
- Azure Resource Management
- Virtual Network and subnet configuration
- Network traffic filtering
- Azure NSG management
- ARM template validation and deployment
- Azure PowerShell administration

## Key Takeaways

This project strengthened my understanding of how Azure infrastructure can be deployed and managed through code rather than manual configuration.

I also gained experience troubleshooting JSON syntax, resolving deployment errors, configuring resource dependencies, and applying security controls to existing infrastructure.
