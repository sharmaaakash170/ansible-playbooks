## 🛠️ Ansible Playbook for Beginner

![Ansible](https://img.shields.io/badge/Automation-Ansible-blue?style=flat&logo=ansible)  

### 📌 Overview  
This repository contains an **Ansible Playbook** designed to learn Ansible from scratch.

### 🚀 Features  
✅ Automated installation and configuration of [service]  
✅ Supports multiple environments (Development, Staging, Production)  
✅ Secure and customizable with environment variables  
✅ Idempotent and scalable  

---

## 🔧 Prerequisites  

Before running the playbook, ensure you have the following:  

- Ansible installed on your control node  
  ```bash
  sudo apt update && sudo apt install -y ansible
  ```
- SSH access to the target servers  
- Properly configured inventory and variables  

---

## 🚀 Usage  

### 🔹 Clone the Repository  
```bash
git clone https://github.com/sharmaaakash170/ansible-playbook.git
cd ansible-playbook
```

### 🔹 Update Inventory  
Modify `inventory/hosts.yml` to match your target servers.  

Example:  
```ini
[web]
192.168.1.10 ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
```

### 🔹 Run the Playbook  
Run the playbook against your target hosts:  
```bash
ansible-playbook -i inventory/hosts.yml playbook.yml
```

To run with a specific tag:  
```bash
ansible-playbook -i inventory/hosts.yml playbook.yml --tags "install"
```

To run in check mode (dry run):  
```bash
ansible-playbook -i inventory/hosts.yml playbook.yml --check
```

---

## 🛠️ Customization  

Modify `group_vars/all.yml` or role-specific variable files to customize configurations.  

Example `group_vars/all.yml`:  
```yaml
mysql_root_password: "your_secure_password"
app_port: 8080
```

---

## 🐛 Troubleshooting  

If you encounter issues, try:  

- Checking Ansible logs with `-vvv` (verbose mode)  
- Verifying SSH access:  
  ```bash
  ssh -i ~/.ssh/id_rsa ubuntu@your-server-ip
  ```
- Running `ansible --version` to ensure it's installed correctly  

---

## 🤝 Contributing  

Contributions are welcome! Feel free to submit a PR or open an issue.  

### 🔹 Steps to Contribute  
1. Fork this repository  
2. Create a new branch (`git checkout -b feature-branch`)  
3. Commit your changes (`git commit -m "Added new feature"`)  
4. Push to the branch (`git push origin feature-branch`)  
5. Open a Pull Request  

---

## 📜 License  

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  

---

## 🔗 Connect with Me  

📌 GitHub: [sharmaaakash170](https://github.com/sharmaaakash170)  
📌 LinkedIn: [Aakash Sharma](https://www.linkedin.com/in/aakash-sharma-8937b81aa/)  

---

