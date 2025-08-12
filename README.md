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


