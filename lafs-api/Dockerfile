#using node 10
From node:10

#create app directory
WORKDIR  /usr/src/lafs

#install dependencies
#a wildcard is used to ensure both package.json and package-lock.json are copied
#where available(npm@5+)
COPY package*.json ./



#if you are building your code for production
# RUN npm ci --only=production

#bundle app source
COPY . .

#EXPOSE port outside container
EXPOSE 3000
# Command used to start application
CMD [ "node", "server/server.js"]
