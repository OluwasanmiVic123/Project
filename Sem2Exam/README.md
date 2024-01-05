# Ansible Project

### table of content
- [Overview](#overview)
- [Requirements](#requirements)
- [Deployment Workflow](#deployment-workflow)
- [Docker Configuration](#docker-configuration)
  - [PHP Configuration (Dockerfile)](#php-configuration-dockerfile)
  - [Docker Compose Configuration](#docker-compose-configuration)
- [Conclusion](#conclusion)

### Laravel App Deployment with Ansible
This repository contains the Ansible configuration for deploying a Laravel application. It uses Ansible roles and variables to manage the deployment process.

#### Ansible Configuration Files

    ansible.cfg: Ansible configuration file that sets parameters for how Ansible will run, such as the location of the inventory file.
    hosts: Inventory file containing the list of servers where the application will be deployed. It defines the target hosts and their connection details.

#### Ansible Playbook

    deploy.yaml: Ansible playbook for deploying the Laravel application. It defines the tasks and roles to be executed during the deployment process.

#### Ansible Roles
The repository contains Ansible roles for different components of the deployment process, such as:

    common: Role for setting up common configurations and dependencies required by the Laravel application.
    nginx: Role for configuring Nginx web server settings.
    php: Role for installing PHP and its dependencies.
    mysql: Role for setting up MySQL database server and managing databases.
    laravel: Role for deploying and configuring the Laravel application.

#### Usage
To use this Ansible configuration for deploying a Laravel application, follow these steps:

    Clone this repository to your local machine.

    Update the hosts file with the target server(s) where you want to deploy the application.

    Modify the variables in the vars directory to match your application's requirements.

    Run the deploy.yaml playbook using the ansible-playbook command:

    shell

    ansible-playbook -i hosts deploy.yaml

    Replace hosts with the path to your inventory file if it's not in the current directory.

    Ansible will execute the tasks defined in the playbook, deploying your Laravel application to the specified server(s).

#### Notes

    Ensure that you have Ansible installed on your local machine before running the playbook.
    Customize the roles and variables to match your specific deployment environment and application requirements.

### Conclusion 
This README provides a brief overview of the contents of the repository and instructions for using the Ansible configuration to deploy a Laravel application. You can customize it further based on your specific deployment needs.
