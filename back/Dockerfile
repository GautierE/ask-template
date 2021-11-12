FROM node:16-alpine as runner
ENV NODE_ENV=development

RUN apk update

COPY  . /app
WORKDIR /app

EXPOSE 3630
CMD ["npm", "run", ""]

FROM runner as builder
ENV NODE_ENV=production

COPY package*.json ./
RUN npm install

CMD ["npm", "start"]