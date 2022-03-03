# PremiumV2 VM Template

This is a basic arm template to create a zonal Premium VM by attaching a PremiumV2_LRS managed data disk.
The VM gets created in the location in which the Resource Group is present.

## Usage

Login to the sub and create an resource group in the required region and a zonal PremiumV2_LRS data disk ([datadisk Template](https://github.com/PushyaragY/armTemplates/blob/main/PremiumV2ArmTemplate.json)).
Update the datadisk Id in the vm's template.json
Then Invoke the following
```powershell
    New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateFile  "template.json" -TemplateParameterFile  "parameters.json" -Verbose
```