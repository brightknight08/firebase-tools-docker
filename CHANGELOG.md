# CHANGELOG

Here are the changes:

## 0.1.0

- forked base codes from the original
  [firebase-tools-docker GitHub repo](https://github.com/AndreySenov/firebase-tools-docker)
- added dockerfiles for **node-8**, **node-10**, **node-12**, **lts-latest**
  ([see the notes](./node-lts/latest-lts/NOTES.md)). also added the **buster**
  versions, too.
- modified [.gitlab-ci.yml file](./.gitlab-ci.yml) to have the build jobs for the
  other non-alpine dockerfiles.
