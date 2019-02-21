# For contributor

## Requirements
1. [Docker](https://docs.docker.com/engine/installation/)
1. [Docker compose](https://docs.docker.com/compose/install/#install-compose)
> Got **ERROR** Couldn't connect to Docker daemon at http+docker://localunixsocket - is it running?
```
sudo usermod -aG docker $USER
sudo systemctl restart docker
su $USER -
```

### Setup
1. Copy `.env.dist` file to `.env` and update settings
    > **TIP:* ```$ cp .env.dist .env```
1. Run `$ echo "DOCKER_UID=$UID" >> .env`
    > **TIP:** Or add `DOCKER_UID=1000` to the `.env` file
1. `docker-compose up -d`

#### Server Thanks https://github.com/naga3/docker-lamp
* Now you can access local server by entering [http://172.18.0.1](http://172.18.0.1)
* MySQL administration page is [http://172.18.0.1:8080](http://172.18.0.1:8080)
> **NOTE:** MySql hostname is "mysql" not ~~localhost~~
