# dockertest

Requirements

1. Automate deployment of EC2 instances

2. Automate the entire installation of apache and deploy a sample html file from a GitHub repository

3. Automate the entire installation of CouchDB


On Ansible Host

    1. Create a file .boto with following contents under our user home folder (~/.boto):
'''
[Credentials]
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_EY=
'''       
    2. yum install ansible | apt-get install ansible
    3. apt-get install python3-boto python-boto python3-boto3 python-boto3
    4. ansible-playbook -i hosts playbook.yml
    5. Added newly created instances to hosts file
    6. ansible-playbook -i hosts install-packages.yml
    7. ansible-playbook -i hosts run-apache-docker.yml
    8. ansible-playbook -i hosts run-couchdb-docker.yml
