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

Il existe divers méthodes pour installer prometheus et grafana. En ce qui nous concerne, nous allons utilisé l'outil Docker.

* ETAPES 1

  - [installation docker](https://docs.docker.com/engine/install/ubuntu)
  - [installation docker compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)


---

* ETAPES 2
  
  1. Dans la home directory (/home/username ou ~):
     
     - sudo mkdir nom_du_dossier
     - sudo nano docker-compose.yml ( lien vers le fichier de configuration: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/docker-compose.yml* )
     - sudo nano prometheus.yml (lien vers le fichier de configuration: *https://github.com/jeanmarctsh/install_prometheus_grafana/blob/install/prometheus.yml*)
     - docker-compose up -d (exécution de la commande en background)

---     

  2. Saisir l'adresse IP et le port au niveau du navigateur

  en cours de redaction