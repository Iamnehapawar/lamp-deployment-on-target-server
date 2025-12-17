# Create LAMP and Deploy index.html on Target Server

##  Task Statement

Create a **LAMP stack** on a **target server** and deploy a custom **index.html** file using **Ansible**.

---

##  Overview

This repository contains an Ansible-based automation that installs and configures the **LAMP stack (Linux, Apache, MariaDB, PHP)** on a remote AWS EC2 instance (target server). After successful installation, a custom `index.html` page is deployed to verify the setup.

The task demonstrates practical knowledge of **remote server automation**, **configuration management**, and **Infrastructure as Code (IaC)**.

---

##  Architecture

* **Local Machine**: Windows (PowerShell)
* **Ansible Control Node**: Amazon Linux 2023 EC2
* **Target Server**: Amazon Linux EC2
* **Automation Tool**: Ansible
* **Connectivity**: SSH using PEM key

```
Local System
    │
    ├── SCP / SSH
    │
Ansible Server (Control Node)
    │
    ├── Ansible Playbook
    │
Target Server
    │
    └── LAMP Stack + index.html
```

---

##  Prerequisites

* Ansible installed on control node
* SSH access to target server using PEM key
* Inventory file configured with target server details

---

##  What the Playbook Does

* Installs Apache, MariaDB, and PHP packages
* Starts and enables required services
* Deploys a custom `index.html` file to Apache web root
* Ensures idempotent and optimized execution

---

##  How to Run

```bash
ansible-playbook lamp_on_target.yml -i inventory.ini
```

---

##  Playbook Result

```
ok=4
changed=3
failed=0
unreachable=0
```

This confirms successful execution on the target server.

---

##  Output Verification

* Apache service running on target server
* Web page accessible via **Target Server Public IP**
* Custom index page displayed successfully

### Sample Output

```
LAMP on Target Server
Linux + Apache + MariaDB + PHP
Deployed using Ansible
Server Status : Running 
```
##  Screenshots

### 1. AWS EC2 Instance (Running State):
![](./img/servers.png)

### 2. Ansible Playbook Execution:
![](./img/run.png)

### 3. Web Output on Target Server:
![](./img/output.png)

---

##  Key Learnings

* Ansible automation on remote servers
* Inventory-based target management
* Secure SSH connectivity
* LAMP stack deployment using IaC

---

##  Conclusion

This task successfully implements **LAMP stack creation and web page deployment** on a target server using Ansible. The solution follows clean coding practices and real-world DevOps standards.

---

##  Technology Stack

AWS EC2 | Linux | Ansible | Apache | MariaDB | PH

Author: Neha Pawar

