FROM node:latest AS Build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM gcr.io/distroless/nodejs22-debian12
WORKDIR /app
COPY --from=Build /app/node_modules /app/node_modules
COPY --from=Build  /app/.next /app/.next

CMD ["node_modules/next/dist/bin/next","start","--port","3000"]

