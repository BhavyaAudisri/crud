FROM node:22-slim

RUN useradd -m appuser

WORKDIR /app

COPY package*.json ./

RUN npm install

RUN npm install express

COPY . .

RUN chown -R appuser:appuser /app

USER appuser

EXPOSE 8080

CMD ["node", "app/server.js"]