FROM node:lts-alpine
ENV NODE_ENV=production
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silentx
# RUN npm install --omit=dev && npm run build
# RUN npm install 
COPY . .
EXPOSE 3000
RUN npm run build
# RUN chown -R node /usr/src/app
USER node
CMD ["npm", "start"]