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

- -t minha-imagem:1.0: nome e tag da imagem
- .: indica que o Dockerfile está no diretório atual

### 🚀 2. Executar o container

- ▶️ Passo 3: Rodar a imagem como container

```bash
docker run -d -p 3000:3000 --name meu-container minha-imagem:1.0
```

* -d: modo destacado (em background)
* -p 3000:3000: mapeia a porta do host para o container
* --name: dá um nome ao container
* minha-imagem:1.0: imagem que será usada

## Comparando Nós Virtuais com Nós Gerenciados

### ⚙️ 1. Management Approach

### 🖥️ 2. Resource Allocation

### 🔀 3. Load Balancing

### 🌐 4. Pod Networking

### 📈 5. Scaling


## Estágios no OCI DevOps

## Resource Manager Introduction and concepts


