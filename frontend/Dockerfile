FROM node:8.9.4

RUN mkdir -p /usr/src/app
COPY . /usr/src/app
WORKDIR /usr/src/app

RUN npm i && npm run build && \
    npm install -g serve && \
    adduser app && \
    chown -R app /usr/src/app
USER app
WORKDIR app

EXPOSE 3000

CMD ["serve", "-s", "-l", "3000", "build"]