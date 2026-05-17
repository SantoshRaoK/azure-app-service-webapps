# azure-app-service-webapps
Hands-on lab: Creating and deploying Azure Web Apps using App Service, Kudu console, deployment slots and autoscaling for AZ-104 exam preparation.
# Azure App Service - Web Apps Lab

## Objective
Deploy and manage Azure Web Apps using App Service including creating
a live web application, using Kudu console, configuring deployment
slots and autoscaling.

## Environment
- Microsoft Azure Free Account
- Resource Group: rg1
- Region: Australia East
- Subscription: Azure Subscription 1
- Web App URL: https://webapp-testing1.azurewebsites.net

## Web App Configuration

| Setting | Value |
|---------|-------|
| Web App Name | webapp-testing1 |
| Resource Group | rg1 |
| Runtime Stack | PHP 8.4 |
| Operating System | Linux |
| App Service Plan | ASP-rg1-b74c (F1: 1) |
| Pricing Tier | Free (F1) |
| Region | Australia East |
| Status | Running |

## What is Azure App Service?
Azure App Service is a fully managed Platform as a Service (PaaS) for
hosting web applications, REST APIs, and mobile backends. Unlike Virtual
Machines, App Service manages the underlying infrastructure — OS updates,
patching, scaling and security are all handled by Microsoft.

## App Service Plans

| Plan | Use Case | Cost |
|------|----------|------|
| Free (F1) | Learning and testing | Free |
| Basic (B1) | Dev and test | Low |
| Standard (S1) | Production workloads | Medium |
| Premium (P1) | High performance | Higher |

## Tasks Completed
- [x] Created Web App with Free SKU (F1 tier)
- [x] Configured PHP 8.4 runtime on Linux
- [x] Accessed Kudu console (Advanced Tool)
- [x] Created first web page using Kudu File Manager
- [x] Deployed HTML page to wwwroot directory
- [x] Verified live website at webapp-testing1.azurewebsites.net
- [ ] Configure Deployment Slots
- [ ] Swap staging slot to production
- [ ] Configure Autoscaling rules

## Screenshots

### 1. Create Web App Configuration
![Create Web App](screenshots/create-webapp.png)

### 2. Web App Deployed - Review and Create
![Deployment Review](screenshots/deployment-review.png)

### 3. Kudu Console - Advanced Tools
![Kudu Console](screenshots/kudu-console.png)

### 4. File Manager - index.php Created
![File Manager](screenshots/file-manager.png)

### 5. Live Website Running on Azure
![Live Website](screenshots/live-website.png)

### 6. Web App Overview - Running Status
![Web App Overview](screenshots/webapp-overview.png)

## Key Concepts Learned

### What is Kudu?
Kudu is the advanced tools console for Azure App Service. It provides:
- File Manager — browse and edit web app files directly
- SSH access to the container
- Log streaming
- Environment variables and app settings
- Deployment history

Access Kudu via: App Service → Advanced Tools → Go

### App Service vs Virtual Machine

| Feature | App Service | Virtual Machine |
|---------|-------------|-----------------|
| OS management | Azure manages | You manage |
| Scaling | Automatic | Manual or Scale Sets |
| Cost | Pay per plan | Pay per VM |
| Control | Limited | Full control |
| Setup time | Minutes | Longer |
| Use case | Web apps and APIs | Custom workloads |

### Deployment Slots (Coming Soon)
- Allows multiple environments — Production and Staging
- Test new version in Staging before going live
- Swap Staging to Production with zero downtime
- Only available on Standard tier and above

### Autoscaling (Coming Soon)
- Scale Out — add more instances when demand increases
- Scale In — remove instances when demand decreases
- Based on CPU, memory or custom metrics
- Configure minimum, maximum and default instances

## Key Exam Scenarios

**Scenario 1:**
You need to host a web application with minimum infrastructure
management and automatic OS patching. What should you use?
- Answer: Azure App Service Web App

**Scenario 2:**
You need to test a new version of your app before releasing to
users with zero downtime. What should you configure?
- Answer: Deployment Slots with swap operation

**Scenario 3:**
You need to access and edit files directly on your Azure Web App.
What tool do you use?
- Answer: Kudu console File Manager

**Scenario 4:**
Which App Service Plan tier is required for Deployment Slots?
- Answer: Standard (S1) tier or above — not available on Free or Basic

## Important Notes
- Free tier (F1) is completely free — perfect for learning
- Kudu URL format: https://[appname].scm.azurewebsites.net
- Web App URL format: https://[appname].azurewebsites.net
- Always delete Resource Group after lab to avoid charges
- Deployment Slots require Standard tier or above

## References
- [Azure App Service Documentation](https://learn.microsoft.com/en-us/azure/app-service/)
- [Kudu Documentation](https://github.com/projectkudu/kudu/wiki)
- [Deployment Slots](https://learn.microsoft.com/en-us/azure/app-service/deploy-staging-slots)
- [AZ-104 Study Guide](https://learn.microsoft.com/en-us/certifications/exams/az-104)
