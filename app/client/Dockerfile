FROM node:16.19 AS build
WORKDIR /usr/src/app
COPY . .
RUN npm install -g @angular/cli@8.3.17
RUN npm install @angular/core@8.0.0   
RUN npm install 
RUN ng build
FROM nginx:1.17
COPY --from=build /usr/src/app/dist/* /usr/share/nginx/html/

