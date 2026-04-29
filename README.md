<!-- This was created with Claude Code -->

# AI Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-AI)


This directory contains Ansible automation for ai management and operations.

## Overview

The AI automation provides playbooks and roles for managing and configuring
ai infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [ai_communication](roles/ai_communication/README.md) | Role for ai communication |
| [ai_communication_advanced](roles/ai_communication_advanced/README.md) | Role for ai communication advanced |
| [check_cpu](roles/check_cpu/README.md) | Role for check cpu |
| [check_status](roles/check_status/README.md) | Role for check status |
| [lightspeed_api](roles/lightspeed_api/README.md) | Role for lightspeed api |
| [rhai_playbook](roles/rhai_playbook/README.md) | Role for rhai playbook |
| [start_granite](roles/start_granite/README.md) | Role for start granite |
| [stop_granite](roles/stop_granite/README.md) | Role for stop granite |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| ai_communication.yml | Playbook for ai communication | localhost |
| ai_communication_advanced.yml | Playbook for ai communication advanced | localhost |
| check_cpu.yml | Playbook for check cpu | {{ vm_name }} |
| check_status.yml | Playbook for check status | {{ vm_name }} |
| lightspeed-request.yml | Playbook for lightspeed-request | localhost |
| lightspeed-response.yml | Playbook for lightspeed-response | datadog.shadowman.dev |
| redhatai_playbook.yml | Playbook for redhatai playbook | localhost |
| startmodel.yml | Playbook for startmodel | ai.shadowman.dev |
| stopmode.yml | Playbook for stopmode | ai.shadowman.dev |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run ai_communication.yml

# Run in stdout mode
ansible-navigator run ai_communication.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - ai_communication
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-AI/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
