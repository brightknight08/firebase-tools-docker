# firebase-tools docker image

> **[Firebase-tools CLI](https://www.npmjs.com/package/firebase-tools)** installed
> globally over the official **[NodeJS images](https://hub.docker.com/_/node)** (with
> different versions with -buster too)

<!--
  PLAIN TEXT DESCRIPTION FOR DOCKER HUB:

      Firebase-tools CLI installed globally over the official NodeJS images (different versions + buster)
  -->

[![NodeJS](https://img.shields.io/badge/nodejs-8,%2010,%2012,%20LTS-3c873a?style=for-the-badge&logo=node.js&labelColor=111)](https://nodejs.org "NodeJS")
[![Firebase-tools](https://img.shields.io/badge/firebase--tools-8.16.1-ea3b00?style=for-the-badge&logo=firebase&labelColor=111)](https://www.npmjs.com/package/firebase-tools "Firebase-tools")
[![Gitlab](https://img.shields.io/badge/CI%2FCD%20by-gitlab-ea3b00?style=for-the-badge&logo=gitlab&labelColor=111)](https://gitlab.com/ "Gitlab")
[![OpenJDK](https://img.shields.io/badge/OpenJDK-11-ea3b00?style=for-the-badge&labelColor=111)](https://openjdk.java.net/ "OpenJDK")
[![Docker Pulls](https://img.shields.io/docker/pulls/thirddegreeapps/firebase-tools-docker?logo=docker&style=for-the-badge&labelColor=111)](https://www.docker.com/ "Docker")

## what's inside

- node (8, 10, 12, latest lts) + npm
- yarn
- Firebase-tools 8.16.1
- Emulators for Cloud Firestore, PubSub, and Realtime Database
- git
- OpenJDK 11 (default-jdk)

## quick reference

- File the issues here
  **[on the issues page on gitlab](https://gitlab.com/timanthony/firebase-tools-docker/-/issues)**
- Find the different node LTS-based Dockerfiles
  **[in this directory](./node-lts/)**
- Do you want to contribute? Or suggest features, improvements, etc? Find
  the [contributing mini-guide here](./CONTRIBUTING.md)
- here's what the image **[firebase-tools-docker:10-buster-rc-8.16.1](registry.gitlab.com/timanthony/firebase-tools-docker:10-buster-rc-8.16.1)**
  means:
  - **firebase-tools-docker**: the name
  - **10**: node version
  - **buster**: Debian buster
  - **rc**: release candidate
  - **8.16.1**: firebase-tools version
- [mirrored github repo](https://github.com/brightknight08/firebase-tools-docker)
- [gitlab main repo](https://gitlab.com/timanthony/firebase-tools-docker)

### notes

Firebase version is kept (we're trying hard, so bear with us)
up-to-date as much as possible. Firebase emulators also come pre-installed

automated builds (done with the awesome Gitlab server and runners) are scheduled
on a weekly basis to keep the other installed softwares up-to-date.

**multiple node versions are provided because Firebase Cloud Functions require
either node-8 or node-10.**

#### nodejs 8

Firebase-tools v8.12.0 no longer supports (or its dependencies) NodeJs 8. Although
NodeJs 8 is still supported, it will be stuck on **Firebase-tools v8.10.0** from
now on.

## credits

HUUUGE, huge thanks to [Andrey Senov](https://github.com/AndreySenov) for the original project in
GitHub. This project itself was forked from his
[firebase-tools-docker project here](https://github.com/AndreySenov/firebase-tools-docker).

## license

**MIT License**

_Copyright (c) 2020 Tim Anthony Manuel_

_Original Copyright (c) 2019-2020 Andrey Senov
forked from https://github.com/AndreySenov/firebase-tools-docker_

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

> ### WE OFFER NO GUARANTEES
>
> THIS DOCKER IMAGE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
> EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
> MERCHANTABILITY,FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
> IN NO EVENT SHALL THE MAINTAINERS BE LIABLE FOR ANY CLAIM, DAMAGES OR
> OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
> ARISING FROM, OUT OF OR IN CONNECTION WITH THE DOCKER IMAGE OR THE USE
> OF OTHER DEALINGS IN THE DOCKER IMAGE.

_however, we do use the images for our own commercial private projects and so we
probably would be updating this every now and then to keep up with the dependency
requirements of firebase tools_
