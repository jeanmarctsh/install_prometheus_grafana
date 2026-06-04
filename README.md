
<h1 align="center">Hands-on with Prometheus and Grafana</h1>

---

## About the tools

Prometheus and Grafana are two complementary open-source tools for monitoring. Prometheus collects and stores metrics, while Grafana enables their visualization through dashboards, facilitating data interpretation and rapid decision-making, particularly through alerting capabilities.

---

## Output

  - Server monitoring setup
  - Exporters installation(node and windows exporter)
  - Dashboard in grafana
  - Metrics collection system
  
## Expected outcome

  - Real-time visibility of server health (containers, disk, cpu, ram, etc...)
  - Early detection of perfomance issues
  - Prevention of server downtime
  - Faster incident response

---

## Project structure

  ```text
  INSTALL_PROMETHEUS_GRAFANA/
  ├── docker-compose.yml       # Configuration of different services in the main file "docker-compose.yml"
  ├── prometheus.yml           # Prometheus main configuration file "prometheus.yml"
  ├── .gitignore               # Define rules in the .gitignore file
  ├── .env.example             # Example .env file
  └── README.md                # Project description
  ```

---

## Prerequisites and Requirements

  - Operating System : Ubuntu 22.04 LTS
  - Storage : SSD, 25GB
  - RAM : 4GB
  - HYPERVISOR TYPE 1 or 2 (e.g., VMware ESXi, VirtualBox, Proxmox)
  - Prometheus-node-export for linux monitoring
  - Windows-exporter for windows monitoring
  - Docker engine and docker compose

---

## Installation Procedure

  * STEP 1
    
     Installation of docker engine and docker-compose.

    - [installation of docker](https://docs.docker.com/engine/install/ubuntu)
    - [installation of docker compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)


  ---

  * STEP 2

    Deployment of Prometheus and Grafana using docker-compose
    
    1. In the user's home directory (/home/username or ~):
      
        ```shell 
        $ mkdir nom_du_dossier && cd nom_du_dossier
        ```

        ```shell 
        $ sudo nano docker-compose.yml
        ```
        ( Link to the configuration file: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/docker-compose.yml* )
  
        ```shell 
        $ sudo nano prometheus.yml 
        ```
        (Link to the configuration file: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/prometheus.yml*)

        To run the docker-compose.yml file, use the following command:  

        ```shell 
        $ docker compose up -d 
        ```
      
  ---     

  * STEP 3 

     Web Access via Browser

    Access the services using your web browser. A browser is required for monitoring dashboards and system visualization. 


  | Prometheus             |  Grafana                |
  |------------------------|-------------------------|
  | http://IP_SERVEUR:9090 | http://IP_SERVEUR:3000  |



    🔌 Connectivity test (Using curl command)

  | Prometheus                     |  Grafana                               |
  |--------------------------------|----------------------------------------| 
  | curl -I http://IP_SERVEUR:9090 | curl -I http://IP_SERVEUR:3000         |                     

---

## 📫 CONTACT

[![Email](https://img.shields.io/badge/Email-red?style=for-the-badge&logo=gmail)](mailto:jeanmarctshimbombo@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/jean-marc-ngandu-b60796222)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=for-the-badge&logo=github)](https://github.com/jeanmarctsh)
