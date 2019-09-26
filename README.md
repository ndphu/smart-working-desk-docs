# smart-working-desk-docs
Documents for Smart Working Desk project


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
 * Run `docker-compose up`
 
## Run the UI
* Cloning repo: https://github.com/ndphu/face-ui.git
* Edit: `src/api/Config.js`, update:
  * baseUrl: 'http://<your_virtual_machine_ip_address>:8080/api'
  * wsUrl : 'ws://<your_virtual_machine_ip_address>:8080/api/ws'
* Run `npm start`

# For cloud hosting:
* TBD...
