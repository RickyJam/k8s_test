FROM node:18-alpine

WORKDIR /app/node_server

COPY index.js package.json /app/node_server/

RUN yarn install --production

CMD ["node", "index.js"]

EXPOSE 3000