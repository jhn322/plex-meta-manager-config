# Plex Meta Manager Config (v1.20 and later)

My Plex Meta Manager config for automatically creating collections and overlays to Plex. These files were originally created using templates and has since then been rewritten completely and updated regularly by me since 2021. For all lists and overlays to work you'll need to configure API tokens from Trakt, MyAnimeList, AniDB, TMDb and more in your config.yml file.

## Install (Docker Compose)

This will install Plex meta manager using docker compose with a daily run schedule for collections, overlays and operations as three seperate containers.

1. Download this repository.
2. Add **your** Plex IP-adress and token to config.yml.
3. **(Highly recommended)** many collections in this config pulls information from services like Trakt, mdblist and more which requires a valid api key/token/id. Please visit the [config section in the wiki](https://metamanager.wiki/en/latest/config/trakt.html) on how to configure them.
4. [Install docker with compose](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/How-to-install-Docker-and-docker-compose-on-Ubuntu) or [Docker desktop](https://www.docker.com/products/docker-desktop/) for Windows (if you haven't already).
5. Open terminal and navigate to your path:

```powershell
Windows: "cd C:\path\to\PMM-folder"

Linux: "cd /path/to/PMM-folder"
```

6. Now paste this in the terminal to create the containers:

```powershell
Windows: "docker-compose up -d"

Linux: "sudo docker-compose up -d"
```

**Done!**

## Docker run

This will run through the entire config one time, It will **not** keep PMM updated on a schedule.

```powershell
Windows: "docker run -it -v "C:\path\to\PMM-folder/config:/config:rw" meisnate12/plex-meta-manager --run"

Linux: "sudo docker run -it -v "/path/to/PMM-folder/config:/config:rw" meisnate12/plex-meta-manager --run"
```

## Update PMM

This will update Plex meta manager to the latest branch version.

```powershell
Stable: docker pull meisnate12/plex-meta-manager
Develop: docker pull meisnate12/plex-meta-manager:develop
Nightly: docker pull meisnate12/plex-meta-manager:nightly
```

## Targeted library types:

- Anime
- Audiobooks
- Movies
- Music
- Remux
- Soundtracks
- TV
- Videos

### Collections examples

**Movies**

![image search api](https://i.imgur.com/BcRlpKv.png)

**TV**

![image search api](https://i.imgur.com/GjuyuRq.png)

**Anime**

![image search api](https://i.imgur.com/GaM8Ti3.png)

### Overlays examples

**Movies**

![image search api](https://i.imgur.com/cTeNiMb.png)

**TV**

![image search api](https://i.imgur.com/7cUfZ53.png)

**Remux**

![image search api](https://i.imgur.com/lcFOxiG.png)

### For more help go to the wiki: https://metamanager.wiki/en/latest/
