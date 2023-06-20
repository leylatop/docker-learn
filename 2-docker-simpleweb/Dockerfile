FROM node:14-alpine

WORKDIR /usr/app
COPY ./package.json ./
COPY .npmrc ./
# 将copy package.json的操作放在前面，这样当package.json没有变化时，就不会重新安装依赖，安装依赖这一步就可以使用缓存的镜像
RUN npm install

COPY ./ ./

CMD ["npm", "start"]