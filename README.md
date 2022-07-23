# k8s-for-ubuntu

Ansible playbook to deploy k8s for Ubuntu

Only pre-requisites to use the playbook are ansible itself and ssh access to the nodes on which you want to have the k8s cluster installed.

Currently only the first control plane node can be installed, but I'll take care of this in the "near" future.

Uses calico as the k8s cluster's network plugin.

Tested on Ubuntu 20.04.

## Usage

Create an ansible hosts file under this directory which has the IP of you chosen control plane node. Then run:

```
ansible-playbook --user <ssh-user-for-the-target-node> --private-key <private-key-file-to-access-the-target-node-for-the-chosen-user> -i hosts kubernetes-installation-playbook.yaml
```
