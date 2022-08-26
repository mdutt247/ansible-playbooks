# LEMP on Ubuntu 20.04
This playbook will install a LEMP environment on an Ubuntu 20.04 machine. A virtualhost will be created with the options specified in the vars/default.yml variable file.

## Settings
* `mysql_root_password`: the password for the MySQL root account.
* `http_host`: your domain name.
* `http_conf`: the name of the configuration file that will be created within nginx.
* `http_port`: HTTP port, default is 80.

## Running this Playbook
Quick Steps:

### 1. Obtain the playbook
```
git clone https://github.com/mdutt247/ansible-playbooks.git
cd ansible-playbooks/lemp_ubuntu2004
```
### 2. Customize Options
```
nano vars/default.yml
```
```
#vars/default.yml
---
mysql_root_password: "mysql_root_password"
http_host: "your_domain"
http_conf: "your_domain.conf"
http_port: "80"
```
### 3. Run the Playbook
```
ansible-playbook -l [target] -i [inventory file] -u [remote user] playbook.yml
```
