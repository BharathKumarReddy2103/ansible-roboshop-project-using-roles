![Roboshop](https://github.com/BharathKumarReddy2103/Ansible-Roboshop/blob/main/robot%20shop.png)

## 📌 Project Overview

This repository is dedicated to practicing and demonstrating **Ansible Roles** using the **Roboshop** e-commerce application – a microservices-based system that simulates an online robot store.

Each component (like `catalogue`, `cart`, `user`, `payment`, `shipping`, `mongodb`, etc.) is configured and managed using **Ansible Roles**, promoting modular, reusable, and scalable automation practices.

> ✅ This project is ideal for learning infrastructure automation using Ansible with real-world microservice architecture.

---

## 🔧 Technologies Used

- **Ansible** – Configuration management and automation
- **YAML** – Declarative language for writing Ansible playbooks
- **AWS EC2** – For testing and deployment
- **Roboshop Application** – E-commerce microservices app for practice

---

## 📂 Repository Structure

```

Ansible-Roboshop-Roles/
├── inventory.ini
├── main.yaml
├── mongodb.yaml
├── mysql.yaml
├── roles/
│ ├── cart/
│ │ ├── tasks/main.yaml
│ │ ├── templates/cart.service.j2
│ │ └── vars/main.yaml
│ ├── catalogue/
│ │ ├── files/mongo.repo
│ │ ├── tasks/main.yaml
│ │ ├── templates/catalogue.service.j2
│ │ └── vars/main.yaml
│ ├── common/
│ │ └── tasks/
│ │ ├── app-setup.yaml
│ │ ├── deployment.yaml
│ │ ├── maven.yaml
│ │ ├── nodejs.yaml
│ │ ├── python.yaml
│ │ └── systemd.yaml
│ ├── user/
│ │ ├── tasks/main.yaml
│ │ ├── templates/user.service.j2
│ │ └── vars/main.yaml
│ ├── payment/
│ │ ├── tasks/main.yaml
│ │ ├── templates/payment.service.j2
│ │ └── vars/main.yaml
│ ├── shipping/
│ │ ├── tasks/main.yaml
│ │ ├── templates/shipping.service.j2
│ │ └── vars/main.yaml
│ ├── redis/
│ │ └── tasks/main.yaml
│ ├── rabbitmq/
│ │ ├── files/rabbitmq.repo
│ │ └── tasks/main.yaml
│ ├── frontend/
│ │ ├── handlers/main.yaml
│ │ ├── tasks/main.yaml
│ │ ├── templates/nginx.conf.j2
│ │ └── vars/main.yaml
│ ├── mongodb/
│ │ ├── files/mongo.repo
│ │ └── tasks/main.yaml
│ └── mysql/
│ ├── tasks/main.yaml
│ └── vars/main.yaml

````

- `roles/`: Individual roles for each microservice/component
- `inventory.ini`: Host definitions
- `main.yaml`: Base playbook with dynamic role execution
- `vault/`: Encrypted files using `ansible-vault` for secrets

---

## 🚀 How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/BharathKumarReddy2103/Ansible-Roboshop-Roles.git
cd Ansible-Roboshop-Roles
````

### 2. Run Playbook

```bash
ansible-playbook -i inventory.ini -e "component=catalogue" main.yaml
```

### 3. With Vault Encrypted Secrets

```bash
ansible-playbook -i inventory.ini mysql.yaml -e "component=mysql" --ask-vault-pass
```

---

## 📘 Learning Objectives

* Practice **Ansible role-based automation**
* Understand **microservices deployment patterns**
* Secure secrets using **Ansible Vault**
* Apply DevOps principles in a real-world **e-commerce app setup**

---

## 📢 Author

**Bharath Kumar Reddy**
Senior DevOps & DataOps Engineer
🔗 [LinkedIn](https://www.linkedin.com/in/bharath-kumar-reddy2103/) | 📁 [GitHub](https://github.com/BharathKumarReddy2103)

---

## 📌 License

This project is for educational and practice purposes. Not intended for production use.
