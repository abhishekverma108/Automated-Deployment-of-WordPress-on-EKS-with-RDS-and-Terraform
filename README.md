# Automated-Deployment-of-WordPress-on-EKS-with-RDS-and-Terraform

Step 1:- Creating EKS Cluster using Terraform
I have written blog on it and try to explain every thing, check it.
https://abhishekverma109.hashnode.dev/eks-cluster-using-terraform

Step 2:- Creating RDS instance on Aws
that can be done using "rds.tf"

Step 3:- Creating Deployment 
run cmd "kubectl apply -f deployment.yml"

Step 4:- Exposing Service of type "Load Balancer"
run cmd "kubectl apply -f svc.yml"

So if you have clone this repo, then these are the following cmd that you thave to run
terraform init //this command is used to initialize a new or existing Terraform working directory. And for installing necessary plugins 
terraform plan // This command analyzes the configuration files in your working directory and generates an execution plan that outlines the changes Terraform will make                   //to your infrastructure. 

terraform apply

aws eks update-kubeconfig --name eks --region ap-south-1
kubectl apply -f deployment.yml
kubectl apply -f svc.yml
