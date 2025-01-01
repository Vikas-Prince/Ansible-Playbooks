# Automated Portfolio Deployment on AWS with Isolated Environment and Bastion Host using Ansible

## Overview

This project demonstrates the automated deployment of my portfolio website on AWS using **Ansible**. The infrastructure consists of a **bastion host** and **isolated private EC2 instances**. The goal is to showcase how to securely deploy and manage resources in an isolated environment using best practices for security and automation.

The setup involves:
- Creating and configuring a **bastion host** to securely access private EC2 instances.
- Provisioning **private EC2 instances** to host the portfolio website.
- Automating the entire provisioning, configuration and deployment process with **Ansible**.
- Ensuring a secure network configuration using **security groups**, **firewalld**, and **SSH key-based access**.

## Features

- **Automated Infrastructure Deployment**: All resources are provisioned automatically using **Ansible**.
- **Isolated Environment**: Private EC2 instances without direct public IPs, ensuring high security.
- **Bastion Host**: Acts as a secure gateway to access private instances via SSH.
- **Web Server Configuration**: Apache or Nginx configured to serve the portfolio.
- **Security Best Practices**: SSH access via bastion host and restricted access to private instances using security groups and firewalls.

## Architecture

The architecture consists of:
1. **Bastion Host**: A public-facing instance used as a gateway to access the private EC2 instances.
2. **Private EC2 Instances**: Two private instances running the portfolio web server, not accessible directly from the internet.
3. **HAProxy (optional)**: A load balancer configured on the bastion host to distribute traffic across the private instances.
4. **AWS Security Groups**: Fine-grained access control between the bastion host and private instances.
5. **Ansible**: Used for provisioning, configuring the web servers, deploying portfolio and managing infrastructure as code.

## Prerequisites

Before you begin, ensure you have the following:

- An **AWS account** with the necessary permissions to create EC2 instances, security groups, and other resources.
- **Ansible** installed on your local machine.
- **AWS CLI** configured with your AWS credentials.
- SSH access setup for your AWS instances.
