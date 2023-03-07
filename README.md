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

+ https://docs.docker.com/engine/install/ubuntu/

+ follow the post install.
  
+ https://docs.docker.com/engine/install/linux-postinstall/

## Step 5. Make & Change to the /opt/mhm-stack directory 
```
cd /opt/
```
## Step 6. Pull MHM stack from github 
```
sudo git clone https://github.com/gs4162/mhm-stack.git
```

## step 7. Change permission of the directoy so the current user has full control
```
sudo chmod -R u+rwx /opt/mhm-stack
```



## Step 8. Open folder, Run docker compose configuration
```
cd /opt/mhm-stack
```
```
sudo docker compose up -d
```
## Step 9. List containers are running
```
sudo docker compose ps
```

## Step 10.. Find IP Address (eth0 ip address example 172.26.229.XXX)
```
ip addr
```
## Step 11.. Open portainer, Set password
```
http://IP.ADDRESS:9000
```
