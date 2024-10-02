
---

# MHM-stack (For Local Testing Only - Not for Production)

**Important: This stack is intended for local testing purposes only. The `.env` file contains default tokens and passwords that must be changed before production use.**

## Steps

+  Download Ubuntu / Connect via SSH (Putty on Windows)
+  Setup remote access 
+  Install Docker & Docker-compose
+ Pull mhm-stack
+ Start the containers
+ Open Portainer

## Step 1. Get Ubuntu 20.04 LTS running (Enable SSH during install).

+ If on Windows, open "Microsoft Store" on your Windows PC and install "Ubuntu 20.04.5 LTS", or visit the link below for a fresh install:

  https://ubuntu.com/download/server

## Step 2. Connect via SSH.

+ In terminal, use the following command to connect:
    ```
    ssh user@IPADDRESS
    ``` 
+  If unsuccessful, ensure OpenSSH is installed:
    ```
    ssh -V
    ```
+   If not installed, visit:

    https://linuxhint.com/enable-use-ssh-ubuntu/
    
## Step 3. Setup Tailscale for remote access.

    https://tailscale.com/kb/1039/install-ubuntu-2004/

+ Enable subnet routing for your IP range:

    https://tailscale.com/kb/1019/subnets/

## Step 4. Install Docker and Docker Compose.

+ Follow the installation guide:

    https://docs.docker.com/engine/install/ubuntu/

+ Complete post-install steps:

    https://docs.docker.com/engine/install/linux-postinstall/

## Step 5. Make and change to the /opt/mhm-stack directory:
```
cd /opt/
```
## Step 6. Pull MHM stack from GitHub:
```
sudo git clone https://github.com/gs4162/mhm-stack.git
```

## Step 7. Change directory permissions so the current user has full control:
```
sudo chmod -R u+rwx /opt/mhm-stack
```

## Step 8. Open the folder and run Docker Compose configuration:
```
cd /opt/mhm-stack
```
## Step 9. Make the current user the owner of the Node-RED folder (replace 'user' with your username):
```
sudo chown -R user:user /opt
```

```
sudo docker compose up -d
```

## Step 10. Verify containers are running:
```
sudo docker compose ps
```

## Step 11. Find IP Address (e.g., eth0 IP address like 172.26.229.XXX):
```
ip addr
```

## Step 12. Open Portainer and set the password:
```
http://IP.ADDRESS:9000
```

## Step 13. Run the entrypoint and update scripts:
```
cd /opt/mhm-stack
```

```
sudo ./update.sh 
```

```
sudo ./entrypoint.sh 
```

---

Let me know if you'd like any further modifications!
