# Windows Server Automation

Automation repository for managing Windows Server virtual machines
hosted on Proxmox.

## Goals

- Automate Windows Server configuration with Ansible and PowerShell.
- Manage updates, security hardening, monitoring, and maintenance.
- Use temporary WinRM access where operationally appropriate.
- Keep credentials and private keys out of source control.
- Document repeatable infrastructure and recovery procedures.

## Repository layout

- docs/       Architecture, setup guides, and runbooks
- powershell/ Windows administration scripts and modules
- ansible/    Playbooks, roles, and configuration
- winrm/      WinRM setup and cleanup
- inventory/  Environment-specific host configuration
- security/   Hardening and auditing
- patching/   Update automation
- monitoring/ Health checks and logging
- backups/    Backup scripts and validation
- scripts/    macOS, Windows, and Proxmox helpers
- tests/      Automated validation

## Security

Do not commit credentials, private keys, certificates with private keys,
or unencrypted secrets. Use Ansible Vault or an approved secrets manager.
