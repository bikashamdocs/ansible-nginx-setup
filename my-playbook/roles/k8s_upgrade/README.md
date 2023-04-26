# Ansible Role to upgrade a kubernetes cluster
This repository contains an Ansible playbook for upgrading a Kubernetes cluster. The playbook is designed to work with kubeadm and assumes that you have a Kubernetes cluster already set up and running.

## Directory Structure
- `k8s_upgrade/default/main.yml`: Default variables for the playbook.
- `k8s_upgrade/tasks/main.yml`: The main playbook, which includes tasks for upgrading the control plane and worker nodes.
- `k8s_upgrade/tasks/upgrade-control-plane.yml`: Tasks for upgrading the Kubernetes control plane.
- `k8s_upgrade/tasks/upgrade-worker-nodes.yml`: Tasks for upgrading the worker nodes.
- `k8s_upgrade/vars/main.yml`: Variables used by the playbook.


