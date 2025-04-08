FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build

# Serve using a simple web server like serve
RUN npm install -g serve
CMD ["serve", "-s", "build", "-l", "3000"]
