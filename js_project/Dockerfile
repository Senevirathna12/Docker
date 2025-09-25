# base image
FROM node:20-alpine

# Specify the working directly inside the Docker
WORKDIR /app

# copy the package.json
COPY package.json .

# install the dependencies
RUN npm install 

# copy the source code -> (COPY source dest)
COPY . .

# Run the app
CMD [ "npm","start" ]