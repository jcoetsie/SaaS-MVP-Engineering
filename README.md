# SaaS-MVP-Engineering

Welcome in this online course on SaaS MVP Engineering.


# Assignment 4
Example Meteor Deploy Script
============================

__This project shows how to deploy a meteor app to a Linux environment.__


### Dependencies
* VirtualBox
* Vagrant 
* Ansible

### Example
Exucute the following commands to get your app running on a Vagrant 
provisioned VM.

```

sh
git clone https://github.com/Nebucom/SaaS-MVP-Engineering.git
cd SaaS-MVP-Engineering
git checkout 
vim provisioning/roles/deploy_twitter_dashboard/vars/main.yml
 -- Update with your settings
vagrant up

```