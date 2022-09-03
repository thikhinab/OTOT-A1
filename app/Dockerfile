# ENV
FROM node:16

# working directory of the app
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
# COPY <src> <dest>
COPY . .

# App binds to port 8080 - EXPOSE instruction - map port by the docker daemon
# EXPOSE instruction informs Docker that the container listens on the specified network ports at runtime.
# EXPOSE does not make the ports of the container accessible to the host.
EXPOSE 8080

# Command to run the app (defines the run time)
CMD ["node", "index.js"]