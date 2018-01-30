# runs multicast inside a container to support the LRC tech setup

# import Node.js; use the current LTS version
FROM debian:stable

# install buildtools for the native extension support
RUN apt-get update && apt-get install -y build-essential apt-utils curl libavahi-compat-libdnssd-dev

# install nodesource binary distribution
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs
RUN node -v
RUN npm install npm --global

# set the working directory
WORKDIR /multicast

# install multicast
RUN sudo npm i multicast -g

# set up multicast
RUN /usr/bin/multicast config

EXPOSE 3944

# set the startup command
CMD ["/usr/bin/multicast start"]

