# awscli-container

![Build](https://img.shields.io/docker/cloud/build/scottam/awscli)
![Docker Pulls](https://img.shields.io/docker/pulls/scottam/awscli)
![MIT Licence](https://img.shields.io/github/license/scottalexandermurray/awscli-container)

This repository contains a dockerfile that is used to build a minimal docker image with the AWS CLI installed.

The reason I decided to create this is to allow processes (in particular, CI/CD) to leverage this image when interacting with AWS

You can check out the DockerHub page [here](https://hub.docker.com/r/scottam/awscli)!

## How-To

### Pull

```sh
docker pull scottam/awscli:latest
```

### Run

```sh
docker run -e AWS_ACCESS_KEY_ID=*access_key* -e AWS_SECRET_ACCESS_KEY=*secret_key* -e AWS_DEFAULT_REGION=*region* scottam/awscli:latest aws s3 ls
```

### Poke around

```sh
docker run -it scottam/awscli:latest sh
```
