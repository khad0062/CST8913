# Lab 3: Advanced Concept
## Section1: On-premises solution Design

![On-permises Architecture](https://github.com/user-attachments/assets/6a1f9621-ae0d-45f3-a827-1d41044bb7ed)

On-premises solution design includes:
1. Physical host or server: It consists of the web application hosted and its installation files, libraries, and files with load balancers.
2. Networking: Routers to connect the internet, and access the web applications, servers, and email service. A firewall is  used to protect against malicious attacks.
3. File storage: Local File system to store documents, images, and videos for products.
4. Email Services: On-premises mail server (e.g., Postfix) for client notifications.
5. Blackened database: Use of dedicated hardware for Microsoft SQL server.

Dependencies:
Web application connects database with SQL server to store, manage, and retrieve the data.
Networking helps to connect and secure all the components in the on-premises architecture.
Web app connects to email service for order confirmations through API.


## Section 2: Migration Strategies
Migration strategy plan for each component.
Web application Migration
Plan to migrate to PaaS (AWS Elastic Beanstalk)
1. We can refactor the web application using docker and simply deploy to AWS Elastic Beanstalk which automatically handles 
the details of capacity provisioning, load balancing, scaling, and application health monitoring.

Database Migration
Plan to migrate to AWS IaaS (EC2 instance) using Rehost migration type.
1. At first, backup server. Then, create the EC2 instance based on the requirements.
2. Deploy the instance in a virtual private cloud and subnet. Install the Microsoft SQL server in the instance.
3. Migrate the data using the AWS Data Migration service.


Local file system.
Plan to migrate to AWS IaaS (Amazon EBS (Elastic Block Store))
1. Use of lift and shift migration without change in the design.
2. Use rsync, Robocopy, or AWS DataSync to copy files to EBS.

Networking
Plan to migrate to AWS cloud-native VPC.
1. Use of VPC, subnet, security group, and Network ACLs.
2. Create VPC for the Web application, database and Local file system. Allowing web application service, port to exposed to internet.

Email service:
Plan to migrate to SaaS (Amazon WorkMail)
1. Purchase the SaaS service and deploy with change in the domain and DNS access.


