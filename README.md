create_user
=========

Create a user and upload an ssh public key for remote authentication

Requirements
------------

No specific required Ansible
Need a default ssh public key or a specific key needs to be called out in a variable

Role Variables
--------------
#define the user you would like to create
user_name: default
#define the user state present or absent
user_state: present
#define the path to the ssh public key
ssh_key:~/.ssh/id_rsa.pub

Dependencies
------------

None


Example Playbook
----------------

---
- hosts: web
  become: yes
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: adam

         ssh_key: ~/.ssh/id_rsa.pub


License
-------

MIT

Author Information
------------------

ian.deschenes@bell.ca
