# Octopus - Poll Application Deployment with Ansible
This project automates the deployment of a poll application across five virtual machines using **Ansible**. The application includes a Flask web client, Redis, a Java worker, PostgreSQL, and a Node.js result web client, all managed via Ansible roles.

Find out more information about the project at [Project PDF](./B-DOP-400_octopus.pdf)

---

## 🛠 Features
- **Automated Deployment**: Deploy the poll application across five virtual machines.
- **Ansible Roles**: Modular roles for each component:
  - `base`: Installs essential packages.
  - `redis`: Installs and configures Redis.
  - `postgresql`: Installs PostgreSQL, sets up a user and schema.
  - `poll`: Deploys and runs the poll web client.
  - `worker`: Deploys and runs the worker service.
  - `result`: Deploys and runs the result web client.
- **Systemd Management**: Services are managed by `systemd` and start on boot.
- **Security**: Sensitive data is encrypted using Ansible Vault.

---

## ⚙️ Setup

1. Prepare five virtual machines with SSH access.
2. Clone this repository and set the Ansible Vault password:
   ```bash
   echo verySecretPassword > /tmp/.vault_pass
   export ANSIBLE_VAULT_PASSWORD_FILE=/tmp/.vault_pass
3. Run the playbook:
  ansible-playbook -i production playbook.yml

---

## Group:
 - Júlia Bomfá
 - Camila Grandini
