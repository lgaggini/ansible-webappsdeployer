# ansible-webappsdeployer

ansible-webappsdeployer is an Ansible role to install and configure webapps on a debian based OS.

It performs: 

* creation of dedicated folder for webapps home
* deploy of source code from git and from remote archives
* installation of configuration files

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-webappsdeployer.git
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-webappsdeployer/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for webapps
  hosts: jobserver
  vars_files:
    - group_vars/webappsdeployer.yml

  roles:
    - { role: webappsdeployer, tags: ['webappsdeployer'] }
```
