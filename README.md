ansible Playbook template
=========

When new create playbook, git clone this repositroy

Requirements
------------

Use Ansible 2.0

Example Playbook
----------------

ls playbooks 
common.yml  init.yml

$ cat playbooks/common.yml 

- hosts: all
  roles:
    - common
    - authorized_key

Example Roles
----------------

ls roles/
authorized_key  common  ssh-keygen

Example Enviroment
----------------

$ cat enviroments/init 
[vm01]
192.168.122.222

# everything in the all
[all:children]
vm01

[all:vars]
ansible_ssh_port=22
ansible_ssh_user=ansible
ansible_ssh_pass=ansible
ansible_sudo_pass=ansible

Example Conf
----------------

ansible.cfg

How to use
----------------

1. hosts and Playbook move inventory directory
cp -p enviroments/init ./
cp -p playbooks/* ./

2. modify init file

3. ansible-playbook -i init init.yml
