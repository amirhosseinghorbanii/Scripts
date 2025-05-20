
# 🔧 Bash and Ansible Automation Scripts

This repository contains a collection of useful scripts written in Bash and Ansible to assist with automation, monitoring, and system management.

## 📁 Contents

### 🛠 Bash Scripts

- **IP Reachability Checker**  
  Simple utility to ping an IP address and check if it's reachable.

- **Guess the Number Game**  
  A fun CLI game where the user guesses a randomly generated number.

- **Disk Space Monitor**  
  Monitors free space on mounted disks and triggers alerts when usage exceeds a critical threshold.

- **Established TCP Connections Monitor**  
  Continuously monitors and displays the number of established TCP connections in real time.

- **Memory Space Monitor (Every 5 Seconds)**  
  Logs the amount of free memory on the system every 5 seconds for health checks or long-term tracking.

### 🔐 Ansible Playbook

- **Replace SSL Certificates Automatically**  
  An Ansible playbook to:
  - Enable Apache SSL module
  - Create required directory for SSL certs
  - Copy new SSL certificate and key
  - Replace paths in Apache site config
  - Restart Apache with the updated certificates

## 📦 Usage

Clone the repository:

```bash
git clone https://github.com/amirhosseinghorbanii/Scripts.git
cd Scripts
```

Run the scripts with:

```bash
chmod +x scriptname.sh
./scriptname.sh
```

Run the Ansible playbook:

```bash
ansible-playbook replace-ssl.yml -i inventory
```

> ⚠️ **Note**: Make sure you edit your inventory file and have Ansible configured correctly for your environment.

## 📜 License

MIT License. Use freely and modify as needed.
