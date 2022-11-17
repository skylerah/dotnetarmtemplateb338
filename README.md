# Deploy arm template (CLI)

## Resources Created
This arm template will create the following resources
1. App Service Plan (Basic)
2. Web App (.NET Core 3.1)
3. Azure SQL Database & Server

## Steps to deploy
#### 1. Create resource group
```cli
az group create --name my-rg --location eastus
```

#### 2. Deploy arm template
```cli
az deployment group create --resource-group my-rg --parameters webAppName="appName" --template-file "path/to/file.json"
```
- if you leave out the `--parameters` option it will assign a random string