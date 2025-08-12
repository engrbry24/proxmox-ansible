# Proxmox VM Automation with Ansible

This project automates the creation and management of virtual machines on Proxmox using Ansible.

## Features

- ✅ Create VMs with UEFI boot (OVMF)
- ✅ Q35 machine type for modern hardware emulation
- ✅ VirtIO SCSI single controller
- ✅ Attach ISO files for OS installation
- ✅ Stop/start VM management

## Prerequisites

- Ansible server with access to Proxmox host
- Python packages: `proxmoxer`, `requests`
- Ansible collection: `community.general`

```bash
# Install required packages
sudo pip3 install proxmoxer requests
ansible-galaxy collection install community.general
```
## Configuration Steps
##### Check your Proxmox settings:

```bash
ssh root@YOUR_PROXMOX_IP "pvesh get /nodes"     # Get node name
ssh root@YOUR_PROXMOX_IP "pvesh get /storage"   # Get storage names
ssh root@YOUR_PROXMOX_IP "ls /var/lib/vz/template/iso/"  # List ISOs
```

## Custom Configuration
##### Create VM with different specs:

```bash
ansible-playbook -i inventory.ini create-vm.yml -e "vm_id=110 vm_name=web-server vm_memory=4096 vm_cores=4"

