# Use official Node image
FROM node:16

WORKDIR /app

# Copy and install deps
COPY package*.json ./
RUN npm config set registry http://registry.npmjs.org/ && npm install

# Copy rest of the app and build
COPY . .
RUN npm run build

EXPOSE 3000
CMD [ "npm", "start" ]
