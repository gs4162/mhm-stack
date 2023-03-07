# MHM-stack 

## Steps

+  Download Ubuntu / Connent via SSH (Putty on windows)
+  Setup remote access 
+  Install Docker & Docker-compose
+ Pull mhm-stack
+ Start the containers
+ Open Portainer

##  Step 1. Get ubuntu 20.04 lts running(Enable SSH during install).


+ If windows, Open "Microsoft Store on your windows PC" Install "Ubuntu 20.04.5 LTS", Fresh install visit below link

  https://ubuntu.com/download/server

## Step 2. Connect via ssh.

+ In teminal go to.
    ```
    ssh user@IPADDRESS
    ``` 
+  If unsuccessful ensure Open-SSH is   installed.
    ```
    ssh -V
    ```
+   If in not installed visit.


    https://linuxhint.com/enable-use-ssh-ubuntu/
    
## Step 3. Setup tailscale for remote access.

    https://tailscale.com/kb/1039/install-ubuntu-2004/

+ Enable subroute for IP range.

    https://tailscale.com/kb/1019/subnets/

## step 4. Install Docker/Docker compose.

https://docs.docker.com/engine/install/ubuntu/

+ follow the post install.

https://docs.docker.com/engine/install/linux-postinstall/
## step 5. Change to the /opt directory 

```
cd /opt
```
## step 6. Change permission of the directoy so the current user has full control
```
chmod -R u+rwx /opt/mhm-stack
```


## Step 7. Pull MHM stack from github 
```
sudo git clone https://github.com/gs4162/mhm-stack.git
```
## Step 8.Make & Change to the /opt/mhm-stack directory 
```
sudo mkdir /opt/mhm-stack
```
```

cd /opt/mhm-stack
```
## Step 9. Run docker compose configuration
```
sudo docker compose up -d
```
## Step 10. List containers are running
```
sudo docker compose ps
```

## Step 11.. Find IP Address (eth0 ip address example 172.26.229.XXX)
```
ip addr
```
## Step 12.. Open portainer, Set password
```
http://IP.ADDRESS:9000
```
