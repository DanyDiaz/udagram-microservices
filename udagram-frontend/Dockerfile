FROM node:13

# Create app directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Install ionic command tools
RUN npm install -g ionic

# Copy app source
COPY . .

# build app with ionic
RUN ionic build

# Bind the port that the image will run on
EXPOSE 8100

# run the api server
CMD ["ionic", "serve", "--no-open", "--external"]