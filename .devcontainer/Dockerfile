FROM node:16

WORKDIR /workspaces
RUN apt update


RUN curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
RUN install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
RUN sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/edge stable main" > /etc/apt/sources.list.d/microsoft-edge-dev.list'
RUN rm microsoft.gpg
RUN apt update
RUN apt install microsoft-edge-dev -y

#RUN apt upgrade

RUN npm install -g @marp-team/marp-cli
