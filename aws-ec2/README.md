# AWS resources with Ansible

## About

* [ansible aws docs](http://docs.ansible.com/ansible/guide_aws.html)
* AWS Resouces create/terminate/update
* Privisioning

## Requirements

* python >= 2.6
* [boto](https://github.com/boto/boto)

## Usage

EC2 create & Provisioning run the playbook, like this:
```
# ~/.aws/credentials
# [mimiczo]
# aws_access_key_id = xxxxx
# aws_secret_access_key = yyyyy

AWS_PROFILE=mimiczo ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i hosts site.yml
```

Provisioning for running EC2 run the playbook, like this:
```
# set target IP Address in hosts file.
# [mimiczo_ec2instances]
# x.x.x.100

ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i hosts site.yml --limit provisioning
```
