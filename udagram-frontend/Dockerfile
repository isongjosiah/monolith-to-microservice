## build
FROM beevelop/ionic:latest AS ionic

# create app directory
WORKDIR /usr/src/app

# install app dependencies
COPY package*.json ./
RUN npm ci

# bundle app source
COPY . .
RUN ionic build

# run
FROM nginx:alpine
#copy www /usr/nginx/html
COPY --from=ionic /usr/src/app/www /usr/share/nginx/html
