# Home automation  
Including 
- Telldus Tellstick  
- Oregon temperature sensors

# Telldus Local API  
- Authentication steps are documented at  
http://api.telldus.net/localapi/api.html  
  
- The local API is otherwise not well documented. Although it got some resemblance with the Telldus Live API  
https://api.telldus.com/  

- My TellStick has some additional info onboard  
http://192.168.1.5/api  
(Telldus TellStick ZNet Lite v2)  

# Installation  
Targeting raspberry pi with docker  
Docker from default repository  
sudo apt-get update  
sudo apt install docker.io  
sudo systemctl start docker  
sudo systemctl enable docker  
docker --version  
Docker version 1.8.3, build f4bf5c7  
