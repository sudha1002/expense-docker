#FROM node:20
FROM node:20.19.4-alpine3.22
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
COPY package.json .
COPY *.js .
RUN npm install
CMD ["node","index.js"]