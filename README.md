## FreshRSS

<p align="center">
    <a href="https://freshrss.github.io/FreshRSS/en/admins/01_Index.html">
        <img src="https://github.com/JuanRodenas/Docker-container-selfhosted/blob/main/freshrss/freshrss.png" alt="freshrss">
    </a>
    <br>
</p>
<!-- markdownlint-enable MD033 -->


## Versión latest docker freshrss
![Docker Image Version (latest)](https://img.shields.io/docker/v/linuxserver/freshrss?arch=amd64&color=blue&logo=docker&logoColor=blue&style=for-the-badge)

FreshRSS is a self-hosted RSS feed aggregator

* [Github](https://github.com/FreshRSS/FreshRSS)
* [Documentation](https://freshrss.github.io/FreshRSS/en/admins/01_Index.html)
* [Docker Image](https://hub.docker.com/r/linuxserver/freshrss)

## Usage

### Requirements

* [Traefik up and running](https://github.com/JuanRodenas/Docker-container-selfhosted/tree/main/traefik).
* A subdomain of your choice, this example uses `freshrss`.
  * You should be able to create a subdomain with your DNS provider, use a `A record` with the same IP address as your root domain.

### Configuration

Replace the environment variables in `.env` with your own, then run :

```bash
docker-compose up -d
```

You should now be able to access the freshrss setup instruction, it is quite straigthforward and nothing is required. 

### Update

The image is automatically updated with [watchtower](https://github.com/JuanRodenas/Docker-container-selfhosted/tree/main/watchtower) thanks to the following label :

```yaml
  # Watchtower Update
  - "com.centurylinklabs.watchtower.enable=true"
```
