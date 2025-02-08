# AWS-Project-1
This is my first AWS project that includes all my skills and knowledge about AWS cloud gained till date. Repository contains infrastructure-as-code for setting up an AWS Virtual Private Cloud (VPC).

This project include:
 
1.	VPC Configuration :
    - VPC Creation: A dedicated VPC created to host resources, ensuring network isolation.


3.	Subnets:
   	 - 2 Public Subnets: For resources that need direct access to the internet (Bastion Host).
   	 - Private Subnets: For resources that should not be directly accessible from the internet (application servers, databases).
       

4.	Route Tables: Configured route tables to ensure proper routing of traffic:
   	- Public subnets have routes to the internet gateway.
    - Private subnets have routes to the NAT gateway for outbound internet access while remaining unreachable from the internet.
      

6.	Auto Scaling Group :
    - Created an auto-scaling group using a launch template to automatically scale EC2 instances based on load, ensuring high availability and fault tolerance.
      

8.	Bastion Host :
    - Bastion Host Deployment: A public EC2 instance that acts as a secure entry point to access private instances in the VPC.
     

10.	SSH Access:
    - Transferred the .pem key file from the local machine to the bastion host via command line.
    - Logged into the bastion host using its public IP.
    - Successfully able to access private instances within the VPC from the bastion host using SSH commands.
     

12.	Security Groups : Public Subnet Security Group:
   	- Allows inbound SSH (port 22) from a specified IP range to the bastion host.
    - Allows outbound traffic to any destination for internet access.
      

13.	Private Subnet Security Group:
    - Allows inbound SSH from the bastion host's security group, enabling secure access from the bastion to private instances.
   	- Restricts outbound traffic based on application requirements
   

15.	VPC Network Configuration :
    - NAT Gateway: Configured for the private subnets to enable outbound internet access while maintaining security.
    - DNS Resolution: Enabled for VPC to allow easy resource discovery.
