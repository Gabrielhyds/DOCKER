# Docker Comandos Principais

## Comandos Básicos de Docker

### Imagens
```sh
# Listar Imagens Locais
docker images

# Baixar uma Imagem do Docker Hub
docker pull <imagem>

# Construir uma Imagem a partir de um Dockerfile
docker build -t <nome-da-imagem> .

# Remover uma Imagem
docker rmi <imagem>

# Listar Contêineres em Execução
docker ps

# Listar Todos os Contêineres (Incluindo Parados)
docker ps -a

# Criar e Iniciar um Contêiner
docker run -it --name <nome-do-conteiner> <imagem>

# Iniciar um Contêiner Parado
docker start <conteiner>

# Parar um Contêiner em Execução
docker stop <conteiner>

# Remover um Contêiner
docker rm <conteiner>

# Acessar um Contêiner em Execução
docker exec -it <conteiner> /bin/bash

# Listar Volumes
docker volume ls

# Criar um Volume
docker volume create <nome-do-volume>

# Remover um Volume
docker volume rm <nome-do-volume>

# Listar Redes
docker network ls

# Criar uma Rede
docker network create <nome-da-rede>

# Conectar um Contêiner a uma Rede
docker network connect <nome-da-rede> <nome-do-conteiner>

# Desconectar um Contêiner de uma Rede
docker network disconnect <nome-da-rede> <nome-do-conteiner>

# Construir uma Imagem e Adicionar uma Tag
docker build -t <nome-da-imagem>:<tag> .

# Adicionar uma Tag a uma Imagem Existente
docker tag <imagem>:<tag-antiga> <imagem>:<nova-tag>

# Ver Logs de um Contêiner
docker logs <conteiner>

# Ver Informações do Sistema Docker
docker info

# Ver Detalhes de um Contêiner
docker inspect <conteiner>

# Iniciar Serviços Definidos no docker-compose.yml
docker-compose up

# Iniciar Serviços em Background
docker-compose up -d

# Parar Serviços
docker-compose down

# Reiniciar Serviços
docker-compose restart

# Listar Serviços em Execução
docker-compose ps

# Executar um Comando em um Serviço em Execução
docker-compose exec <serviço> <comando>

# Remover Todas as Imagens
docker rmi $(docker images -q)

# Remover Todos os Contêineres
docker rm $(docker ps -a -q)

# Remover Recursos Não Utilizados
docker system prune

# Remover Volumes Não Utilizados
docker volume prune

# Remover Redes Não Utilizadas
docker network prune
