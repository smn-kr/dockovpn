<p align=center><img src="https://alekslitvinenk.github.io/docker-openvpn/assets/img/logo-s.png"></p><br>

<p align="center">
<a href="https://github.com/smn-kr/docker-openvpn/blob/master/README.md">[English]</a>
<br>

# 🔐DockOvpn
## Introduction 

This project is a fork of the [DockOvpn Project](https://github.com/dockovpn/dockovpn).
The project aims to setup a Open VPN Server in a docker container.
Unfortunatly the project hasnt seen much updates in the last 2 years (at the time 31.10.2026).

This project contains some quickfixes to enable the user to update the dependencies in this project.
For example the alpine version of this project is now pinned to latest tag instead of a specific version tag.

This project unfortunatly this repo won´t be maintained as well, but it should be at least possible to update the container image.

## Prerequisites

1. Any hardware or vps/vds server running Linux. You should have administrative rights on this machine.
2. Docker installation on your server.
3. Public ip address assigned to your server.
4. Install docker-compose additionally to docker on your server

## 1. Run dockovpn

It is recommended to use [docker-compose](https://docs.docker.com/compose/) to setup the project

To run dockvpn with docker-compose run:

```bash
docker-compose up -d && \
docker-compose exec -d dockovpn wget -O /opt/Dockovpn/client.ovpn localhost:8080
```

You can find a example docker compose file [here](https://github.com/smn-kr/dockovpn/blob/master/docker-compose.yml). 

After run this command you can find your `client.ovpn` inside `openvpn_conf` folder.

To update the container please run:

```bash
docker-compose build && \
docker-compose up -d 
```

## Other resources

[Privacy Policy](https://github.com/smn-kr/docker-openvpn/blob/master/PRIVACY_POLICY.md) \
[Contrubition Guidelines](https://github.com/smn-kr/docker-openvpn/blob/master/CONTRIBUTING.md) \
[Code Of Conduct](https://github.com/smn-kr/docker-openvpn/blob/master/CODE_OF_CONDUCT.md) \
[Release Guideline](https://github.com/smn-kr/docker-openvpn/blob/master/docs/RELEASE_GUIDELINE.md) \
[License Agreement](https://github.com/smn-kr/docker-openvpn/blob/master/LICENSE)
