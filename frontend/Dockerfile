FROM node:10-alpine as builder
WORKDIR /usr/src/app
COPY . .
RUN npm install
RUN npm run build

FROM nginx:alpine
COPY --from=builder /usr/src/app/build/ /usr/share/nginx/html
COPY nginx/conf.d /etc/nginx/conf.d
EXPOSE 80