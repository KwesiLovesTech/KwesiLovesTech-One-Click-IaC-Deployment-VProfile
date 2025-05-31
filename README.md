
# 🚀 One-Click IaC Deployment Project

This project enables a **One-Click Deployment** of a complete multi-tier web application stack using **Infrastructure as Code (IaC)** principles. It leverages **Vagrant**, **VirtualBox**, and **Bash scripts** to provision and configure each tier automatically, from infrastructure setup to application deployment.

---

## 📦 Stack Components

| Tier        | Technology     | Role                      |
|-------------|----------------|---------------------------|
| Frontend    | Nginx          | Web server / Reverse proxy |
| Backend     | Tomcat         | Java Application Server    |
| Database    | MariaDB        | Relational Data Store      |
| Caching     | Memcached      | In-memory Key-Value Store  |
| Messaging   | RabbitMQ       | Message Queue Broker       |

---

## ⚙️ How It Works

All VMs are provisioned using **Vagrant**, and configurations are applied using **Bash scripts**. Each service runs in its own isolated virtual machine, mimicking a production-like environment.

---

## ▶️ Quick Start: One-Click Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/oneclick-iac-deployment.git
cd oneclick-iac-deployment
```

### 2️⃣ Launch the Full Stack

```bash
vagrant up
```

This command provisions and configures:
- `web01` – Nginx
- `app01` – Tomcat + App Deployment
- `db01` – MariaDB
- `mc01` – Memcached
- `rmq01` – RabbitMQ

Each machine will be launched and configured automatically via shell provisioning.

---

## 📁 Project Structure

```
.
├── Vagrantfile
├── scripts/
│   ├── install_nginx.sh
│   ├── install_tomcat.sh
│   ├── install_mariadb.sh
│   ├── install_memcached.sh
│   └── install_rabbitmq.sh
├── README.md
└── images/
```

---

## 🌐 Accessing the Application

Once provisioning is complete:

- **Frontend**: http://192.168.56.11  
- **Backend**: http://192.168.56.12:8080  
- **Database (MariaDB)**: Port 3306 on `db01`  
- **RabbitMQ UI**: Port 15672 on `rmq01`  
- **Memcached**: Port 11211 on `mc01`

> You can validate access by pinging each VM or visiting their respective IPs.

---

## ✅ Features

- Fully automated provisioning using Vagrant and shell scripts
- Modular Bash scripts per component
- Multi-tier architecture simulation for local DevOps labs
- Consistent naming, documentation, and service startup

---

## 🛠️ Requirements

- Vagrant
- VirtualBox
- Git
- Unix-based OS (macOS/Linux recommended)

---

## 📝 License

MIT License © 2025 Kwesi Ifeogwu

This project is built for DevOps learning, testing, and demonstration purposes. Fork and customize as needed!

---

## 🤝 Acknowledgments

Inspired by real-world enterprise stack patterns and VProfile project architecture.
