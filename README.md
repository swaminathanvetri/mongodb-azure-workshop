# MongoDB Atlas Azure App Service workshop

## 1. Creating Azure App service from Azure portal

### 1.1 Search for webapp in `Azure search panel` on the top

![Azure portal search](/assets/azportal-webapp-search.png)

### 1.2 Click on `Create` drop down and click on `WebApp`

![Create new webapp](assets/azportal-webapp-create.png)

### 1.3 Create new resource group for the `web app`

![Create New resource group](assets/azportal-webapp-new-rg.png)

### 1.4 Choose an unique name, runtime stack and OS

* Choose an unique name `prefix your name to make the DNS globally unique`
* Choose `Pubish` as `Code`
* Choose `Runtime stack` as `.NET 6(LTS)`
* Choose `Operating System` as `Linux`
* Choose `Region` as `Central India`
* Click on Deployment
![Name/Publish/Runtimestack/OS](assets/azportal-webapp-creation-name-stack-region-selection.png)

### 1.5 Choose App service plan

![Choose App Service plan](assets/azportal-webapp-appservice-plan-selection.png)

### 1.6 Choose Deployment options

* Leave the Continuous deployment as `Disable`
* Click on `Networking`

![Deployment](assets/azportal-webapp-deployment-section.png)

### 1.7 Choose Networking options

* Leave the default selection `as-is` and click `Monitoring`
![Networking](assets/azportal-webapp-networking-section.png)

### 1.8 Choose Monitoring options

* Disable `Application Insights` _Only for demo purposes_
* Click on `Tags`

    ![Monitoring](assets/azportal-webapp-monitoring-section.png)

### 1.9 Create tags

![Tags](assets/azportal-webapp-tag-section.png)

### 1.10 Review and Create

* Click on Review + Create
![Review](assets/azportal-webapp-review-page.png)

### 1.11 Monitor Deployment progress
![Monitor Deployment](assets/azportal-webapp-deployment-inprogress.png)

### 1.12 Deployment Notification

![](assets/azportal-webapp-deployment-success.png)

## 2. Setting up VS Code with Azure Tools Extension

### 2.1 Install `Azure Tools extension in VS Code`

![](assets/vscode-azuretools-installation.png)

### 2.2 Sign in to Azure

#### 2.2.1 Sign in 
![](assets/vscode-azure-signin.png)

#### 2.2.2 Pick Azure Login

![](assets/vscode-pick-az-login.png)

#### 2.2.3 Azure login confirmation in the browser

![](assets/vscode-az-login-browser-confirmation.png)

#### 2.2.4 Signed in View in `VS Code`
![](assets/vscode-signedin-subscription-view.png)

## 3. Deploying dotnet app from VSCode to Azure App service

### 3.1 Publish the dotnet app into local folder

To publish the application, Navigate to the folder from the `terminal` or `command prompt` where `.csproj` file is present  run the below command  

```dotnet publish -o /.publish```

You should see a new `publish` folder created alongside other folders which will contain the published DLLs

### 3.2 Deploy the publish folder to Azure app service

#### 3.2.1 Right click on the `publish` folder and click `Deploy to webapp`

![Right click publish](assets/vscode-webapp-publish-step1.png)

#### 3.2.2 Choose the Azure app service that was created in step `1`
![Choose web app](assets/vscode-webapp-publish-choose-webapp.png)

#### 3.2.3 Provide confirmation for deployment
![Provide confirmation](assets/vscode-webapp-publish-confirmation.png)

#### 3.2.4 Monitor the deployment progress in `output` window

* Monitor deployment
![](assets/vscode-webapp-publish-progress-output-window.png)


#### 3.2.5 Browse to the web app once deployment is done 
![](assets/vscode-webapp-publish-completion.png)

`Allow access from ALL network in MongoDB Atlas to enable access to the DB from Azure` - **ONLY for Demo purpose, this is strictly prohibited for production workloads**


# Bonus exercises

## Setting up continuous deployment from Azure Portal

## Reading the secrets from Azure Key Vault

