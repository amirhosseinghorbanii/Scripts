# Scripts

This repository contains a collection of useful infrastructure automation and system administration scripts for various tasks, including Docker backups, Kubernetes provisioning, service configuration, and system monitoring.

## 🔧 Included Scripts

### 1. Docker Backup Script
Backup Docker container images and logs automatically.

- **Script:** `docker-backup.sh`
- **Features:**
  - Saves container images with timestamps
  - Collects container logs
  - Compresses old logs over 4MB
  - Automatically removes logs older than 3 days

### 2. Kubernetes Installation with Ansible
Provision a Kubernetes cluster (masters and workers) using an Ansible playbook.

- **Playbook:** `k8s-installation.yml`
- **Features:**
  - Disables swap and configures kernel modules
  - Installs and configures containerd
  - Adds Docker and Kubernetes repositories
  - Installs Kubernetes components: kubeadm, kubelet, kubectl
  - Holds Kubernetes packages to prevent auto-updates
  - Reboots nodes post-installation

### 3. Apache SSL Automation (Ansible)
Enable SSL for Apache, configure virtual hosts, and apply certificates.

- **Playbook:** `apache-ssl.yml`
- **Features:**
  - Enables Apache SSL module
  - Creates SSL directory
  - Copies certs from local to remote
  - Updates Apache config paths
  - Restarts Apache
  - Checks HTTPS response status

## 📦 Usage

### Docker Backup Script

```bash
chmod +x docker-backup.sh
./docker-backup.sh
```

### Ansible Playbooks

```bash
ansible-playbook -i inventory apache-ssl.yml
ansible-playbook -i inventory k8s-installation.yml
```

> Make sure to configure the `inventory` file with your host groups.

## 🧰 Requirements

- Ansible 2.9+
- Docker
- Kubernetes-compatible OS (e.g., Ubuntu 20.04+)
- Apache2 (for SSL automation)

## 📂 Structure

```
Scripts/
├── apache-ssl.yml
├── k8s-installation.yml
├── docker-backup.sh
├── README.md
└── inventory/
```

## 📜 License

MIT License

---

Feel free to contribute or fork!