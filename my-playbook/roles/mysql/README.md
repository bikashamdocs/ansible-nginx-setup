# This Ansible Role is designed to install MySQL on a target system.

This Ansible role automates the installation of MySQL on a target host. The role includes default variables, handlers, tasks, and vars files.

# Requirements 
- Ansible 2.10 or later
- Target system running Ubuntu or Debian

## Role Variables
The following default variables are used in this role:

- db_user: The MySQL user to create. Default is demo-user.
- db_pass: The password for the MySQL user. Default is demo123.
- db_name: The name of the MySQL database to create. Default is demo-db.
- mysql_version: The version of MySQL to install. Default is 8.0.

## Handlers
Handlers are used to trigger actions at the end of a play. This role includes a handler to restart the MySQL service once the installation and configuration are complete. The handler is defined in the handlers/main.yml file.

## Tasks

The main tasks for this role are defined in the tasks/main.yml file. The tasks include:

- Installing MySQL and dependencies
- Starting and enabling the MySQL service
- Creating a MySQL user with specified credentials
- Creating a new MySQL database

## Vars

The vars/main.yml file can be used to override any of the default variables in defaults/main.yml.
