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
Flash SD-card Samsung Evo with Raspbian Buster using Balena Etcher.  
In boot directory. Touch ssh and add wpa_supplicant.conf for wifi.  
Boot up pi. Change password and /etc/hostname  
sudo apt-get update  
sudo apt-get upgrade  

Docker from Raspbian stretch official repos too old to support docker-compose features (2020-01-16).  
docker --version  
Docker version 1.8.3, build f4bf5c7  

Using official Docker repos blending the following instructions  
https://docs.docker.com/install/linux/docker-ce/debian/  
and  
https://withblue.ink/2019/07/13/yes-you-can-run-docker-on-raspbian.html  
going for arch=armhf  

sudo apt-get remove docker docker-engine docker.io containerd runc  
sudo apt update  
sudo apt install apt-transport-https ca-certificates curl gnupg2 software-properties-common  
curl -fsSL https://download.docker.com/linux/raspbian/gpg | sudo apt-key add -

echo "deb [arch=armhf] https://download.docker.com/linux/$(. /etc/os-release; echo "$ID") \
     $(lsb_release -cs) stable" | \
    sudo tee /etc/apt/sources.list.d/docker.list

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
docker --version  
Docker version 19.03.5, build 633a0ea
