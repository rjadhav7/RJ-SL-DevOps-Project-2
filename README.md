# RJ-SL-DevOps-Project-2
# Automating Infrastructure using Terraform
# Project prerequisites: -
•	Install ansible 2.9.26 (Run ssh-keygen to generate the publick key to bootstarping)
•	Install Terraform 1.0.9 + provider registry.terraform.io/hashicorp/aws v3.62.0
•	Replace you own credential in cred.tf 
•	From your aws console create key pair named as Jenkins-key.pem to access(ssh) Jenkins-Master vm
•	Create files under your project directory as below: -
o	main.tf
o	cred.tf 
o	providers.tf
o	variables.tf
o	installJenkins.yml

Step 1: Run ssh-keygen to generate the publick key for password less authentication to install packages on remote client (Eg.Jenkins-Master)
Step 2: terraform init
Step 3: terraform plan
Step 4: terraform apply -auto-approve
In out of terraform you will get Jenminks-Master IP like http://Jenkins-MasterIP:8080
Step 5: Run ansible play book to install the Jenkins, Python3 and Java. (Eg. ansible-playbook installJenkins.yml -i inventory.txt)
In output of ansible-playbook you will get jenkins password
Your Jenkins-Master instance will be ready for configuration
