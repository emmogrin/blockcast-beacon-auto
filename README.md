# SAINT KHEN's Blockcast BEACON Auto-Installer for PC and VPS 

> One-click setup script for Blockcast BEACON node  
> Built by **SAINT KHEN** — [@admirkhen](https://twitter.com/admirkhen)

---

## What It Does

This script automates:

- Cloning the official Blockcast BEACON Docker setup
- Launching the node using Docker Compose
- Generating your Hardware ID & Challenge Key
- Showing your Registration URL
- Providing full next steps for rewards setup

---

## Quick Start

Open your terminal and run:

```bash
git clone https://github.com/emmogrin/blockcast-beacon-auto.git
cd blockcast-beacon-auto
chmod +x blockcast-beacon-install.sh
./blockcast-beacon-install.sh
```

After Running the Script

1. Copy the Hardware ID, Challenge Key, and Registration URL from the terminal output.
2. Visit https:
 ```bash
 https://app.blockcast.network?referral-code=0srony
 ```

3. Register your node using the URL or manually.
 
 Keep your node online for:
6 hours to pass connectivity checks
24 hours to start earning rewards

---

Important

Docker is required. Install it first: https://www.docker.com/products/docker-desktop

Backup your private key from:
~/.blockcast/certs/gw_challenge.key

---

Credits

SAINT KHEN
Twitter: @admirkhen
GitHub: emmogrin
