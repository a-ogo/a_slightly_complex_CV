# Ansible Repository Structure

This directory contains the Ansible configuration for managing infrastructure components.

## Directory Structure

- **inventories/**: Contains inventory files for different environments
  - **production/**: Production environment inventory
  - **staging/**: Staging environment inventory
  
- **roles/**: Contains all Ansible roles
  - **web/**: Web server configuration
  - **linux/**: Linux base configuration
  - **monitoring/**: Monitoring tools configuration
  - **backup/**: Backup system configuration
  - **docker/**: Docker installation and configuration
  - **jenkins/**: Jenkins CI/CD configuration
  - **wazuh/**: Wazuh security monitoring configuration

- **playbooks/**: Contains all playbooks
  - **site.yml**: Main playbook that includes all other playbooks
  - **[component].yml**: Individual component playbooks

- **group_vars/**: Variables for groups of hosts

## Usage

To run the main playbook:

bash
ansible-playbook -i inventories/production playbooks/
site.yml

To run a specific component playbook:

bash
ansible-playbook -i inventories/production playbooks/
web.yml
