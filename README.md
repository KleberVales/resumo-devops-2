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

### 💰 6. Pricing


## Estágios no OCI DevOps

A estratégia blue-green no OCI DevOps é composta por até quatro estágios, sendo dois opcionais:

1. Deployment Stage

Seleção dos dois ambientes (OKE ou Instance Group)
Escolha dos artifacts a serem implantados
Load balancer para Instance Group ou NGINX ingress controller para OKE

2. Invoke Function Stage (opcional)

Função personalizada para validar a aplicação no ambiente standby

3. Manual Approval Stage (opcional)

Etapa de aprovação manual antes da mudança de tráfego

4. Blue-Green Traffic Shift Stage

Redirecionamento de 100% do tráfego para o ambiente standby validado



## Resource Manager Introduction and concepts


