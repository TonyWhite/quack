# quack

Bash script for Duck DNS

## Features

* 🎯 Extremely lightweight for your server: lowest impact on CPU, RAM and Network
* 📉 Extremely lightweight for duckdns.org: connect to it only when your IP changes
* 🤓 Nerd friendly: `/tmp/last_ip` stores IP in plaintext
* 🔒 Privacy friendly: check the "online status" with Open DNS
* 👍 Simple IP detection with icanhazip.com
* 💪 Robust: I don't think this script needs compatibility updates (except for IPV6, than 'curl -6' is the only thing to edit)

## Setup

### 1. 📦 Install Dependencies

* wget
* curl
* cron (optional)

### 2. 📜 Install the script

Download the script directly from GitHub

```
sudo su
cd /usr/bin
wget https://raw.githubusercontent.com/TonyWhite/quack/main/quack
chmod +x quack
```

### 3. 📅 Launch with Cron (optional)

Edit cron with root

```
sudo su
crontab -e
```

Append this and save

```
* * * * * quack >/dev/null 2>&1
```

IP will be checked every minute.

## 💣 Uninstall

You are free to brutally delete this script from your machine.

```
rm /usr/bin/quack /tmp/last_ip
```

Now remove unused packages:

* wget (usually installed by default)
* curl
* cron (usually installed by default)
