# Desafio de Infra - Lemobs

Este projeto tem como objetivo levantar uma aplicação web angular utilizando Nginx e Docker. 

## Ambiente:

Máquina Ubuntu 18.04

## Passo a Passo Seguido: 
### 1 - Instalar o Docker

apt install docker.io

#### 1.1 - Atualizar o Ubuntu

apt update

### 2- Instalar npm

apt install npm

### 3 - Instalar o Angular CLI

npm install -g @angular/cli@1.7.1

### 4 - Importar a Aplicação (em https://github.com/start-javascript/sb-admin-material) e executar.

git clone https://github.com/start-javascript/sb-admin-material.git
cd sb-admin-material

### 5- Criar a Dockerfile (alpine e nginx)

OBS: Escolhi usar a imagem do alpine por ser mais leve que as outras do dockerhub.

## Referências: 

- Descomplicando o Docker - Ed. Brasport
- https://hub.docker.com/_/nginx
- https://medium.com/marcosmota287/rodando-aplica%C3%A7%C3%A3o-angular-com-docker-e-nginx-9c28e7a99f4
https://medium.com/@chemidy/create-a-small-and-secure-angular-docker-image-based-on-nginx-93452cb08aa2

## Autora

* **Grazielle Alessa** - [graziellealessa](https://github.com/graziellealessa)

