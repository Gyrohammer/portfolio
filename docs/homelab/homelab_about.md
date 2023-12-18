# Home Server (Homelab)

I got into homelabbing out of a need for data resilience and privacy. My main need was to have a NAS (Network Attached Storage) for simple computer backup for both my system and my partners system. That was the initial goal, what has transpired since has been a result of my curiosity and want for more self-hosted applications. Below are some brief descriptions of those services with some light details:

## Jellfyin <img align="" width="20" height="20" src="../assets/jellyfin_logo.png"/>
I have quite a lot of physical media which means uploading it to the server allows me to play it whenever and wherever I please. I do this in tandem with wireguard, a VPN which is hosted on the OPNSense router as well as on the main server.

## Wireguard <img align="" width="20" height="20" src="../assets/wireguard-icon.png"/>
This is my VPN of choice for accessing my home network on the go. Not only does this ensure privacy on public networks, but it also blocks ads due to PiHole, a DNS filter.

## Photosync <img align="" width="20" height="20" src="../assets/photosync-icon.png"/>
As well as backing up to iTunes, I employ backing my photo library up to a local folder on the server. This ensures two copies are made (three if we think recursively) as well as makes sure they're easily accessible should I need to manually look through them.

## Gameservers <img align="" width="20" height="20" src="../assets/server-icon.png"/>
Hosting a server for a multiplayer game can be a pain which is why I took it upon myself to host anything that friends or family wish to play. By using cloudflares DNS system I can resolve my personal IP address to a url for easier usage.

## Network Management <img align="" width="20" height="20" src="../assets/opnsense-icon.png"/>
My router is a OPNSense system running on an intel NUC. I also have unifi systems on my network which are controlled by a docker container on the main server. OPNSense was chosen to familiarize myself with enterprise implementations akin to PFSense and for data privacy. This NUC can also be used as another host if I were to set up a docker swarm for other projects.