# Create an environment and deploy a Docker images on ec2

## Prerequisites:
 - Ansible
 - docker 
 - docker-py 
 - AWS account 
 - valid pem key in AWS

## Configure the environment
 - check group_vars/all
 - the playbooks assume usage of an ubuntu AMI, such as - ami-4b133c5d
 - the api is checked out from "https://github.com/bdpd/cpm-user-api"

## Run tasks:
 - Create the environment - `ansible-playbook -i hosts site.yml --tags "create"`
 - Deploy the code - `ansible-playbook -i hosts site.yml --tags "deploy" -u ubuntu`
 - Destroy the env - `ansible-playbook -i hosts site.yml --tags "destroy"`

