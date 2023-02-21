GCP_Final_project
- Overview:
In this project you can access web application on private standard GKE Cluster by using Terraform_files & Dockerfile.
- Infrastructure Components:
1. VPC includes ------> 2 subnets (Restricted Subnet & Management Subnet)
2.The Management Subnet includes ------>  (NAT gateway & Private VM)
3.The Restricted Subnet includes ------>  (Private standard GKE cluster)
________________________________________________________________________________
* To create infrastructure by using Terraform_files , you must write this command in a terminal:
1. terraform init
2. terrafrom apply

