# PI-HOLE & Unbound Docker Compose

## Useful Resources

- [Setup Pihole Docker (Official)](https://github.com/pi-hole/docker-pi-hole/#running-pi-hole-docker)
- [Configure Clients to use Pihole](https://discourse.pi-hole.net/t/how-do-i-configure-my-devices-to-use-pi-hole-as-their-dns-server/245)
- [Blog Post](https://pimylifeup.com/pi-hole-docker/)
- [resolvconf ubuntu 17+ issue fix](https://askubuntu.com/questions/907246/how-to-disable-systemd-resolved-in-ubuntu)
- [Second Helpful Blog Post - Run PiHole on Localhost](https://thanosmour-tk.medium.com/run-pi-hole-in-localhost-and-some-extras-4b50e76611e6)
- [Unbound as Upstream DNS](https://nlnetlabs.nl/projects/unbound/about/)
- [Reddit Thread for Getting Unbound to run in same Container as PiHole](https://www.reddit.com/r/docker/comments/rbgrm8/how_to_install_unbound_and_pihole_in_docker_using/)

Use in combination with the browser extension [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm) for blocking youtube ads for example. Update: Youtube is getting hip to ad blockers of all kinds. Check out these open source solutions as work around.
    - [invidious.io](https://invidious.io/)


## Environment

Create an `.env` file in the same directory as the `docker-compose.yml` file.
```
# directory/folder structure
pihole (root dir name)
    |
    .gitignore
    .READMe.md
    docker-compose.yml
    .env
```

Inside of the `env file`:

```
PIHOLE_PWD=<super secret password for logging into pihole dashboard>
```

## Run Project

The project can be run with the command `docker-compose up -d`. Pihole and Unbound will restart automatically unless explicity stopped by a user.