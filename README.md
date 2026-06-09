# Azure NetApp Files Cache Setup Script

## ⚠️ Disclaimer

THIS CODE IS PROVIDED AS-IS WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT.

## Overview

This PowerShell script automates the setup and configuration of Azure NetApp Files (ANF) FlexCache with cluster peering to an on-premises NetApp cluster. The script enables write-back caching using the SMB protocol and establishes peering relationships between Azure and on-premises infrastructure.

## Prerequisites

- PowerShell 5.0 or higher
- Azure CLI or Azure PowerShell modules installed
- **Az.NetAppFiles module version 1.3.0 or higher** (required for cache cmdlets)
- **Az.Accounts module** (dependency for authentication)
- Azure subscription with appropriate permissions
- Network connectivity to on-premises cluster
- SSH access to on-premises cluster

### Module Installation

```powershell
Install-Module Az -Force
Install-Module Az.NetAppFiles -Force
Get-Module -ListAvailable Az.NetAppFiles
