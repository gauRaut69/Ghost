FROM gitpod/workspace-full

USER root

RUN apt-get update \
    && apt-get install -y docker.io \
    && rm -rf /var/lib/apt/lists/*

USER gitpod

CMD ["sleep", "infinity"]
