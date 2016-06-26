# Ansible Examples
This repository contains examples and best practices for building Ansible Playbooks.

## Ansible for OS X

```
brew update
brew install ansible
```

## Ansible for Ubuntu

```
sudo apt-get update
sudo apt-get install ansible
```

## Configuration

```
# Ansible Custom hosts file
custom_path/hosts

# file
[all_servers:vars]
ansible_ssh_private_key_file=~/.ssh/keypair.pem
ansible_ssh_user=ubuntu

[example]
x.x.x.100
```

## Test

```
#all PING
ansible all -m ping -i ../custom_path/hosts

#group PING
ansible example -m ping -i ../custom_path/hosts
```
