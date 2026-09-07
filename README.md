<div align="center">
  <h1>Ansible for HomeLabs</h1>
  <p>Automation and configuration management for my home lab infrastructure.</p>
</div>

### Overview

This repository contains Ansible inventory and playbooks for managing home lab systems, including a Raspberry Pi cluster and future Proxmox or Ubuntu hosts.

### Inventory

Example inventory shown in [`example.inventory.ini`](/example.inventory.ini).

Current groups:

- `pi_cluster`: `pi1.local` through `pi4.local`

### Tasks

* [Docker Install](./tasks/docker.yml)

### Requirements

- Ansible installed locally
- SSH access to each managed host
- Hostnames resolvable on the local network
- A user with appropriate privileges on the managed systems

### Verify Connectivity

```bash
ansible -i hosts.ini pi_cluster -m ping -u <username>
```
