FROM node:12
# create app directory
WORKDIR /usr/src/app

# install app dependencies
COPY package.json ./
RUN yarn install

# bundle app source
COPY . .
EXPOSE 8080
CMD ["yarn", "run", "prod"]
