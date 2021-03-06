# Synapse Load Solution - Create Azure Resources
The scripts in this folder are used to build the components used in the architecture.  Each script builds only one component so you can pick and choose what is needed for your environment.    
	

## Script List 
1. 01ResourceGroupCreate.ps1 - Script to create a resource group in your Azure subscription.  
2. 02AzureSQLDBCreate.ps1 - Script to create the Azure SQL Database to store the metadata table. You will get prompted during the running of the script - that will setup/supply your SQL admin user/password. 
3. 03AzureADLSCreate.ps1 - Script to create the Azure Data Lake Storage (gen 2) to store the parquet files for loading
4. 04ADF-CreateADF.ps1 - Script to create the Azure Data Factory 
5. 05SynapseCreate.ps1 - Script to create the Azure Synapse SQL pool (formerly Azure SQL Data Warehouse)

## Variable List 
Each PowerShell script will contain a variable section at the top.  Below is a list of variables used for the PowerShell scripts in this directory and some info on each one.  Any PowerShell variable and/or json file that needs edited with your information will have the text `***Change This***`.  This will allow you to do a text search/replace for this to edit with your details.  

| Variable        | Explanation |          
| ------------- |-------------| 
| $SubscriptionName     | Subscription name to create resources | 
| $SubscriptionId      | Subscription ID |  
| $resourceGroupName | Resource group name to hold resources |
| $resourceGroupLocation | Region location for resource group (i.e. East US2) |
| $azsqlserver | Logical server name for Azure SQL Database (Your server name can contain only lowercase letters, numbers, and '-', but can't start or end with '-' or have more than 63 characters. And needs to be unique) | 
| $azsqlDB | Azure SQL DB name | 
| $edition | Edition of Azure SQL DB to create (i.e "GeneralPurpose") |
| $ComputeModel | Compute model - only options are "Provisioned" or "Serverless" |
|$ComputeGen | Compute generation (i.e. "Gen5")|

