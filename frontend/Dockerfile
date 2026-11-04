FROM node:22-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

ARG VITE_BASE_URL=http://localhost:3000/api
ENV VITE_BASE_URL=${VITE_BASE_URL}
RUN npm run build

CMD ["./node_modules/.bin/vite", "preview", "--host", "0.0.0.0", "--port", "4173"]
