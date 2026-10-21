# Ambiente local

Guia para Windows + WSL2 (Ubuntu/Fedora). Em Linux/macOS, pule a parte do WSL.

## 1. WSL

```powershell
wsl --install -d Ubuntu
```

!!! warning "Use o filesystem do Linux"
    Clone os repos em `~/code`, não em `/mnt/c/...`. O I/O em `/mnt/c` é muito mais lento.

## 2. Git e GitHub CLI

```bash
sudo apt install -y git gh
gh auth login
```

## 3. Node.js (via nvm)

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
nvm install 24
corepack enable   # habilita o yarn
```

## 4. Python

```bash
sudo apt install -y python3 python3-venv
python3 -m venv .venv && source .venv/bin/activate
```

## 5. Podman

```bash
sudo apt install -y podman
podman run --rm hello-world
```
