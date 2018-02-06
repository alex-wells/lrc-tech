# runs multicast inside a container to support the LRC tech setup

# import Node.js; use the current LTS version
FROM debian:stable

# install buildtools for the native extension support
RUN apt-get update && apt-get install -y build-essential apt-utils curl libavahi-compat-libdnssd-dev sudo

# install nodesource binary distribution
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs
RUN node -v
RUN npm install npm --global

# set the working directory
WORKDIR /multicast

# install multicast
RUN npm i multicast

# set up multicast
RUN ln -s /multicast/node_modules/multicast/index.js /multicast/multicast
ADD config /multicast/node_modules/multicast/.config

EXPOSE 3944

# set the startup command
ENTRYPOINT ["/multicast/multicast", "start"]

