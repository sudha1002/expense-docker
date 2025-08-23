#FROM node:20
FROM node:20.19.4-alpine3.22
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
CMD ["node","index.js"]