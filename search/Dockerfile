FROM node:lts AS runtime
WORKDIR /app

COPY package.json yarn.lock ./
RUN yarn install
COPY . .

ENV HOST=0.0.0.0
ENV PORT=3000
EXPOSE 3000
CMD yarn build && node ./dist/server/entry.mjs
