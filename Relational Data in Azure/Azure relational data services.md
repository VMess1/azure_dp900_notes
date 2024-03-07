# Azure SQL services & capabilities
Azure SQL is a collective for a family of Microsoft SQL Server based DB services in Azure. Specific services are detailed below

## SQL Server on Azure Virtual Machines (VMs)
- IaaS solution
- 99.99% availability
- A VM running in Azure with an installation of SQL Server instance
- Each instance can support multiple DBs
- You manage all aspects of the server including OS, SQL Server updates, config, backups and other maintenance tasks
- Fully compatible with on-premises physical and virtualised installation
- You can scale up the platform where the SQL Server is running adding more memory, CPU power and disk space
- Best option for "lift and shift" migration of existing on-premises SQL Server installations to the cloud where you require access to OS features that are unsupported at a PaaS level

## Azure SQL Managed Instance
- PaaS solution
- 99.99% availability
- Runs a fully controllable instance of SQL Server in the cloud
- Each managed instance can support multiple DBs
- Additionally _instance pools_ can be used to share resources efficiently across smaller instances
- Managed instances depend on other Azure services including:
    - Azure Storage for backups
    - Azure Event Hubs for telemetry
    - Microsoft Entra ID for authentication
    - Azure Key Vault for Transparent Data Encryption (TDE)
    - A couple of Azure platform services that provide security and supportability features
- Near-100% compatibility with SQL Server
- Most on-premises DBs can be migrated with **Azure Database Migration service**
- Fully automated updates, backups and recovery
- Best for most cloud migration scenarios when you need minimal changes to existing applications

## Azure SQL Database
- PaaS solution
- 99.995% availability
- You can provision a _single database_ in a dedicated, managed (logical) server; or you can use an _elastic pool_ to share resources across multiple DBs & take advantage of on-demand scalability
- Supports most core DB-level capabilities of SQL Server
- Some features depended on by an on-premises application may not be available
