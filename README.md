# keycloak_docker
Configuration for a production build in Docker compose for Keycloak + Nginx Proxy Manager
___
## Preparation
Before you  run Keycloak, you need to run Nginx Proxy Manager on your machine <img src="https://sun9-42.userapi.com/PhRgi64F_O0dDpeh6HK9U4y6YYz2HsCKe2X9kQ/TC0Tel0fVVs.jpg" width="50" height="50"/>

[**Setup Instructions**](https://nginxproxymanager.com/setup/) for Nginx Proxy Manager

## Installation
Clone the repository:
```
https://github.com/vlad-terehoff/keycloak_docker.git
```
## Usage
1. Change *keycloak.env* and *database.env*
2. Set the ip address of your machine in the nginx.conf file
   ```
   server_name xxx.xxx.x.xxx;
   ``` 
3. Run all containers:
   ```
   docker compose up -d --build
   ```
## Finally

After you up docker compose for **Keycloak** and **Nginx Proxy Manager** you need connect them together. 

![](https://github.com/vlad-terehoff/images/blob/main/docker_keycloak/step%201.png?raw=true)

**Forward Port** -> it port which you open in container

In our case 2443
```
    ports:
      - "2443:80"
```

And don't forget to set the SSL certificate

![](https://github.com/vlad-terehoff/images/blob/main/docker_keycloak/step%202.png?raw=true)
