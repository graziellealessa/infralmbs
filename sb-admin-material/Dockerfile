# 1 - Criar o site estatico
FROM node:alpine as builder
RUN apk update && apk add --no-cache make git
# Criar a pasta para aplicacao
WORKDIR /app
# Instalar as dependencias
COPY package.json package-lock.json /app/
RUN cd /app && npm set progress=false && npm install
# Copiar os arquivos do projeto para dentro da imagem docker
COPY .  /app
RUN cd /app && npm run build

# 2 - Criar a imagem do nginx com o site estatico
FROM nginx:alpine
## Remover o site do nginx default
RUN rm -rf /usr/share/nginx/html/*
## Copiar o site criado para a pasta pública do nginx
COPY --from=builder /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
