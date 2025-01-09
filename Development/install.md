# Development Environment Setup Guide

This guide provides a structured step-by-step approach to setting up my Linux development environment. It includes all essential tools and configurations to optimize your workflow.

## Table of Contents

1. [Essential Tools Installation](#essential-tools-installation)
2. [Shell & Configuration](#shell--configuration)
3. [Programming Tools](#programming-tools)
4. [Docker & Databases](#docker--databases)
5. [Final Notes](#final-notes)

---

## Essential Tools Installation

### Update and Upgrade Packages

```bash
sudo apt update && sudo apt upgrade -y
```

### Install Core Utilities

```bash
sudo apt install -y git curl ca-certificates gnupg lsb-release
```

---

## Shell & Configuration

### Installing ZSH & Oh My Zsh

```bash
sudo apt install -y zsh
chsh -s $(which zsh) # Set ZSH as default shell

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
export ZSH="$HOME/.oh-my-zsh"
```

### Setting Up Dotfiles

```bash
git clone https://github.com/ericzardo/dotfiles.git ~/.dotfiles

ln -sf ~/.dotfiles/.zshrc ~/.zshrc
ln -sf ~/.dotfiles/.gitconfig ~/.gitconfig
ln -sf ~/.dotfiles/.bashrc ~/.bashrc
```

---

## Programming Tools

### Installing Node.js & NVM

#### NVM Installation

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

#### Node.js & Yarn

```bash
nvm install 20
npm install --global yarn
```

---

## Docker & Databases

### Installing Docker

```bash
# Add Docker GPG key and repository
sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list

# Install Docker
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Add user to Docker group
sudo usermod -aG docker $USER

# Add permissions to docker
newgrp docker
```

### Running MySQL Container

```bash
docker run --name mysql-dev -e MYSQL_ROOT_PASSWORD=admin123 -d -p 3306:3306 -v mysql_data:/var/lib/mysql mysql:8.0
```

---

## Final Notes

Once you complete the steps above, your development environment will be ready. Some changes, like Docker permissions, may require restarting your terminal. Enjoy your optimized setup!

