FROM ubuntu:20.04

WORKDIR /workspaces

# install nodejs
RUN apt-get update
RUN apt install wget gnupg -y
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -
RUN apt-get update
RUN apt install nodejs -y
RUN apt install npm -y

RUN npm install n -g


# install marp
RUN npm install -g @marp-team/marp-cli

# install google chrome
RUN sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
RUN apt-get update
RUN apt install google-chrome-stable -y