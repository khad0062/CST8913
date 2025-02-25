# Refactoring a Legacy Application for Cloud-Native Deployment on Azure
## Task 1: Monolithic Architecture Components and Dependencies
1. Windows Server 2019 virtual machine (Azure VM) contains a monolithic web application. The application contains the frontend, which was developed using React.js, and the backend service, which is used with Node.js and the SQL server database.
2. Dependencies: Frontend directly calls backend APIs, which interact with the SQL Server database which is in same VM.
2. Public load balancer is used to distribute the incoming traffic across the VMs, which have the same configurations. A public load balancer maps the public IP and port of incoming traffic to the private IP and port of the VM.
### Monolithic architecture Diagram





