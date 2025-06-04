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
├── roles/
│   ├── catalogue/
│   │   └── tasks/
│   │       └── main.yaml
│   ├── mongodb/
│   │   └── tasks/
│   │       └── main.yaml
│   ├── common/
│   │   ├── tasks/
│   │   │   └── main.yaml
│   │   └── templates/
│   └── ...
├── inventory.ini
├── main.yaml
├── mysql.yaml
├── vault/
│   └── secrets.yaml

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
