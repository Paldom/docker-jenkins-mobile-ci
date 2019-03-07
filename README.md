# docker-jenkins-mobile-ci
Dockerized Jenkins for mobile CI+CD pipelines, preinstalled plugins, macOS slave.

This [repository](https://github.com/Paldom/docker-jenkins-mobile-ci) contains the Dockerfile of the [dpal/docker-jenkins-mobile-ci](https://hub.docker.com/r/dpal/docker-jenkins-mobile-ci/) image, built on [official jenkins](https://hub.docker.com/r/jenkins/jenkins/) image.

Preinstalled with BlueOcean and many plugins like SCM (GitHub, BitBucket etc.) integration and plugins for supporting Android and iOS mobile application development.

A macOS slave is configured for running pipelines.

## Usage

### Prerequisites

Please note that macOS slave is required (optionally with physical devices) in order to run stages defined in Jenkinsfile. 
You can find example projects with configured Jenkinsfiles below:

- **Android:** https://github.com/Paldom/Mobile-CI-Android-Example
- **iOS:** https://github.com/Paldom/Mobile-CI-iOS-Example

### Pull image

#### From Docker Hub

```sh
docker pull dpal/docker-jenkins-mobile-ci:latest
```

#### Or build from GitHub

```sh
docker build -t dpal/docker-jenkins-mobile-ci github.com/paldom/docker-jenkins-mobile-ci
```

### Run docker image

Here's an example how to run this docker container:

```sh
docker run -p 8080:8080 -p 50000:50000 dpal/docker-jenkins-mobile-ci
```

For advanced usage and more details see [official guide](https://github.com/jenkinsci/docker/blob/master/README.md).