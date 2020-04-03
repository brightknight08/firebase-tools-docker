FROM node:8
ARG BUILD_DATE
ARG CI_JOB_ID
ARG CI_PIPELINE_ID
ARG VERSION
ARG VCS_REF
LABEL org.label-schema.schema-version="1.0" \
  org.label-schema.name="firebase-tools" \
  org.label-schema.version=${VERSION} \
  org.label-schema.build-date=${BUILD_DATE} \
  org.label-schema.description="Firebase CLI on the NodeJS image" \
  org.label-schema.url="https://github.com/firebase/firebase-tools/" \
  org.label-schema.vcs-url="${CI_PROJECT_URL}" \
  org.label-schema.vcs-ref=${VCS_REF} \
  ci_job_id=${CI_JOB_ID} \
  ci_pipeline_id=${CI_PIPELINE_ID} \
  node_version="8" \
  firebase_tools_version=${VERSION}
ENV FIREBASE_TOOLS_VERSION=${VERSION}
ENV HOME=/home/node
ENV DEBIAN_FRONTEND noninteractive
#     '--> https://github.com/eduwass/docker-node-git
RUN apt update && \
  apt install -y default-jdk && \
  apt install -y git && \
  yarn global add firebase-tools@${VERSION} && \
  yarn cache clean && \
  firebase setup:emulators:firestore && \
  firebase setup:emulators:pubsub && \
  firebase setup:emulators:database && \
  npm rebuild && \
  firebase -V && \
  java -version && \
  chown -R node:node $HOME
USER node
VOLUME $HOME/.cache
WORKDIR $HOME
CMD ["sh"]
