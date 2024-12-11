# Elasticsearch Install Role

An Ansible role to install and configure Elasticsearch on supported platforms.

## Features
- Installs Elasticsearch on Debian, Ubuntu.
- Configures Elasticsearch with customizable parameters.
- Manages Elasticsearch service for startup and runtime configuration.

## Requirements
- Ansible 2.9 or higher.
- Supported platforms:
  - **Debian-based systems:** Debian, Ubuntu.

## Role Variables
The following variables can be customized to suit your requirements:

### Defaults
Located in `defaults/main.yml`:
```yaml
# Default Elasticsearch version
elasticsearch_version: "7.17.0"
```

Exemple playbook
```yaml
# Exemple playbook
- name: Install Elasticsearch cluster
  hosts: all
  become: yes
  gather_facts: yes
  vars:
    elasticsearch_version: "8.10.1"

  roles:
  - elasticsearch_install
```

## Dependencies
None.

## License
MIT

## Author Information
This role was created by Chakib. Contributions and feedback are welcome!