
# Lab 01 — Ansible Windows Server Configuration

## Objective

Configure a Windows Server VM hosted on Proxmox using Ansible from a Mac control node.

## Lab Architecture

- **Hypervisor:** Proxmox VE
- **Control Node:** macOS with Ansible installed
- **Managed Node:** Windows Server VM
- **Management Protocol:** WinRM over HTTPS
- **Automation Languages:** Ansible YAML and PowerShell

## Learning Objectives

- Prepare the Mac as an Ansible control node.
- Configure secure WinRM connectivity to Windows Server.
- Create an Ansible inventory for the Windows VM.
- Verify connectivity using an Ansible playbook.
- Configure a basic Windows Server baseline.
- Install and validate IIS.
- Document verification and cleanup procedures.

## Prerequisites

- A running Windows Server VM on Proxmox.
- Network connectivity between the Mac and Windows Server.
- Administrator access to configure WinRM.
- Ansible and the required Windows collection installed on the Mac.
- WinRM credentials stored securely outside Git.

## Planned Files

```text
ansible-windows-server-lab/
├── inventory/
│   └── hosts.yml
├── playbooks/
│   ├── test-connectivity.yml
│   ├── configure-baseline.yml
│   └── install-iis.yml
├── group_vars/
│   └── windows.yml.example
├── tests/
│   └── validation.md
└── README.md
```

- `inventory/hosts.yml` — Lab-specific inventory.
- `playbooks/test-connectivity.yml` — Test WinRM connectivity.
- `playbooks/configure-baseline.yml` — Apply baseline settings.
- `playbooks/install-iis.yml` — Install IIS.
- `group_vars/windows.yml.example` — Example configuration variables.
- `tests/validation.md` — Verification checklist.

## Security

- Use WinRM over HTTPS where supported.
- Restrict firewall access to trusted management hosts.
- Never commit passwords, private keys, or unencrypted secrets.
- Use Ansible Vault or an approved secrets manager for credentials.
- Test configuration changes before applying them to additional servers.

## Status

**Initial lab structure.**

Playbooks and procedures must be tested against the target Windows Server before the lab is considered complete.
