# Odoo 18 Instance Setup

## Introduction

Welcome to the setup guide for your Odoo instance using Docker Compose. This guide will walk you through the installation of essential tools and services needed to run Odoo efficiently. Make sure to follow each step carefully to ensure a smooth setup process.

## Prerequisites

Before you begin, make sure your system has the following essentials installed:

- Python3
- Git
- Nano

Update your system by running the following commands:

```bash
sudo apt update
sudo apt upgrade
```

This should also be installed 

```bash
sudo apt install docker.io
```

For Docker Compose Use these Commands.. You can change version from 1.29.2 to Some valid Version number 
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

Make Sure to version is Valid.. 


## Nginx Installation AND Configurations

```bash
sudo apt install nginx -y
```

Check Status if it is Installed Correctly

```bash
service nginx status
```

If Not Started
```bash
service nginx start
```

For Configurations of Nginx Go to Directory
```bash
cd /etc/nginx/sites-available
```

Change fileName if more servers and domains are needed in your server..
```bash
sudo nano nginx.conf
```

File Content is available in current repo 
```bash
sudo ln -s /etc/nginx/sites-available/nginx.conf /etc/nginx/sites-enabled/nginx.conf
```

Testing Nginx Config File you have configured... 
```bash
sudo nginx -t
```

It should Output like this
```bash
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
```

After successfully configuration, it is recommended to restart nginx service
```bash
sudo service nginx restart
```

Make Sure to add below line in your Odoo configurations
```bash
proxy_mode=True
```

Also Make Sure to Restart Odoo Server Docker As Well.. 

Any Question Ask me or add an Issue.. Thanks.........