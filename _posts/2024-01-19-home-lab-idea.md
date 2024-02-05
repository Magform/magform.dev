---
Title: "Home Lab Idea"
toc: true
categories:
    - Home Lab
tags:
    - Home Lab
    - Networking
    - DIY
    - Virtualization
    - Security
    - Configuration
excerpt: "An idea for setting up a home lab for learning server management, networking, and more."
---

# Home Lab Idea

Embarking on the journey of constructing my home lab, I meticulously assessed the learning goals I aspired to achieve, considering the balance between financial investment and effort expended.  

My primary focus revolves around gaining comprehensive insights into server management, containers, virtual machines, server hardware, and networking. To maintain fiscal prudence, I opted for retired enterprise hardware—although aging, it still efficiently serves its purpose.  

In terms of effort, my abundant spare time fuels my enthusiasm for hands-on projects, allowing me the flexibility to delve deeply into each endeavor. While time constraints are loose, budget considerations guide the timing of my hardware acquisitions.  

## Hardware

Outlined below are the components currently in my possession or slated for acquisition in the upcoming weeks:  

Machine name | Hardware | CPU | RAM | Graphic Card | Storage
---|---|---|---|---|---
VMs | Dell Precision 5810 | Intel Xeon E5-1650 v4 | 2x16GB | Nvidia Quadro M4000 8GB | 4TB HDD + 2x256GB SSD
Storage | HP Proliant DL360p G8 | 2xE5-E650L V2 | 8x8GB | none | 4x6TB HDD
3D Printer | Raspberry pi 3B | ARM Cortex-A53 | 1GB | none | 64GB SD
Router | Fodenn F10 | N95 | 16GB | none | 512GB M.2 SSD
Switch | PLANET WGSW-28040 | | | |

## Configuration and Utilities

Let's delve into the planned configurations and utilities for each component:

### VMs

In the Dell Precision 5810, I will set up VMs using Proxmox to leverage the processing power from my laptop and maybe also for some cloud gaming.  
Additionally, I plan to run a VM containing a Docker instance to host gaming servers.  
To optimize power usage, I will only run this machine when necessary configuring some remote power on.  

### Storage

The HP Proliant DL360p G8 will serve as my high-performance storage machine.  
I will run a media manager and backup services on separate VMs with Docker inside.  

#### Media Manager

- [Jellyfin](https://jellyfin.org/)
- [Jellyseer](https://github.com/Fallenbagel/jellyseerr)
- [Sonarr](https://sonarr.tv/)
- [Radarr](https://radarr.video/)
- [qBitTorrent](https://www.qbittorrent.org/)

#### Backup

- [Nextcloud](https://nextcloud.com/)
- [Synchthing](https://syncthing.net/)
- [Photonix](https://photonix.org/)

### 3D Printer

Utilizing the Raspberry Pi 3B, I'll enhance my 3D printer experience by implementing Klipper and Mainsail, potentially using [Printd](https://github.com/mkuf/prind) for configuring and controlling everything.

### Router

The Fodemm F10 MiniPC will serve as an always-on machine, providing more than just routing capabilities. It will also host various monitoring tools, smart home applications, and utility services:

#### Monitoring

- [UptimeKuma](https://uptime.kuma.pet/)
- [Graphana](https://grafana.com/)
- [Prometheus](https://prometheus.io/)
- [OpenSpeedTest](https://github.com/openspeedtest/Docker-Image)

#### Smart Home

- [Home Assistant](https://www.home-assistant.io/)
- [Firefly-III](https://www.firefly-iii.org/)
- [Grocy](https://github.com/grocy/grocy)

#### Utility

- [dashboard](https://github.com/gethomepage/homepage)
- [Portainer](https://www.portainer.io/)
- [OpenWRT](https://openwrt.org/)
- [piHole](https://pi-hole.net/)
- [Cloudflared](https://hub.docker.com/r/cloudflare/cloudflared)
- [Authelia](https://www.authelia.com/)
- [VaultWarden](https://github.com/dani-garcia/vaultwarden)
- [Nginx Proxy Manager](https://nginxproxymanager.com/)

## Conclusion

This represents my current blueprint for the home lab. Over the next few weeks, I'll delve into the configurations, foreseeing possible adjustments and enhancements. Stay tuned for updates on my evolving ideas, configurations, and experiments within my home lab.
