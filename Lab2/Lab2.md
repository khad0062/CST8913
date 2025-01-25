Deployment using IaaS Infrastructure
1.	Deploy Virtual Machine (Windows or Linux) in Azure as per application requirements.
2.	Flask Webserver (Install python and other dependencies.
3.	React Frontend, Postgres and manually configure can be deployed in VM. It can be deployed in a single machine or can use different or can use the docker container for each application.
4.	 Create Virtual Network along with Security groups and firewall to control inbound and outbound traffic( VNet).

 Deployment using PaaS Infrastructure
1.	Flask Web Server:
•	Service: Azure App Service
•	Fully managed platform for deploying and scaling the Flask backend.
2.	 React Frontend:
•	Service: Azure Static Web Apps
•	Hosts the static React app with automatic scaling and CI/CD integration.
3.	 PostgreSQL Database:
•	Service: Azure Database for PostgreSQL
•	Managed database service, handling scaling, backups, and patching.
4.	 Networking & Security:
•	Azure handles load balancing, scaling, and security automatically.

