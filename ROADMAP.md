# ROADMAP

Here's where the versions will be based from:

## 1.0

## 0.5

- add non-LTS node versions
- add [docker bench](https://github.com/docker/docker-bench-security)
- add test and deploy stage jobs

## 0.4

- conform to the guidelines stated [here](https://github.com/nodejs/docker-node/blob/master/docs/BestPractices.md)
- add script to automate the gitlab-ci yaml file update when new dockerfiles
  are added.

## 0.3

- add tests for the resulting docker images. this can be a node install, firebase
  deploy, etc.
- add apine-based images

## 0.2

- add script to automate the _dockerfile_ creation. this will make it easier to
  modify the template files and propagate the changes to all the docker files
  later
- add template files for the said script
