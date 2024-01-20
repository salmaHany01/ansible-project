# Ansible-project
Welcome to the Ansible Project! This project is a comprehensive guide to implementing Ansible, an open-source automation platform. These hands-on labs cover a range of topics, from web server configuration to securing sensitive information using Ansible Vault, also yaml playbook to install sql on the managed host and create a database and new users using vault. 

**Ansible Playbooks for Web Server Configuration using Ansible Vault**

I've gained experience in Ansible by creating playbooks—configurations that specify automation tasks. The primary focus is on configuring Nginx web servers, ensuring a consistent setup across various systems through deploying a static website. 

**Ansible Playbook Setup MySQL DB, User, and Password using vault**

This Ansible playbook automates the setup of a MySQL database server. It installs the MySQL client and server, configures the root password, creates a specified database, and sets up a user with defined credentials. Easily customize your MySQL environment using variables such as root password, database name, and user credentials, using vault to encrypt database.

**Security with Ansible Vault**

Additionally, the project explores Ansible Vault, a feature ensuring secure storage and encryption for sensitive data in playbooks. The demonstration involves encrypting critical information, such as database passwords, showcasing how to safeguard confidential data during automation. 

## Getting Started
Follow these steps to get started with the Ansible Project:

Install Ansible Package:
```shell
$ yum install ansible
```
Create Inventory:
Create an inventory containing the list of managed hosts/machines.

Run Ansible Playbook:
Execute the Ansible playbook for web server configuration.
```shell
$ ansible-playbook web_server_playbook
```
Ansible Vault: Encrypt Sensitive Data:
Create an Ansible Vault to encrypt sensitive data, such as a database password.
```shell
$ ansible-vault encrypt_string --vault-id vault.txt 'string-to-encrypt' --name 'variable_name'
```
Run Ansible Playbook with Encrypted Variables:
Run a playbook containing encrypted variables, prompting the user to enter the vault password interactively.
```shell
$ ansible-playbook --ask-vault-pass vault.yml
```

## Conclusion
This project has provided practical experience in utilizing Ansible as an automation tool for managing and configuring systems. Gain knowledge in automating configurations and utilizing Ansible Vault for enhanced security. 
