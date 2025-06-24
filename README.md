## *How to Run Nexus Network Node on Android (Termux + Ubuntu Proot)*
A reliable method for *ARM devices* (Tested on Termux).

### *1. Install Ubuntu in Termux*
```bash
pkg install proot-distro -y
proot-distro install ubuntu
```
```bash
proot-distro login ubuntu
```
### *2. Install Nexus CLI*
```bash
apt update && apt install curl -y
curl -sSL https://cli.nexus.xyz/ | bash
source ~/.bashrc
```

### *3. Register & Start Node*
# Register wallet
```bash
nexus-network register-user --wallet-address YOUR_WALLET_ADDRESS
```
# Register node and start
```bash
nexus-network register-node && nexus-network start
```
Replace YOUR_WALLET_ADDRESS with your actual wallet (e.g., 0x206e9E56a5f886Ff1aE8a3eE744134A10A18d400).

---

### *Why This Works?*
- ✅ *Ubuntu (proot)* = Full Linux compatibility.  
- ✅ No /lib linker issues (common in Termux).  
- ✅ Optimized for *ARM phones*.  

---

🚀 *Done!* Your node is now running inside Termux.  
For long-term sessions, use tmux or screen.
