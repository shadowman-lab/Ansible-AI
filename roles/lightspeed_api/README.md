<!-- This was created with Claude Code -->

lightspeed_api
==============

An Ansible role for lightspeed api.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **lightspeed_prompt**: Configuration parameter for lightspeed_api
  - Default: `Fail`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: lightspeed_api
      vars:
        lightspeed_prompt: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
