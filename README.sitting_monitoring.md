# smart-working-desk-docs
Documents for Sitting Monitoring And Reminding App

# Code repositories
### Services
#### Web API server
   https://github.com/ndphu/face-service
   
#### Face recognization worker
   https://github.com/ndphu/face-recognizer-worker

#### Monitoring service
   https://github.com/ndphu/monitor-service

#### Notification service
   https://github.com/ndphu/notification-service
   
#### Commons packages
   https://github.com/ndphu/swd-commons
 
### Web UI
   https://github.com/ndphu/face-ui

### Slackbot
   TBD

### Hardwares and emulator
#### Capture daemon on Raspberry Pi and Camera emulation for Windows
   https://github.com/ndphu/framed

### OPS
#### Docker stuffs
   https://github.com/ndphu/smart-working-desk-ops



# For local hosting:
## Prerequiresite
 * A virtualmachine running Ubuntu/CentOS (Ubuntu 18.04 is reccomended)
 * Docker is up and running (https://docs.docker.com/install/linux/docker-ce/ubuntu/)
    * I'm using Docker Engine - Community 19.03.2
 * Docker Compose is installed (https://docs.docker.com/compose/install/)
    * I'm using docker-compose version 1.24.1
    
## Bringup the backend
 * Cloning repo: https://github.com/ndphu/smart-working-desk-ops.git
 * Navigate to `local` directory
 * Source the `env.sh` file to test credentials
 * Run `docker-compose build --no-cache` then `docker-compose up`
 * Please check the `env.sh` file for needed credentials to integrate with Firebase Auth and Slack
 
### Bring up the UI
* Cloning repo: https://github.com/ndphu/face-ui.git
* Edit: `src/api/Config.js`, update:
  * baseUrl: "http://<your_virtual_machine_ip_address>:8080/api"
  * wsUrl : "ws://<your_virtual_machine_ip_address>:8080/api/ws"
* Run `npm start`

## Emulate the Camera Device
 * Download the Windows build: https://github.com/ndphu/framed-mqtt/releases/tag/0.0.1-alpha-windows
 * Update `mqttBroker` to `tcp://<your_virtual_machine_ip_address>:1883`
 * Set the `deviceSerial` correctly with the device created from `Smart Working Desk UI`


# For cloud hosting:
* TBD...
