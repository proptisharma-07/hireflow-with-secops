FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN apk update && \
    apk upgrade && \
    npm ci --omit=dev

COPY . .

EXPOSE 8000

CMD ["npm", "start"]