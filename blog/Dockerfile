FROM node:lts-buster-slim AS development



COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm ci

WORKDIR /blog
COPY . .

RUN npm install -g @angular/cli

EXPOSE 4200

CMD ["ng","serve"]
