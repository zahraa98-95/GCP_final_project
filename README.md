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
![Screenshot from 2023-02-21 20-29-19](https://user-images.githubusercontent.com/78254667/220429621-211f3ee5-f6bf-4d3b-8562-aa0fc057bc9f.png)
![Screenshot from 2023-02-21 20-30-37](https://user-images.githubusercontent.com/78254667/220429642-df54f65d-3189-4c49-ad31-f04198b751c7.png)

* In console_cloud_google go to Compute Engine choose vm instance & click on ssh then write this command:
1. sudo apt update
2. sudo apt-get install kubectl
3. gcloud auth login
4. sudo apt-get install google-cloud-sdk-gke-gcloud-auth-plugin
5. gcloud container clusters get-credentials private-cluster --zone us-central1-a --project zahra-project41853
![WhatsApp Image 2023-02-21 at 8 41 12 PM](https://user-images.githubusercontent.com/78254667/220431572-896ce705-e319-47a2-957d-1f31d768d72d.jpeg)

* In console_cloud_google go to Kubernetes Engine & click on Services & Ingress:
![Screenshot from 2023-02-21 17-18-39](https://user-images.githubusercontent.com/78254667/220432819-367f6021-b696-473f-8721-f35367a8b0c6.png)

* My Final Output:
![Screenshot from 2023-02-21 17-11-02](https://user-images.githubusercontent.com/78254667/220433114-721e2a62-96b4-4dc0-b8f9-b52b4d19de89.png)



