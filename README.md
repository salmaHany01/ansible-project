# Ansible Project

This project showcases the implementation and utilization of Ansible, an open-source automation platform, through a series of hands-on labs. The labs cover various aspects of Ansible, including web server configuration, and encryption of sensitive information using Ansible Vault.



## Ansible Playbooks for Web Server Configuration using Ansible Vault

I expanded my expertise in Ansible by creating playbooks—configurations specifying automation tasks. To configure web servers Nginx, ensuring a consistent setup across various systems. Deploying a sample website and implementing security measures provided hands-on experience in automating web server configurations with Ansible.

Additionally, I explored Ansible Vault, a feature ensuring secure storage and encryption for sensitive data in playbooks. Encrypting critical information, such as database passwords, demonstrated how to bolster security and safeguard confidential data during automation. By seamlessly integrating encrypted data into an Ansible playbook, I automated tasks while maintaining the confidentiality of sensitive information.

This project provided me with practical experience in utilizing Ansible as an automation tool for managing and configuring systems. I gained knowledge in automating configurations, and utilizing Ansible Vault for enhanced security. 

## Getting Started

In this case, we are using RHEL9 Linux OS. First, install Ansible package.
```shell
$ yum install ansible
```
Second, create an inventory that contains the list of the managed hosts/ machines. Then run the ansible playbook.
```shell
$ ansible-playbook webServerPlaybook.yml
```
To create an ansible vault used to encrypt sensitive data, in this case, our database password. 
```shell
$ ansible-vault encrypt_string --vault-id vault.txt 'string-to-encrypt' --name 'variable_name'
```
This command runs a playbook that contains encrypted variables, it prompts the user to enter the vault password interactively.
```shell
$ ansible-playbook --ask-vault-pass vaultPlaybook.yml
```
