FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --omit=dev

COPY . .

ENV SERVER_PORT=8080
ENV SERVER_HOST=0.0.0.0
ENV REDIS_HOST=redis
ENV REDIS_PORT=6379

EXPOSE 8080

CMD ["node", "server.js"]