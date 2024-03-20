# Unifi Controller Deployment for Docker Compose

This project provides an easy means of setting up the Ubiquiti Unifi Controller stack on a Raspberry PI.

## Starting

Execute the following in this project's directory to start the controller, mongodb and the mongo-express admin console:

```bash
docker compose up -d
```

All services use the username and password:

* username: `unifi`
* password: `pwd`

The following URLs will be setup:

* Controller UI: [https://localhost:8443](https://localhost:8443)
* Mongo Express UI: [http://localhost:8081](http://localhost:8081)
* Mongo connection URL: `mongodb://unifi:pwd@unifi-db:27017/`

## Network setup

The default configuration of all Unifi devices looks for the controller host using the hostname `unifi`. Ensure that your local router's DNS settings are configured accordingly. 

## Stopping the services

Within this directory, run: 

```bash
docker compose down
```
