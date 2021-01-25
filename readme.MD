# Ansible Home Lab

This is just a repo to keep documented my learning path with Ansible.
The idea is to fully automate my entire home lab setup deployment and configuration.

### Requirements

For the lab environment Im using:

 * Main Host: 
    - Ubuntu 20.04
    - Vmware Workstation (to create Targets)
    - Ansible installed

 * Target Machines:
    - Raspberry PI


### About

By default the plabook will:
 
 - Update repositories
 - Install docker
 - Start a portainer container
 - Start a  pihole container
 - Start a nodered container
 - Start a Home-assistant container
 - Install Git

You can edit/add/remove any task. 

### Inventory

Here change the machine names with yours. 

### Runing it

The following command will run the playbook called "rpi-playbook.yml" targetting the machines/devices in the file "inventory"

```sh
$ ansible-playbook rpi-playbook.yml -i inventory
```

### Todos

 - Improve roles with vars