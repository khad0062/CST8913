# Refactoring a Legacy Application for Cloud-Native Deployment on Azure
## Task 1: Monolithic Architecture Components and Dependencies
1. Windows Server 2019 virtual machine (Azure VM) contains a monolithic web application. The application contains the frontend, which was developed using React.js, and the backend service, which is used with Node.js and the SQL server database.
2. Dependencies: Frontend directly calls backend APIs, which interact with the SQL Server database which is in the same VM.
2. Public load balancer is used to distribute the incoming traffic across the VMs, which have the same configurations. A public load balancer maps the public IP and port of incoming traffic to the private IP and port of the VM.
### Monolithic architecture Diagram
![Monlithic architecture](https://github.com/user-attachments/assets/ddadb7d0-0c8b-41a2-b79f-23748cbc8430)

## Task 2: Refactoring Strategy
### Break down the monolithic application into microservices
1. Static web page is hosted on the Azure static web apps.
2. Backend services like product-service, order-service which are written in node.js into Azure web app where we can select the runtime stack as node programming language.
3. VM-hosted SQL server is hosted in Azure SQL database.
4. Message queue system is implemented using the Azure functions.
5. Azure Monitor collects and aggregates the data from every layer and component of your system across multiple Azure and non-Azure subscriptions and tenants.
6.

## Task 3: Implement Refactoring Changes
### Step 1: Deploy the Frontend to Azure App Service
1. Push the code to the GitHub repository and Package the web application frontend (React).
2. Create an Azure static web app.
3. For the backend service use the Azure web app using the runtime stack as node programming language. One can directly deploy the services from the GitHub actions.
4. Deploy the frontend code and backend  using GitHub Actions.
### Step 2: Migrate the Database to Azure SQL Database
1. Use Azure Database Migration Service to move SQL Server to Azure SQL Database.
2. Update the connection string in the application settings.
3. Optimize indexes and performance tuning.
### Step 3: Convert Background Jobs into Azure Functions
1. Identify background processes.
2. Convert them into Azure Functions triggered by:
3. Queue Storage (Message processing).
4. Deploy functions using Azure Functions App.
### Step 4: Store Static Content and Logs in Azure Blob Storage
1. Move images, logs, and other static assets from the VM to Azure Blob Storage.
2. Update the app to retrieve assets from Blob Storage URL.
3. Use Azure Storage SDK or REST API in the application.
### Step 5: Setting up Azure AD 
1. Register the app in Azure AD and configure OAuth 2.0 authentication.
2. Update the web app to use Azure AD authentication.
3. Protect APIs with JWT tokens and Azure AD roles.
### Step 6: Monitoring & Logging (Azure Monitor) 
1. Enable Application Insights in Azure App Service for real-time telemetry.
2. Configure Log Analytics to collect application logs.
3. Set up alerts for performance issues and failures.

















