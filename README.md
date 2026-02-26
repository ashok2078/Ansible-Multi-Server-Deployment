# Ansible-Multi-Server-Deployment
# Automated Multi-Server Web Deployment via Ansible

This project demonstrates how to automate the deployment of a live website across multiple RedHat/CentOS nodes using **Ansible** and **GitHub**.

##  Architecture Overview
1 **Ansible Control Node:** The Master server used to manage and push configurations.
2 **Web Nodes:** - **Node 1:** 192.168.20.128
3   **Node 2:** 192.168.20.129
4 **Tech Stack:** Ansible, Git, Apache (httpd), RHEL/CentOS.

##  Key Features & Implementation
5 **Automated Provisioning:** Installs Git and Apache on multiple servers simultaneously.
6 **Continuous Deployment:** Fetches the latest code directly from this GitHub repository to `/var/www/html/`.
7 **Infrastructure as Code (IaC):** All server configurations are managed via a single `deploy.yml` playbook.
8 **Security & Fixes:** - Configured Passwordless SSH for seamless automation.
9     Handled Git "dubious ownership" security issues via `safe.directory` configuration.
10    - Optimized network access by managing Firewall and SELinux settings.

## Project Structure
```text
.
 inventory.ini        # Contains target server IPs and connection details
 deploy.yml           # Main Ansible Playbook for automation tasks
 index.html           # Source web page hosted on GitHub
