# Ansible

The goal of this repository is to provide a bunch of ansible scripts

There is the list all of ansible scripts that this repository contains :

| Ansible script | Description |
|----------------|-------------|
| Basic packages | Install next packages : vim, htop |
| Docker | Install docker package |
| Unattended upgrades | Install unattended-upgrades package |
| Kubernetes | Install kubernetes cluster with kubeadm |

## How to use

### Inventory

---

You need to create an **inventory.yml** file. This file will contain informations about where you want to execute ansible scipts

If you want to execute it on you local machine :

```
localhost ansible_connection=local
```

If you want to execute it on a remote machine :

```
test-machine ansible_host=192.0.2.50
```

### Playbook

---

Then you need to create a **playbook.yml** file. This file will contain informations about which ansible scripts you want to run

```
- hosts: all
  become: true
  roles:
    - script-1
    - script-2
```