My Ansibles (Ubuntu)
====================

Personal collection of Ansible roles developed for Ubuntu servers.

## Usage

This assumes that you have Ansible installed in your control machine.

For information related to Ansible's installation and requirements, please refer to the [Installation Docs](http://docs.ansible.com/intro_installation.html).

Once you have your own playbook defined, you can execute it with the following command:

```bash
$> ansible-playbook -i hosts playbook.yml
```

## How to define your own playbook

This repository follows the recommended **roles** based file structure in order to maximize tasks reuse and simplify playbook definition.

The first step to define your own playbook is to clone this repository into your control machine:

```bash
$> git clone https://github.com/albertico/my-ansibles-ubuntu.git
```

Three main files must be edited in order to define your own playbook details.

### Configuration File: `ansible.cfg`

The `ansible.cfg` file defines the main configuration parameters to be used during Ansible execution.  Settings such as remote user, whether to ask for password or use a certificate file, SSH settings, etc., are globally defined in the configuration file.

The order in which configuration files are processed is the following:

```
* ANSIBLE_CONFIG (an environment variable)
* ansible.cfg (in the current directory)
* .ansible.cfg (in the home directory)
* /etc/ansible/ansible.cfg
```

For details related to Ansible's configuration files and the available parameters, please refer to the [Ansible Configuration File Docs](http://docs.ansible.com/intro_configuration.html#explanation-of-values-by-section).

### Inventory File: `hosts`

The `hosts` file contains the inventory list of servers available during playbook execution.  Hosts can be individually listed or grouped.

Although the preferred practice in Ansible is actually not to store variables in the main inventory file, hosts or groups could include the definition of certain variables.

For details related to Ansible's inventory file, please refer to the [Inventory Docs](http://docs.ansible.com/intro_inventory.html).

### Playbook: `playbook.yml`

The `playbook.yml` file contains the actual list of roles (and tasks) to execute for each host or group of hosts defined in the inventory file.  As previously stated, this repository follows the recommended role-based playbook definition.

For details on general Playbook definition, please refer to the [Intro to Playbooks Docs](http://docs.ansible.com/playbooks_intro.html).

For details on Role-based Playbooks, please refer to the [Playbook Roles Docs](http://docs.ansible.com/playbooks_roles.html).

## Roles

Each role definition may include the tasks, handlers, variables and templates (among other files) that define the role's behavior and execution.  Changes could be made to a particular role, either by changing the defined variables or by extending the tasks, handlers or any other available file.

Having the roles and playbooks defined as a Git repository allows for the proper versioning of the playbook and roles definition based on your environments and requirements.

For details related to Roles structure and definition, please refer to the [Roles section](http://docs.ansible.com/playbooks_roles.html#roles) under the [Playbook Roles Docs](http://docs.ansible.com/playbooks_roles.html).

### Defined Roles

- Include list of defined roles

## Author

> **Alberto A. Colón Viera** (Albertico)

> **Web:** [alberti.co](http://alberti.co)  
> **Twitter:** [@alberti_co](https://twitter.com/alberti_co)  

## Copyright and License

Copyright © 2014-2015 [Alberto A. Colón Viera](https://github.com/albertico)

[MIT License](http://opensource.org/licenses/MIT)
