### Ansible Personal

This directory contains Ansible playbooks for my 
personal configuration of Arch based Linux distributions.  
Inventory file is not needed becuase it's designed to by run 
on localhost.  

Functionalities:
* Install packages from Arch repositories and AUR
* Backup current system and prepare for distro hopping
* Unpack the backup onto a new system  

Extra roles and collections:
* [aur](https://github.com/kewlfft/ansible-aur)

To install, run:
```
ansible-galaxy collection install kewlfft.aur
```

To run the playbook, run:
```bash
### run all tasks with 'install' tag
ansible-playbook site.yaml -t 'install'

### run only ./tasks/pacman.yaml task
ansible-playbook site.yaml -t 'pacman'
```
