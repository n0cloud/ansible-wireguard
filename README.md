# Ansible Wireguard

A simple ansible playbook to install [Wireguard](https://www.wireguard.com/) VPN / sercure overlay network.


## Requirements

 - Ansible 2.4 (or newer) installed on the machine that will run Ansible commands.
 - Jinja

## Install
You must configure the inventory file in inventory/hosts.ini
 

    git clone ...
    cd ansible-wireguard
    # Edit inventory/hosts.ini
    ansible-playbook -i inventory/hosts.ini wireguard.yml

## Verify the installation
You can get the status of Wireguard by running the following command on every hosts

    wg show
 or with ansible

    ansible -i inventory/hosts.ini -a "wg show" wireguard
