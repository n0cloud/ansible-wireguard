# Ansible Wireguard

A simple ansible playbook to install [Wireguard](https://www.wireguard.com/) VPN / sercure overlay network.

## Todo
 - Add support for OS other then Debian
 - Use python-netaddr to generate private Ips

## Requirements

 - Ansible 2.4 (or newer) installed on the machine that will run Ansible commands.
 - Jinja

## Install
You must configure the inventory file in inventory/hosts.ini
 

    git clone https://github.com/N0Cloud/ansible-wireguard.git
    cd ansible-wireguard
    # Edit inventory/hosts.ini
    ansible-playbook -i inventory/hosts.ini wireguard.yml

## Verify the installation
You can get the status of Wireguard by running the following command on every hosts

    wg show
 or with ansible

    ansible -i inventory/hosts.ini -a "wg show" wireguard

## Resources
For more information go to [Wireguard documentation](https://www.wireguard.com/quickstart/).
