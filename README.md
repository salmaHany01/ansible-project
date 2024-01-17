# Ansible Project

This project showcases the implementation and utilization of Ansible, an open-source automation platform, through a series of hands-on labs. The labs cover various aspects of Ansible, including web server configuration, and encryption of sensitive information using Ansible Vault.



## Lab 1: Ansible Playbooks for Web Server Configuration

*Objective:*
The objective of this lab was to automate the configuration of a web server using Ansible playbooks. Specifically, the lab focused on configuring the Apache or Nginx web server, deploying a sample website, and ensuring proper security settings.

In this lab, I expanded my Ansible skills by writing playbooks, which are Ansible's configuration files used to define automation tasks. I learned how to leverage Ansible's modules to configure web servers, such as Apache or Nginx, allowing for efficient and consistent setup across multiple systems. By deploying a sample website and implementing security settings, I gained hands-on experience in automating web server configurations with Ansible.

## Lab 2: Ansible Vault

*Objective:*
The objective of this lab was to explore the use of Ansible Vault for encrypting sensitive information, such as database passwords. The lab involved incorporating the encrypted data into an Ansible playbook, thus enhancing security and protection of sensitive data during automation processes.

In this lab, I delved into Ansible Vault, a feature that provides secure storage and encryption for sensitive data used in playbooks. By encrypting sensitive information, such as database passwords, I learned how to enhance security and protect confidential data during automation operations. Incorporating the encrypted data into an Ansible playbook allowed me to automate tasks while ensuring the confidentiality of sensitive information.

These labs collectively provided me with practical experience in utilizing Ansible as an automation tool for managing and configuring systems. I gained knowledge in automating configurations, and utilizing Ansible Vault for enhanced security. 

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
