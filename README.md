# 🛠️ Arcium Node Full Setup Guide for Ubuntu PC (Testnet + Rewards Ready)

🔋 *No token needed. Rewards via Encrypted Credits & identity.json*

---

## ✅ 1. System Update + Required Tools

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install build-essential curl git pkg-config libssl-dev docker.io docker-compose -y
```

---

## ✅ 2. Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

---

## ✅ 3. Install Arcup CLI

```bash
TARGET=x86_64_linux
curl -L "https://bin.arcium.com/download/arcup_${TARGET}_0.1.47" -o ~/.cargo/bin/arcup
chmod +x ~/.cargo/bin/arcup
arcup install
```

---

## ✅ 4. Generate Node Identity

```bash
arcup generate identity
```

🔐 This will create `~/.arcup/identity.json` — Save it safely. Rewards are tracked using this file.

---

## ✅ 5. Node Configuration

Create a file at `~/.arcup/config.yaml` with the following content:

```yaml
network: testnet
role: arx
jurisdiction: IN
node_name: Lakshay
```

---

## ✅ 6. Start the Node

```bash
arcup start
```

---

## ✅ 7. Check Status & Logs

```bash
arcup status
arcup logs
```

---

## ✅ 8. Phantom Wallet (For Rewards)

- Create wallet from: https://phantom.app  
- Save wallet address securely  
- This will be used to claim rewards in future

---

## ✅ 9. Join Arcium Discord

Stay updated and for announcements/rewards connection:  
👉 https://discord.gg/arcium

---

## ✅ Bonus: Restart Script

```bash
echo -e '#!/bin/bash\nsource \$HOME/.cargo/env\narcup start' > start_arcium.sh
chmod +x start_arcium.sh
./start_arcium.sh
```

---
