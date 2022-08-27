FROM node:18-alpine

WORKDIR /app/node_service

COPY index.js package.json /app/node_service/

RUN yarn install --production

CMD ["node", "index.js"]

EXPOSE 3000