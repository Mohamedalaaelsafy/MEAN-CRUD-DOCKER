FROM node:latest
WORKDIR /usr/src/app
COPY ./package*.json ./
RUN npm ci --only=production
RUN npm audit fix --force
COPY . .
EXPOSE 3000
CMD ["node","index.js"]
