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
- Web App URL : https://webapp-testing1.azurewebsites.net/


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
<img width="956" height="531" alt="Screenshot 2026-05-17 181758" src="https://github.com/user-attachments/assets/03fadd3d-0410-414b-94a0-61c73fa7b761" />

### 2. Web App Deployed - Review and Create
<img width="959" height="533" alt="Screenshot 2026-05-17 181905" src="https://github.com/user-attachments/assets/fbd42158-3cbe-4471-b0df-49c566c7d317" />

### 3. Kudu Console - Advanced Tools
<img width="953" height="422" alt="Screenshot 2026-05-17 192455" src="https://github.com/user-attachments/assets/075a6000-816c-48ca-a135-d12bd1cd94bd" />
### 4. File Manager - index.php Created
<img width="944" height="474" alt="Screenshot 2026-05-17 192858" src="https://github.com/user-attachments/assets/95013783-7b3a-4445-b52a-cf7bbe6861db" />

### 5. Live Website Running on Azure
<img width="863" height="400" alt="Screenshot 2026-05-17 193120" src="https://github.com/user-attachments/assets/15ff92e5-5a95-4559-b135-5e390cfe0e2d" />

### 6. Web App Overview - Running Status
<img width="956" height="475" alt="Screenshot 2026-05-17 210754" src="https://github.com/user-attachments/assets/db10f502-3249-4148-b437-faa517d4f9c4" />

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
