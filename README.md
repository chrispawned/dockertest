# dockertest

Requirements

1. Automate deployment of EC2 instances

2. Automate the entire installation of apache and deploy a sample html file from a GitHub repository

3. Automate the entire installation of CouchDB

On Ansible Host

1. For Ansible to connect to our AWS account we need an IAM user. Create an IAM user and keep note of the access credentials. Create a file .boto with the above credentials under our user home folder (~/.boto):

[Credentials]   
AWS_ACCESS_KEY_ID=  
AWS_SECRET_ACCESS_EY=  

2. Install ansible using the following command

apt-get install ansible

3. Python boto package is required for using the ec2 module of ansible. Use the following command to install boto package

apt-get install python3-boto python-boto python3-boto3 python-boto3

4. Use the following command to deploy new EC2 instances

ansible-playbook -i hosts playbook.yml

5. Add newly created instances to hosts file of ansible
6. Use the following command to install packages as per requirement

ansible-playbook -i hosts install-packages.yml

7. Use the following command to run apache image of docker with files fetched from remote github repo using docker-compose

ansible-playbook -i hosts run-apache-docker.yml

8. Use the following command to run couchdb image of docker using docker-compose

ansible-playbook -i hosts run-couchdb-docker.yml

