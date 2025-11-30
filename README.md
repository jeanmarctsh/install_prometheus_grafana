# INSTALLATION PROMETHEUS ET GRAFANA

---

## SOMMAIRE

1. [INTRODUCTION](#introduction)
2. [PRESENTATION](#presentation)
3. [PROCESSUS D'INSTALLATION](#processus-dinstallation)

---

## INTRODUCTION

Dans un monde informatique où la gestion de ressources constitue un élément majeur pour le bon fonctionnnement d'un parc informatique, il est nécessaire de mettre en place un dispositif de surveillance qui permet de collecter les données de différents équipements au sein d'un parc informatique. Et ce, en temps réel. Il existe plusieurs outils tels que : Zabbix, nagios, cacti, grafana et prometheus, etc... Dans le cadre de notre projet, nous allons utilisé Grafana afin d'effectuer un monitoring complet de nos différentes machines clientes et serveurs.

---

## PRESENTATION

---

## PROCESSUS D'INSTALLATION

Avant d'installer prometheus et grafana. Il est nécessaire de choisir quelle méthode d'installation à mettre en oeuvre, en ce qui nous concerne, nous allons nous servir de l'outil docker.

* ETAPE 1
  
  Installation de docker engine et docker-compose

  - [installation docker](https://docs.docker.com/engine/install/ubuntu)
  - [installation docker compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)


---

* ETAPE 2

  Déploiement de Prometheus et grafana via docker-compose
  
  1. Dans la home directory (/home/username ou ~):
     
     - sudo mkdir nom_du_dossier
     - sudo nano docker-compose.yml ( lien vers le fichier de configuration: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/docker-compose.yml* )
     - sudo nano prometheus.yml (lien vers le fichier de configuration: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/prometheus.yml*)
     - docker-compose up -d (exécution de la commande en background)

---     

* ETAPE 3 

  Connexion via navigateur web avec adresse IP

  Avant de passer à la supervision d'une infrastructure informatique, il est nécessaire que les différentes machines du système disposent d'un navigateur web. 

    - Pour Prometheus: **[http://IP_SERVEUR:9090]**
    - Pour Grafana:    **[http://IP_SERVEUR:3000]**

