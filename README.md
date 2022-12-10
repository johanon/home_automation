# Home automation  
Including 
- Nodered, Influx, Grafana
- Telldus Tellstick  
- Oregon temperature sensors
- Tibber 

# Telldus Local API  
- Authentication steps are documented at  
http://api.telldus.net/localapi/api.html  
  
- The local API is otherwise not well documented. Although it got some resemblance with the Telldus Live API  
https://api.telldus.com/  

- Telldus TellStick ZNet Lite v2 has some additional info onboard  
http://192.168.1.5/api  
  
# Tibber
- Enter token in config node

# Installation  
Targeting raspberry pi with docker  

git clone https://github.com/johanon/home_automation.git  
cd home_automation  
sudo docker-compose up -d  

# Update    
- Ubuntu  
sudo apt-get update  
sudo apt-get upgrade  

- Containers  
docker-compose pull   
update veriosn number in nodered image ./nodered/Dockerfile   
docker-compose build  
docker-compose up -d  
(docker image prune)  



# Raspberry Pi additional installation notes    
Flash SD-card Samsung Evo with Raspbian OS

sudo apt update
sudo apt upgrade -y
curl -sSL https://get.docker.com | sh
sudo reboot
docker run hello-world

docker --version  
Docker version 20.10.21, build baeda1f