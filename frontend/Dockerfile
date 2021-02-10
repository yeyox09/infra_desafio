FROM node:14.10.1 as build
WORKDIR /app
RUN npm cache clean --force
COPY ./frontend-desafio/package.json /app/
RUN npm install --no-package-lock
COPY ./frontend-desafio .
RUN npm run build --prod --aot --optimization --build-optimizer --vendor-chunk
FROM nginx:1.15.12-alpine
COPY --from=build /app/dist/frontend-desafio/ /usr/share/nginx/html
COPY /nginx-custom.conf /etc/nginx/conf.d/default.conf