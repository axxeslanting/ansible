# Ansible config for Linux Laptops
This repository contains ansible configuration to configure Linux laptops (Ubuntu 22.04 LTS) by using ansible pull.
The default playbook configures a basic environment for everyone, additional packages for developers are available.

**default environment:**\
ansible-pull -U https://github.com/axxeslanting/ansible

**default environment + additional packages for developers:**\
ansible-pull -U https://github.com/axxeslanting/ansible -e developer=true

**NOTE:**\
openjdk-16-jdk has been superseded, it is not installed by this playbook.\
https://jdk.java.net/16/

## Requirements
**Ansible core 2.15 is needed to run certain modules, installation is done by following commands:**\
sudo apt update\
sudo apt upgrade\
sudo apt -y install software-properties-common\
sudo apt-add-repository ppa:ansible/ansible\
sudo apt update\
sudo apt install ansible

**Git is also a requirement to use ansible-pull, installation is done by following commands:**\
sudo apt install git -y