FROM node:slim
RUN mkdir /app
WORKDIR /app
# 只有基于该镜像构建的下一级镜像才会执行 ONBUILD 指令
ONBUILD COPY ./package.json /app
ONBUILD RUN [ "npm", "install" ]
ONBUILD COPY . /app/
CMD [ "npm", "start" ]