# home-assistant-docker-compose

Already configured setup for Home Assistant with Zigbee2MQTT, Mosquitto-MQTT, and MariaDB.
Some changes are required, but outside of editing ".env" file, it should work out of the box. (it does work even if you don't change anything in the file, but the default passwords are in no way safe).

# Usage

    git clone https://github.com/lesquerre/home-assistant-docker-compose.git
    cd home-assistant-docker-compose
    nano -l .env #or whatever editor you prefer
    (change default settings & save)
    docker-compose up -d
    
    
Home Assistant URL: http://< serverIP >:8123 (or http://localhost:8123 if deployed locally).

Password is the one you set up in .env file

# Config file details

# .env file
You need to update the value of ZIGBEE_ADAPTER_TTY to the actual tty that you have on you machine, otherwise the container will not start. For example, for CC2531 this is /dev/ttyACM0.
Also, you should change the default passwords with something else.
    
    LOCAL_USER=1000
    MYSQL_ROOT_PASSWORD=password
    HA_MYSQL_PASSWORD=password
    VSCODE_PASSWORD=password
    ZIGBEE_ADAPTER_TTY=/dev/ttyACM0
    

 
