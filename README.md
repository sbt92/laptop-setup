# Laptop Setup
This is an Ansible Playbook to get my Debian systems up and running as quickly as possible. 
Originally created to setup my workstations it has evolved to an infra repo for my Debian systems


## Prereqs
Your created user will not have sudo access. If so its probably worth adding your user to the sudo group and restarting
```
su -
usermod -aG sudo sam
```

Once you've downloaded the repo uncomment the roles you want. e.g. Work for Work Machines. Note if a new version of Debian has released some third party repositories may not be supported yet like Docker

## Install
```
sudo apt-get update
sudo apt-get install ansible
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml --ask-become-pass
```

## What this does not do
- Install GPG Keys
- Install SSH Keys
- Install VS Codes Plugins (This is handled by the sync in VS Code when you log in)