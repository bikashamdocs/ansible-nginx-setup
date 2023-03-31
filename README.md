# Ansible Playbook: Install Nginx on Ubuntu Local & Remote Machine
This Ansible playbook installs and configures Nginx on an Ubuntu local & Remote Machine.

# Project Structure

1. `ansible.cfg` is the configuration file for Ansible. It contains settings such as the location of the inventory file and SSH options.
2. `inventory/host.ini` is the inventory file that defines the hosts that Ansible will manage. It lists the IP addresses or domain names of the hosts and groups them into categories.
3. `roles/` is a directory that contains all the roles for the Ansible project. In this project, there's only one role named nginx.
4. `site.yml` is the main playbook that will be executed for the entire Ansible project. It includes the nginx role.
5. `group_vars` directory to store environment-specific variable values for your inventory groups. This can be useful for defining variables that are specific to certain environments, such as development, staging, and production.




# Requirements
1. Ansible 2.10 or later
2. Ubuntu operating system (tested on Ubuntu 20.04)
3. Role Variables- You can modify these Role variables in the vars/main.yml file to customize the Nginx installation.

# Dependencies
NA

# Usage

1. Clone the repository to your local machine:

```bash
git clone https://github.com/bikashamdocs/Ansible_Repo_Final.git
```
2. Change directory to the cloned repository:

```bash
cd my-playbook
```

3. Modify the inventory file prod_host.ini or dev_host.ini to specify the target host or group of hosts to install Nginx on.

4. Run the playbook to install Nginx:

```bash
ansible-playbook -i inventory/prod_host.ini site.yml --extra-vars "@group_vars/your-environment/all.yml"
```
or

```bash
ansible-playbook -i inventory/dev_host.ini site.yml --extra-vars "@group_vars/your-environment/all.yml"
```

# Using Key-Based Authentication with Ansible:

Prerequisites:
 1. A remote server that you want to manage with Ansible
 2. A user account on the remote server with sudo privileges

Step 1: Generate an SSH key pair

```bash
ssh-keygen
```
By default, this will create a 2048-bit RSA key pair in the ~/.ssh directory.

Step 2: Copy the public key to the remote server using the ssh-copy-id command:

```bash
ssh-copy-id remote_user_name@remote_server_ip_address
```
Step 3: Modify your Ansible inventory file
In your Ansible inventory file, modify the entry for the remote server to use the SSH key. Replace remote_user_name with the username of the remote user, and /path/to/private/key with the path to the private key file on your Ansible control node.


# Testing
1. This role includes a tests directory with a sample inventory and test playbook. You can run the tests using the following command:

```bash
ansible-playbook tests/test.yml -i tests/inventory
```

# License

NA


# Author Information
This role was created by Bikash.
