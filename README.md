# 🚀 INSTALLATION PROMETHEUS ET GRAFANA


---

## SOMMAIRE

- [🚀 INSTALLATION PROMETHEUS ET GRAFANA](#-installation-prometheus-et-grafana)
  - [SOMMAIRE](#sommaire)
  - [📝 INTRODUCTION](#-introduction)
  - [💻 PRESENTATION](#-presentation)
  - [🔧 PREREQUIS](#-prerequis)
  - [⚙️ PROCESSUS D'INSTALLATION](#️-processus-dinstallation)

---

## 📝 INTRODUCTION

Dans un monde informatique où la gestion de ressources constitue un élément majeur pour le bon fonctionnnement d'un parc informatique, il est nécessaire de mettre en place un dispositif de surveillance qui permet de collecter les données de différents équipements au sein d'un parc informatique. Et ce, en temps réel. Il existe plusieurs outils tels que : Zabbix, nagios, cacti, grafana et prometheus, etc... Dans le cadre de notre projet, nous allons utilisé Grafana afin d'effectuer un monitoring complet de nos différentes machines clientes et serveurs.

---

## 💻 PRESENTATION

---

## 🔧 PREREQUIS

- OS : Ubuntu 22.04 LTS
- Disque : SSD 25GO
- RAM : 4GO
- HYPERVISEUR DE TYPE 1 ou 2

---

## ⚙️ PROCESSUS D'INSTALLATION

Avant d'installer prometheus et grafana. Il est nécessaire de choisir la méthode d'installation à mettre en place, en ce qui nous concerne, nous allons nous servir de l'outil docker.

* ETAPE 1
  
  🐋 Installation de docker engine et docker-compose.

  - [installation docker](https://docs.docker.com/engine/install/ubuntu)
  - [installation docker compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)


---

* ETAPE 2

  📊🔔📈 Déploiement de Prometheus et grafana via docker-compose
  
  1. Dans la home directory (/home/username ou ~):
     
       ```shell 
       $ sudo mkdir nom_du_dossier && cd nom_du_dossier
       ```

       ```shell 
       $ sudo nano docker-compose.yml
       ```
      ( lien vers le fichier de configuration: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/docker-compose.yml* )
 
       ```shell 
       $ sudo nano prometheus.yml 
       ```
      (lien vers le fichier de configuration: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/prometheus.yml*)

      Exécution de la commande en arrière plan:  

       ```shell 
       $ docker-compose up -d 
       ```
     
---     

* ETAPE 3 

  🌐 Connexion via navigateur web avec adresse IP

  Avant de passer à la supervision d'une infrastructure informatique, il est nécessaire que les différentes machines du système    disposent d'un navigateur web. 

| Prometheus             |  Grafana                |
|------------------------|-------------------------|
| http://IP_SERVEUR:9090 | http://IP_SERVEUR:3000  |



  🔌 Test de connectivité avec curl

| Prometheus                     |  Grafana                               |
|--------------------------------|----------------------------------------| 
| curl -I http://IP_SERVEUR:9090 | curl -I http://IP_SERVEUR:3030         |                     

   
  


---

Afin de mieux collecter les métriques de différents ordinateurs de notre parc, il est important d'installer

  - Node-exporter : Pour collecter les métriques sur les ordinateurs Linux.
  - Windows-exporter : Pour collecter les métriques sur les ordinateurs Windows. 

