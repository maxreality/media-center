dockerized  media-center setup to make my life easier

Contains Plex, Sonarr, Radarr, Tautulli, Gluetun, Transmission, Jackett, Nzbget

Gluetun is the VPN container. Torrents/Newsgroups depend on Gluetun being up and running, otherwise downloading doesn't happen. This is for protection.
Plex plays the videos
Tautulli is an add-on for Plex that keeps the library organized
Sonarr fetches show via Transmission for Torrents or Nzbget for Usenet
Radarr fetches movies via Transmission for Torrents or Nzbget for Usenet
Jackett is the liason between Sonarr/Radarr and the trackers
Transmission is the torrent client
Nzbget is the newsgroups client

Prerequisites
-----

Docker Composer

See the [Docker Composer website](https://docs.docker.com/compose/) for installation instructions.

Build
-----

Steps to build a Docker image:

1. Clone this repo

        git clone https://github.com/maxreality/media-center.git

2. Fill in the blanks for your VPN

3. Ensure your mnt directories exist and change docker-compose to reflect them

4. Docker-compose

        docker-compose -f [path/to/docker-composer.yaml] up -d
    This will take a few minutes.

5. Once everything has started up, you should be able to access the webapp via [http://localhost:8989/]
