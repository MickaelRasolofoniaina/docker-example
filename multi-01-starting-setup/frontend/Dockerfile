FROM node

WORKDIR /app

RUN npm install -g serve

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

ARG DEFAULT_PORT=80

ENV PORT=$DEFAULT_PORT

EXPOSE $PORT

CMD ["sh", "-c", "serve -s build -l $PORT"]