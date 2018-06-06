FROM node:10.0.0-slim

COPY ./src/services/catalog/package.json /opt/microservices/
COPY ./src/services/catalog/app.js /opt/microservices/
RUN cd /opt/microservices; yarn install

ARG service_version
ENV SERVICE_VERSION ${service_version:-v1}

EXPOSE 3000
WORKDIR /opt/microservices

CMD ["yarn","start"]