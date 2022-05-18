#using node 10
From node:10

#create app directory
WORKDIR  /usr/src/lafs

#install dependencies
#a wildcard is used to ensure both package.json and package-lock.json are copied
#where available(npm@5+)
COPY package*.json ./

RUN npm install -g @angular/cli@v6-lts
RUN npm install

#if you are building your code for production
# RUN npm ci --only=production

#bundle app source
COPY . .

#EXPOSE port outside container
EXPOSE 4200
# Command used to start application
CMD ng serve --host 0.0.0.0
