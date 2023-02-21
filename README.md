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

![Screenshot from 2023-02-21 20-20-07](https://user-images.githubusercontent.com/78254667/220427719-96fd6344-024e-49a5-9018-5a3c53f9c4bd.png)

* Build Dockerfile and push image to GCR:
1.  docker build . -t gcr.io/zahra-project41853/python-img:v3.0
2.  docker push gcr.io/zahra-project41853/python-img:v3.0


