# 🚀 AWS EC2 Static Website Deployment (Apache)

## 📌 Overview

This project demonstrates how to deploy a static website on an AWS EC2 instance using the Apache HTTP Server. It covers infrastructure setup, server configuration, and deployment workflow.

The goal is to establish a simple, scalable, and production-aligned deployment pipeline for static assets.

---

## 🧱 Tech Stack

* Cloud Provider: Amazon Web Services (EC2)
* Web Server: Apache HTTP Server
* Version Control: GitHub
* OS: Amazon Linux / Ubuntu

---

## 📁 Project Structure

```
aws-website-deploy-httpd/
│
├── index.html
├── about.html
├── contact.html
│
├── css/
│   └── styles.css
│
├── js/
│   └── script.js
│
├── images/
│   └── (assets)
│
└── README.md
```

---

## ⚙️ Deployment Steps

### 1️⃣ Launch EC2 Instance

* Create an EC2 instance (Amazon Linux / Ubuntu)
* Allow inbound traffic on:

  * Port 22 (SSH)
  * Port 80 (HTTP)

---

### 2️⃣ Connect to Instance

```bash
ssh -i your-key.pem ec2-user@your-public-ip
```

---

### 3️⃣ Install Apache

#### Ubuntu:

```bash
sudo apt update
sudo apt install apache2 -y
```

---

### 4️⃣ Start Apache Server

Ubuntu:

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

---

### 5️⃣ Clone Repository

```bash
git clone git@github.com:Anilkumar7877/aws-website-deploy-httpd.git
cd aws-website-deploy-httpd
```

---

### 6️⃣ Deploy Website Files

```bash
sudo cp -r * /var/www/html/
```

---

### 7️⃣ Verify Deployment

Open in browser:

```
http://<your-ec2-public-ip>
```

## 🧪 Troubleshooting

### ❌ Website Not Loading

* Check Apache status:

```bash
sudo systemctl status httpd
```

* Verify port 80 is open in security group

---

### ❌ Permission Denied

* Use `sudo` or update directory ownership

---

### ❌ Git Clone Authentication Error

* Use SSH instead of HTTPS
* Configure SSH keys for GitHub

---

## 📈 Key Takeaways

* Demonstrates real-world cloud deployment workflow
* Reinforces Linux permissions and server management
* Establishes foundation for DevOps practices

