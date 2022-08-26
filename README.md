# MDITech - Ansible Playbooks
A collection of minimalist Ansible playbooks

* [LEMP on Ubuntu 20.04](https://github.com/mdutt247/ansible-playbooks/tree/main/lemp_ubuntu2004)

*you should setup a fresh server before starting.*

## Playbook Structure
The playbooks contained in this repository were created for educational purposes, and should serve as a base for you to create your own playbooks and roles.

Our playbooks follow a distinctive structure to facilitate reuse while keeping them mostly self-contained and straightforward.

This is how the `lemp` playbook is structured:

```
lemp_ubuntu2004
├── files
│   ├── info.php.j2
│   └── nginx.conf.j2
├── vars
│   └── default.yml
├── playbook.yml
└── readme.md
```

* `files/`: directory containing templates and other files required by the playbook.
* `vars/`: directory to save variable files. A default.yml var file is included by default.
* `playbook.yml`: the playbook file.
* `readme.md`: instructions and links related to this playbook.

## Getting Started
Set up your Ansible environment

### Connection Test
From your local machine or Ansible control node, run:

```
ansible all -m ping -u remote_user
```
If you're able to get a "pong" reply back from your node(s), your setup works as expected and you'll be able to run both ad-hoc commands and playbooks on your nodes, using Ansible.
