# 🛠️ Arcium Node Full Setup Guide for Ubuntu PC (Testnet + Rewards Ready)

🔋 *No token needed. Rewards via Encrypted Credits & identity.json*

---

## ✅ 1. System Update + Required Tools

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install build-essential curl git pkg-config libssl-dev docker.io docker-compose -y


---

✅ 2. Install Rust

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env


---

✅ 3. Install Arcup CLI

TARGET=x86_64_linux
curl -L "https://bin.arcium.com/download/arcup_${TARGET}_0.1.47" -o ~/.cargo/bin/arcup
chmod +x ~/.cargo/bin/arcup
arcup install


---

✅ 4. Generate Node Identity

arcup generate identity

🔐 This will create ~/.arcup/identity.json — save it safely. Future rewards are linked to this file.


---

✅ 5. Node Configuration

Create ~/.arcup/config.yaml with this content:

network: testnet
role: arx
jurisdiction: IN
node_name: Lakshay


---

✅ 6. Start the Node

arcup start


---

✅ 7. Check Status & Logs

arcup status
arcup logs


---

✅ 8. Wallet for Rewards

1. Create a Phantom Wallet: https://phantom.app


2. Save your wallet address


3. Rewards will be claimable here in future (ARX airdrop or credits)




---

✅ 9. Join Arcium Discord

Stay updated and connect your identity if needed:
🔗 https://discord.gg/arcium
