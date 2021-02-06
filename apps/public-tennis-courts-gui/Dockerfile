# pull official base image
FROM node:15.8.0-alpine

# set working directory
WORKDIR /var/www/public-tennis-courts-gui

# add `/app/node_modules/.bin` to $PATH
ENV PATH /apps/public-tennis-courts-gui/node_modules/.bin:$PATH

# install app dependencies
COPY ./app/package.json ./
COPY ./app/package-lock.json ./
RUN npm install --silent
RUN npm install react-scripts@3.4.1 -g --silent

# add app
COPY ./app ./

# start app
CMD ["npm", "start"]