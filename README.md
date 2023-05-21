# DOCKER

## Ouroboros
* Keep docker images updated
* https://github.com/pyouroboros/ouroboros
* https://hub.docker.com/r/pyouroboros/ouroboros

## Dozzle
* Log viewer for docker containers
* https://dozzle.dev/
* https://github.com/amir20/dozzle
* https://hub.docker.com/r/amir20/dozzle/

## qBittorrent
* Web Client 
* https://hub.docker.com/r/linuxserver/qbittorrent

## HomeBridge
* HomeKit support for the impatient.
* https://homebridge.io/
* https://github.com/oznu/docker-homebridge

## Poste.io
* Poste.io ~ complete mail server
* https://poste.io/
* https://hub.docker.com/r/analogic/poste.io/
* **Does not work on RPI/ARM**

## Uptime Kuma
* A self-hosted monitoring tool similar to "Uptime Robot"
* https://uptime.kuma.pet/
* https://github.com/louislam/uptime-kuma
* https://hub.docker.com/r/louislam/uptime-kuma

## Homarr
* A modern and lightweight homepage for your server
* https://homarr.dev/
* https://github.com/ajnart/homarr/

## Yacht
* A container management UI with a focus on templates and 1-click deployments.
* https://yacht.sh/

## Dash
* a modern server dashboard
* https://getdashdot.com/
* https://github.com/MauriceNino/dashdot

## Troubleshooting

### Connect to Docker remote from IntelliJ IDEA (e.g RPI)
 * Setup a SSH Configuration: https://www.jetbrains.com/help/idea/create-ssh-configurations.html
 * On the remote where docker is running:
   * Run to edit the file: `sudo nano /etc/default/docker`
   * Using the `-H` flag in the `DOCKER_OPTS` variable in the `/etc/default/docker` file.
    ````
    DOCKER_OPTS="-H tcp://0.0.0.0:80"
    ````
   * Run `sudo usermod -aG docker $USER`
 * Explanations:
   * `usermod`: This is the command for modifying user accounts.
   * `-a`: This flag tells `usermod` to add the specified group to the user's existing groups (instead of replacing them).
   * `-G docker`: This specifies the name of the group to add the user to, which is "docker" in this case.
   * `$USER`: This is a shell variable that expands to the username of the currently logged-in user. The command is replacing `$USER` with the actual username of the user account you want to modify.
   * To list all available groups: `sudo getent group`
   * To list groups associated to the current user: `groups $USER`
