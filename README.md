Ansible role: sshd
===

[![CI](https://github.com/xenion1987/ansible-role-sshd/actions/workflows/ci.yml/badge.svg)](https://github.com/xenion1987/ansible-role-sshd/actions/workflows/ci.yml)
[![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/Xenion1987/sshd?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/Xenion1987/sshd)

Manage SSH server configuration via Ansible on Linux systems.

Requirements
---

- Min. Ansible version: 2.11

Role Variables
---

main
---

| Variable | Type | Required | Choices | Default | Description |
| --- | --- | --- | --- | --- | --- |
| `sshd_install_package` | `bool` | `false` | `true`, `false` | `true` | Ensure SSH Server is installed. |
| `sshd_package_name` | `str` | `false` | | `openssh-server` | SSH Server package name to be installed. |
| `sshd_config_path` | `str` | `false` | | `/etc/ssh/sshd_config.d` | Path to the directory where the custom SSH configurations should be stored. |
| `sshd_config_file_name` | `str` | `false` | | `sshd_config_custom.conf` | Name of the custom SSH configuration file. |
| `sshd_config_lines` | `list` | `false` | | `[]` | Name of the custom SSH configuration file. |



Dependencies
---

None

Example Playbook
---

```yaml
- name: "Play | sshd"
  hosts: all
  roles:
    - role: sshd
```

License
---

BSD, MIT

Author Information
---

Xenion1987 @ Access-InTech
