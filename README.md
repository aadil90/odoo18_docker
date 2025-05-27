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