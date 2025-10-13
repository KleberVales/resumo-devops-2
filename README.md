# resumo-devops-2

## Como construir uma imagem e como executar um container no docker.

### 🛠️ 1. Criar a imagem Docker

- 📄 Passo 1: Crie um arquivo Dockerfile

Exemplo básico para uma aplicação Node.js:
```Dockerfile

# Usa uma imagem base oficial
FROM node:18

# Cria diretório de trabalho
WORKDIR /app

# Copia os arquivos do projeto
COPY package*.json ./
RUN npm install
COPY . .

# Expõe a porta
EXPOSE 3000

# Comando para iniciar a aplicação
CMD ["node", "index.js"]


```

### 🧱 Passo 2: Construir a imagem

No terminal, execute:

```bash

docker build -t minha-imagem:1.0 .

```




## Comparando Nós Virtuais com Nós Gerenciados

## Estágios no OCI DevOps

## Resource Manager Introduction and concepts


