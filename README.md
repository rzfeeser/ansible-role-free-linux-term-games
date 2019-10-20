Role Name
=========

ansible-role-free-linux-term-games

Ever feel like you just need to take 10 and play some games? I sure do! This role installs (or removes) a wide assortment of free linux terminal games. In this case, 'terminal games' means games that do not have a dependency on a GUI.

Requirements
------------

This role depends on access to the apt (Debian / Ubuntu) or yum (Redhat / Centos) package installer on the host that Ansible is configuring.

Role Variables
--------------

absentorpresent: present (or absent)
    - This variable is mapped within vars/main.yml and is set to a default of present. To uninstall all games, simply add "-e absentorpresent=absent" to the end of your ansible-playbook command.

freegamesapt: []
    - a list of games available within the aptitude repository

freegamesyum: []
    - a delicious list of games available within the yum repository

Dependencies
------------

There are no additional dependencies for this role.

Example Playbook
----------------

To install games on your remote hosts, run a playbook such as the one below:

    - name: "Make some free linux terminal games {{ absentorpresent }}"
      hosts: localhost

      roles:
           - ansible-role-free-linux-term-games

To install games on your Ansible controller, run a playbook such as the one below:

    - name: "Make some free linux terminal games {{ absentorpresent }}"
      hosts: localhost
      connection: local

      roles:
           - ansible-role-free-linux-term-games

License
-------

MIT

Author Information
------------------

Author: Russell Zachary Feeser

Contact:
    email: rzfeeser@gmail.com

Profession: Trainer and Consultant

Available for:
    - Ansible
    - Ansible Module Design with Python
    - Network Automation with Python and Ansible
    - Python for API and API Design
    - Python Basics
    - OpenStack
    - 5G
    - 4G LTE
    - IP Multimedia Subsystem
    - Session Initiation Protocol
    - Playing Minecraft and StarCraft II :p
