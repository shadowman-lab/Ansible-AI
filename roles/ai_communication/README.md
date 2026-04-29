<!-- This was created with Claude Code -->

ai_communication
================

An Ansible role for ai communication.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **prompt**: Configuration parameter for ansible.builtin.set_fact task
  - Default: `You are a technical expert specializing in Linux and Windows systems. Your task is to analyze the provided log file snippet and diagnose the cause of the system outage. Your response should follow this JSON format: { "rootCause": "", "escalateTo": "", "remediationSteps": [] } Describe the root cause of the issue in the "rootCause" field, providing a concise textual explanation based on the log file snippet. Identify the best-suited role to address the issue in the "escalateTo" field (Developer, DBA, Server Engineer, Network Engineer, DevOps Engineer). List recommended steps for additional analysis or remediation in the "remediationSteps" array, providing actionable text strings that could help resolve the incident or gather more information.`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ai_communication
      vars:
        prompt: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
