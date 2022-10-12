
# MHM-stack 

List

. Download Ubuntu
. Install Docker & Docker-compose
. Pull mhm-stack
. Start the containers
. Open Portainer

Step 1. 

```
Open "Microsoft Store on your windows PC" Install "Ubuntu 20.04.5 LTS"
```

Step 2. (Install docker & docker-compose) 
 
https://docs.docker.com/engine/install/ubuntu/

Step 3. Change to the /opt directory 

```
cd /opt
```

Step 4. Pull MHM stack from github 

```
git clone https://github.com/gs4162/mhm-stack.git
```
Step 5. Change to the /opt/mhm-stack directory 
```
cd /opt/mhm-stack
```
Step 6. Run docker compose configuration

```
sudo docker-compose up -d
```
Step 7. List containers are running

```
sudo docker-compose ps
```
Step 8. Find IP Address (eth0 ip address example 172.26.229.XXX)
```
ip addr
```
Step 9. Open portainer, Set password

http://IP.ADDRESS:9000

