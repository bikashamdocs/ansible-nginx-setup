# Ansible Playbook: Install Nginx on Ubuntu Local & Remote Machine
This Ansible playbook installs and configures Nginx on an Ubuntu local & Remote Machine.

# Role Structure

## Defaults

- `defaults/main.yml` file contains the default variables used by the Nginx role. These variables can be overridden as needed.

## Handlers

- `handlers/main.yml` file defines the handlers used by the Nginx role.

## Meta

- `meta/main.yml` file contains metadata about the Nginx role, including the author, description, and dependencies.

## Tasks

- `tasks/main.yml` file contains the tasks required to install and configure Nginx on the remote host.

## Templates

- `templates/nginx.conf.j2` file is the Jinja2 template used to generate the Nginx configuration file. The variables used in the template are defined in the defaults/main.yml file.

## Tests

- `tests/test.yml` file contains the tests used to verify the installation and configuration of Nginx.

## Vars

- `vars/main.yml` file contains the variables used to configure the Nginx server. These variables are specific to the Nginx role and are not intended to be overridden.
- 
# Requirements
1. Ansible 2.10 or later
2. Ubuntu operating system (tested on Ubuntu 20.04)
3. Role Variables- You can modify these Role variables in the vars/main.yml file to customize the Nginx installation.

# Dependencies
NA



# License

NA


# Author Information
This role was created by Bikash.
