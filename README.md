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


Example Roles
----------------

ls roles/
authorized_key  common  ssh-keygen


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
