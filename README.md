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

To check logs:
```bash
docker compose logs blockcastd
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
To restart the node after a system reboot:
 ```bash
 cd blockcast-beacon-auto && cd beacon-docker-compose
```
```bash
 docker compose up -d
 ```
This will resume your Blockcast node without resetting your keys or registration.

---
To check logs :
```bash
docker compose logs -f blockcastd
```
most variables would have successful attached to them.
and it would display online in the main site.

_____________________-___-_--__-_-_-_-_-_-_-__--___-_-_-__-_-__-_-_-_-_-_-_-_-__-_-_-__-_-_-__-_-_-_--_-__-_-_-_-_-_-_-_-
1. BACK UP YOUR PRIVATE KEY (BEFORE VPS RESET)

On your running node (phone or VPS), run:
```bash
cat ~/.blockcast/certs/gw_challenge.key
```
This is your private key.

Now do:
```bash
cp ~/.blockcast/certs/gw_challenge.key ~/gw_challenge.key
```
Then move or download gw_challenge.key to your local device or safe storage (Google Drive, USB, etc.).


---

2. RESTORE ON NEW VPS / NEW MACHINE

After setting up Docker and running the node once (docker compose up -d), stop it:

docker compose down

Then replace the auto-generated key with your backed up key:
```bash

cp gw_challenge.key ~/.blockcast/certs/gw_challenge.key
```

Restart your node:
```bash
docker compose up -d
```

You should now see the same Hardware ID when you run:
```bash

docker compose exec blockcastd blockcastd init
```

---

Important

Do not share your gw_challenge.key — it gives access to your node rewards.

If the path .blockcast/certs/ doesn’t exist after first run, just recreate it manually and drop your key in.


Credits

SAINT KHEN
Twitter: @admirkhen
GitHub: emmogrin
