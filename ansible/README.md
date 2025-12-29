# AI/ML Environment Setup with Ansible

Ansible automation for setting up AI/ML development environment on localhost.

## Structure

```
ansible/
├── ansible.cfg          # Ansible configuration
├── inventory/
│   └── hosts.yml        # Inventory with localhost
├── playbooks/
│   └── setup-ml-env.yml # Main setup playbook
└── requirements.yml     # Galaxy collections/roles
```

## Prerequisites

- Ansible 2.15+
- Python 3.10+

## Usage

1. Install Ansible collections:
   ```bash
   cd ansible
   ansible-galaxy install -r requirements.yml
   ```

2. Run the playbook:
   ```bash
   ansible-playbook playbooks/setup-ml-env.yml
   ```

3. Run with sudo for system-level changes:
   ```bash
   ansible-playbook playbooks/setup-ml-env.yml --ask-become-pass
   ```
