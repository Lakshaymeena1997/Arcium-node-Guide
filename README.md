# 🛠️ Arcium Node Full Setup Guide for Ubuntu PC (Testnet + Rewards Ready)

🔋 *No token needed. Rewards via Encrypted Credits & identity.json*

---

## ✅ 1. System Update + Required Tools

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install build-essential curl git pkg-config libssl-dev docker.io docker-compose -y

INSTALL RUST
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env

INSTALL ARCUP CLI
TARGET=x86_64_linux
curl -L "https://bin.arcium.com/download/arcup_${TARGET}_0.1.47" -o ~/.cargo/bin/arcup
chmod +x ~/.cargo/bin/arcup
arcup install
