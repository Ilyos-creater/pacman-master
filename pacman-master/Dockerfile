FROM node:14-alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A production install is used by default; adjust as needed for development
COPY package.json ./
RUN npm install --production

# Bundle app source
COPY . .

EXPOSE 8080

CMD ["npm", "start"]
