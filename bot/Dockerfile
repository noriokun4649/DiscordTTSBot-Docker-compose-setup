FROM node:erbium-alpine3.12

WORKDIR /var/docker/discord-tts-bot

RUN apk update && \
    apk upgrade && \
    apk --no-cache --virtual add git python3 make g++ && \
    git clone https://github.com/noriokun4649/Discord-TTS-Voice-channel-Bot.git . && \
    apk del

RUN npm install

VOLUME  /var/docker/discord-tts-bot/config

ENTRYPOINT [ "npm", "start" ]