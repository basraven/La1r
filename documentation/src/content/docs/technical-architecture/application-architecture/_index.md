---
title: Application Architecture
type: docs
bookToc: false
bookCollapseSection : false
weight: 4
---
## Application Architecture
There is a large variety of applications currently running on the platform. \
This page gives an overview of all these applications and also acts as a formal catalog.
For that reason, this page will probably change a lot.
All applications with date added 14-06-2020 are applications which were added when this page was written and add date was unknown.

| Application Name              | Status                                                                        | Purpose                                                           | Namespace (if existing)           | Folder link                                                                   | Url                                   |
| ---                           | ---                                                                           | ---                                                               | ---                               | ---                                                                           | ---                                   |
| **Local machine**             |                                                                               |                                                                   |                                   |                                                                               |                                       |
| Control - Docker Jumphost     | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Jumphost on local dev machine to manage the cluster from Windows | Local - Control                   | [Control](/control/control.ps1/)                                              | N/A                                   |
| **Bian - Experimental AI**    |                                                                               |                                                                   |                                   |                                                                               |                                       |
| Doorbell image recognition    | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Image Recognition on video with Python 3.x                       | Brian - Image recognition         | [Image Recognition](/brian/image-recognition/)                                | N/A                                   |
| Zeppelin - Analytics          | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Zeppelin analytics platform for running spark jobs               | Brian - Zeppelin Analytics        | [Zeppelin Experimental](/brian/zeppelin/)                                     | http://zeppelin.bas                   |
| **Ansible**                   |                                                                               |                                                                   |                                   |                                                                               |                                       |
| DnsMasq                       | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Configuration of custom DNS Service from the server              | Ansible                           | [DnsMasq](/playbooks/roles/dnsmasq/)                                          | N/A                                   |
| OVPN                          | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  VPN Bare-Metal Service, hosts all major connections              | Ansible                           | [OVPN](/playbooks/roles/ovpn/)                                                | http://ovpn.bas                       |
| Prometheus Node Exporter      | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Exports all metrics data from each server to Prometheus          | Ansible                           | [Prometheus Node Exporter](/playbooks/roles/prometheus_node_exporter/)        | N/A                                   |
| Samba                         | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  File storage server for local LAN use only, to access data       | Ansible                           | [Samba](/playbooks/roles/samba/)                                              | N/A                                   |
| NFS                           | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  File storage server on external backup storage servers           | Ansible - Pi                      | [NFS](/playbooks/roles/nfs/)                                                  | N/A                                   |
| **Kubernetes**                |                                                                               |                                                                   |                                   |                                                                               |                                       |
| Backup jobs                   | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Bi-weekly and monthly backup Kubernetes jobs on all storage      | Kubernetes - Backup               | [Backup](/kubernetes/backup/)                                                 | N/A                                   |
| Comms - WhatsApp              | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  REST Endpoint expose Whatsapp client through Selenium            | Kubernetes - Comms                | [WhatsApp](/kubernetes/comms/whatsapp/)                                       | http://whatsapp.bas                   |
| Comms - Telegram              | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  REST Endpoint exposed Telegram client                            | Kubernetes - Comms                | [Telegram](/kubernetes/comms/telegram/)                                       | http://telegram.bas                   |
| FindLF - Wifi Tracking        | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  In-house wifi tracking                                           | Kubernetes - event                | [FindLF](/kubernetes/event/findlf/)                                           | N/A                                   |
| influxdb - kafka sink         | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  InfluxDB instance as data sink for Kafka                         | Kubernetes - event                | [InfluxDB Sink](/kubernetes/event/influxdb/)                                  | N/A                                   |
| kafka - event architecture    | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Kafka cluster which tracks all (home-automation) events          | Kubernetes - event                | [Kafka](/kubernetes/event/kafka/)                                             | http://kafka.bas                      |
| Nifi - event orchestration    | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Orchestrating all trafic in the event-driven architecture        | Kubernetes - event                | [Nifi](/kubernetes/event/nifi/)                                               | http://nifi.bas                       |
| Mosquito - "raw" data sink    | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Data sink for all event data which integrations with MQTT        | Kubernetes - event                | [Raw](/kubernetes/event/raw/)                                                 | N/A                                   |
| Zeppelin - Event-Driven       | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Zeppelin analytics platform for running event-driven analytics   | Kubernetes - event                | [Zeppelin Event](/kubernetes/event/zeppelin/)                                 | http://zeppelin.bas                   |
| Zookeeper - Election          | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Support app for leader election of decentralized infra           | Kubernetes - event                | [zookeeper](/kubernetes/event/zookeeper/)                                     | http://zookeeper.bas                  |
| homeassistant                 | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Home Automation Instance, integrates with home automation tools  | Kubernetes - homeautomation       | [Home Assistant](/kubernetes/homeautomation/homeassistant/)                   | http://homeassistant.bas              |
| openhab                       | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Secundairy Home Automation Instance, integrates to homeassistant | Kubernetes - homeautomation       | [Openhab](/kubernetes/homeautomation/openhab/)                                | http://openhab.bas                    |
| Kubernetes Dashboard          | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Management dashboard to manage Kubernetes through a GUI          | Kubernetes - kubernetes-dashboard | [Kubernetes Dashboard](/kubernetes/kubernetes-dashboard/)                     | http://kubernetes.bas                 |
| Traefik 2.x                   | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Reverse Proxy, managing all domain requests on port 65111        | Kubernetes - kube-system          | [Traefik 2.x](/kubernetes/kube-system/traefik)                                | http://treafik.bas                    |
| Weaveworks                    | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  L3 Network overlay for Kubernetes                                | Kubernetes - kube-system          | [Weaveworks](/kubernetes/kube-system/kubernetes/Makefile)                     | N/A                                   |
| Weave-scope                   | ![](https://img.shields.io/badge/Status-Disabled-red)                         |  Management GUI for Weaveworks network overlay                    | Kubernetes - kube-system          | [Weave Scope](/kubernetes/kube-system/weave-scope)                            | http://weavescope.bas                 |
| Chronograf - Monitoring       | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Management UI for Chronograf for monitoring                      | Kubernetes - monitoring           | [Chronograf Monitoring](/kubernetes/monitoring/chronograf)                    | http://chronograf.bas                 |
| Exporter - openvpn            | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  OpenVPN metrics exporter for Prometheus                          | Kubernetes - monitoring           | [Exporter Openvpn](/kubernetes/monitoring/exporter-openvpn)                   | N/A                                   |
| Exporter - qbittorent         | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Qbittorrent metrics exporter for Prometheus                      | Kubernetes - monitoring           | [Exporter Qbittorent](/kubernetes/monitoring/exporter-qbittorent)             | N/A                                   |
| Exporter - tautulli           | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Tautulli metrics exporter for Prometheus                         | Kubernetes - monitoring           | [Exporter Tautulli](/kubernetes/monitoring/exporter-tautulli)                 | N/A                                   |
| Exporter - varken             | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Plex metrics exporter for Prometheus                             | Kubernetes - monitoring           | [Exporter Varken](/kubernetes/monitoring/exporter-varken)                     | N/A                                   |
| Grafana                       | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Grafana Cluster Dashboards, dashboard for entire cluster         | Kubernetes - monitoring           | [Grafana](/kubernetes/monitoring/grafana)                                     | http://grafana.bas                    |
| Heimdall                      | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Customizable starting page                                       | Kubernetes - monitoring           | [Heimdall](/kubernetes/monitoring/heimdall)                                   | http://home.bas                       |
| InfluxDB - Monitoring         | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Data Store for Traefik (online & offline) and Varken             | Kubernetes - monitoring           | [InfluxDB Monitoring](/kubernetes/monitoring/influxdb)                        | N/A                                   |
| OpenVPN Status                | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  OpenVPN static metric aggregator on OVPN management port         | Kubernetes - monitoring           | [OpenVPN Status](/kubernetes/monitoring/openvpn-status)                       | http://openvpn.bas                    |
| Prometheus                    | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Metrics collector and data store                                 | Kubernetes - monitoring           | [Prometheus](/kubernetes/monitoring/prometheus)                               | http://prometheus.bas                 |
| Email - Nextcloud             | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  SMTP Server for sending out emails from Nextcloud                | Kubernetes - nextcloud            | [Email Nextcloud](/kubernetes/nextcloud/email)                                | http://email.bas                      |
| MariaDB - Nextcloud           | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  MySQL Database for storing Nextcloud Data                        | Kubernetes - nextcloud            | [MariaDB Nextcloud](/kubernetes/nextcloud/mariadb)                            | N/A                                   |
| Nextcloud                     | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Private storage cloud                                            | Kubernetes - nextcloud            | [Nextcloud](/kubernetes/nextcloud/nextcloud)                                  | http://cloud.bas                      |
| Redis - Nextcloud             | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Redis Cache for Nextcloud temp storage                           | Kubernetes - nextcloud            | [Redis Nextcloud](/kubernetes/nextcloud/redis)                                | N/A                                   |
| Nginx - Nextcloud Public      | ![](https://img.shields.io/website.svg?url=http%3A%2F%2Fcloud.basraven.nl)    |  Public Exposure of some of the Nextcloud resources, filtered     | Kubernetes - online               | [NGINX](/kubernetes/online/nginx)                                             | http://cloud.basraven.nl              |
| Traefik 2.x - Public          | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Reverse Proxy for all public endpoints                           | Kubernetes - online               | [Traefik 2.x Online](/kubernetes/online/traefik)                              | http://treafik-online.bas             |
| Authelia                      | ![](https://img.shields.io/badge/status-work%20in%20progress-orange)          |  Authentication Proxy, to secure expose applications              | Kubernetes - security             | [Authelia](/kubernetes/security/authelia)                                     | http://aithelia.bas                   |
| Openldap                      | ![](https://img.shields.io/badge/status-work%20in%20progress-orange)          |  OpenLDAP IAM implementation, for centralized user management     | Kubernetes - security             | [OpenLDAP](/kubernetes/security/openldap)                                     | http://ldap.bas                       |
| Phpladpadmin                  | ![](https://img.shields.io/badge/status-work%20in%20progress-orange)          |  OpenLDAP Management UI                                           | Kubernetes - security             | [PhpLdapAdmin](/kubernetes/security/openldap/phpldapadmin.yml)                | http://openldap.bas                   |
| Couchpotato                   | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Torrent Movie download library                                   | Kubernetes - torrent              | [coachpotato](/kubernetes/torrent/couchpotato/)                               | http://couch.bas                      |
| Jackett                       | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Torrent Trackers Management                                      | Kubernetes - torrent              | [Jackett](/kubernetes/torrent/jackett/)                                       | http://jackett.bas                    |
| Plex                          | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Plex Media Server                                                | Kubernetes - torrent              | [Plex](/kubernetes/torrent/plex/)                                             | http://plex.bas                       |
| Qbittorent                    | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Bittorrent Download Client                                       | Kubernetes - torrent              | [Qbittorent](/kubernetes/torrent/qbittorrent/)                                | http://torrent.bas                    |
| Radarr                        | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Movie Torrent data aggregator                                    | Kubernetes - torrent              | [Radarr](/kubernetes/torrent/radarr/)                                         | http://radarr.bas                     |
| Sonarr                        | ![](https://img.shields.io/badge/Status-Active-brightgreen)                   |  Series Torrent data aggregator                                   | Kubernetes - torrent              | [Sonarr](/kubernetes/torrent/sonarr/)                                         | http://sonarr.bas                     |