# Multi stage docker
# Stage 1 create a build
FROM node:18-alpine as builder

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# Stage 2 serving the application
FROM node:18-alpine

WORKDIR /app

COPY --from=builder /app/dist .

RUN npm install -g serve

CMD ["serve", "-s", ".", "-l", "tcp://0.0.0.0:5000"]
