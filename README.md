# Ansible LAMP Stack Automation

This project demonstrates automated deployment of a **LAMP stack (Linux, Apache, MySQL, PHP)** using **Ansible** and **Vagrant**.

The setup provisions multiple Ubuntu servers and configures a working PHP application that connects to a remote MySQL database.

---

## 🧠 Architecture

| Node | Role |
|----|----|
| ansible-control | Ansible control node |
| web1 | Apache + PHP |
| db1 | MySQL database |

Client → Apache (web1) → MySQL (db1)
---

## 🛠️ Technologies Used

- Ansible
- Vagrant + VirtualBox
- Ubuntu 22.04
- Apache2
- MySQL
- PHP
- Jinja2 templates

---

## 📂 Project Structure

ansible-lamp-vagrant/
├── inventory/
│   └── hosts.ini
├── group_vars/
│   └── db/
│       └── main.yml
├── playbooks/
│   └── site.yml
├── roles/
│   ├── apache/
│   ├── mysql/
│   └── php/
├── ansible.cfg
└── README.md

---

## ⚙️ How to Run

### 1️⃣ Start the VMs
```bash
vagrant up

vagrant ssh ansible-control

ansible-playbook -i inventory/hosts.ini playbooks/site.yml
## 📂 Project Structure

ansible-lamp-vagrant/
├── inventory/
│   └── hosts.ini
├── group_vars/
│   └── db/
│       └── main.yml
├── playbooks/
│   └── site.yml
├── roles/
│   ├── apache/
│   ├── mysql/
│   └── php/
├── ansible.cfg
└── README.md

---

## ⚙️ How to Run

### 1️⃣ Start the VMs
```bash
vagrant up

vagrant ssh ansible-control

ansible-playbook playbooks/site.yml


## Key Ansible Concepts Used


•	Roles for modular automation
•	Inventory grouping
•	Group variables
•	Jinja2 templates
•	Idempotent playbooks
