FROM node:8.7-wheezy

MAINTAINER Christian Dornbusch <christian.dornbusch@useeds.de>

# Global install yarn package manager and gulp
RUN apt-get update && apt-get install -y curl apt-transport-https && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && apt-get install -y yarn && \
    npm install --global gulp-cli

WORKDIR /workspace
