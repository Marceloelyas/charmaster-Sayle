# charmaster-Sayle

### 📂 Como usar

# 1.Salve o arquivo na pasta do seu projeto:

bash
cd ~/Documentos/Backend/Aprendendo/chatmaster-backend
cat > ../dashboard.html << 'EOF'
# (cole todo o HTML acima aqui)
EOF
Acesse no navegador: http://localhost:3000/dashboard.html


# 🎨 Funcionalidades do Dashboard


# Elemento         	Descrição
**Header**        	Título, descrição e badge de progresso
**Stats Cards**    	6 métricas do aprendizado
**Progress Bar**  	Animação de 0% a 100%
**13 Módulos**    	Cada um com status, descrição, tags e link
**Arquitetura**	    Diagrama visual do fluxo da aplicação
**Code Snippet**	  Exemplo de código real (JWT)
**Recursos**	      Links para documentação oficial
**Footer**	        Créditos e opções de reset

# 🎯 Cores e Status

🟢 Verde (Completed) - Módulo concluído

🟡 Laranja (In Progress) - Módulo em andamento

🔴 Vermelho (Pending) - Módulo pendente

O dashboard é totalmente responsivo e funciona em mobile, tablet e desktop!

# 📦 Passo 1: Preparar os arquivos

Primeiro, vamos organizar a estrutura final do projeto:
bash
cd ~/onde se encontra o seu projeto/ dashboard.html

# Criar arquivo .gitignore
cat > .gitignore << 'EOF'
# Node
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.env
.env.local
.env.*.local

# Database
*.db
*.db-journal
*.sqlite
*.sqlite3

# Logs
logs/
*.log
error.log
combined.log

# OS
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/
*.swp
*.swo

# Build
dist/
build/
*.min.js

# PM2
.pm2/
EOF
Criar README.md completo
bash
cat > README.md << 'EOF'

# 💬 ChatMaster - Chat em Tempo Real com Node.js

## 📋 Sobre o Projeto

ChatMaster é uma aplicação de chat em tempo real desenvolvida como projeto de aprendizado para dominar o desenvolvimento back-end com Node.js. O projeto implementa todas as principais tecnologias e conceitos modernos de desenvolvimento web.

## 🎯 Tecnologias Abordadas

### Back-End
| Tecnologia | Descrição |
|------------|-----------|
| **Node.js** | Ambiente de execução JavaScript |
| **Express.js** | Framework web para Node.js |
| **Socket.io** | WebSockets para comunicação em tempo real |
| **SQLite/PostgreSQL** | Banco de dados relacional |
| **JWT** | Autenticação baseada em tokens |
| **bcrypt** | Hashing de senhas |
| **Helmet** | Segurança de headers HTTP |
| **Winston** | Logging estruturado |

### DevOps & Ferramentas
| Ferramenta | Descrição |
|------------|-----------|
| **Docker** | Containerização da aplicação |
| **PM2** | Gerenciamento de processos |
| **Nginx** | Proxy reverso e balanceamento |
| **Git** | Controle de versão |
| **npm** | Gerenciador de pacotes |

## 📚 Módulos do Curso

1. ✅ Introdução ao Node.js
2. ✅ Módulos Principais do Node.js
3. ✅ Gerenciador de Pacotes (npm)
4. ✅ HTTP e Modelo de Padrões Web
5. ✅ API REST e Serviços Web
6. ✅ Introdução ao Express
7. ✅ Middleware Express
8. ✅ Tratamento de Erros no Express
9. ✅ WebSockets (Socket.io)
10. ✅ Node e SQL
11. ✅ Segurança e Privacidade
12. ✅ Autenticação (JWT)
13. ✅ Ferramentas e Implantação

## 🏗️ Arquitetura
Frontend (HTML/CSS/JS)

↓
HTTP/WebSocket
↓
Express + Socket.io
↓
SQLite/PostgreSQL

text

## 🚀 Como Rodar o Projeto

### Pré-requisitos
- Node.js 18+
- npm ou yarn
- Git

### Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/chatmaster.git
cd chatmaster/backend

# Instale as dependências
npm install

# Configure as variáveis de ambiente
cp .env.example .env

# Execute em modo desenvolvimento
npm run dev

## Acesse a aplicação

Frontend: http://localhost:3000

API Health Check: http://localhost:3000/api/health

Dashboard: http://localhost:3000/dashboard.html

### 📦 Estrutura do Projeto
text
chatmaster-backend/
├── src/
│   ├── config/         # Configurações (banco, etc)
│   ├── controllers/    # Controladores
│   ├── middleware/     # Middlewares (auth, security)
│   ├── models/         # Modelos de dados
│   ├── routes/         # Rotas da API
│   ├── services/       # Serviços (websocket, etc)
│   └── utils/          # Utilitários
├── frontend/
│   └── public/         # Arquivos estáticos
├── .env                # Variáveis de ambiente
├── .gitignore
├── package.json
├── server.js
└── README.md

# 🔐 Autenticação

## Endpoints da API
## Método	      Endpoint	          Descrição
**POST**	          /api/auth/register	Registrar novo usuário
**POST**	          /api/auth/login	    Login e retorno do JWT
**GET**	            /api/auth/me	      Obter dados do usuário atual
**GET**	            /api/messages	      Listar mensagens
**POST**	          /api/messages	      Criar nova mensagem
**DELETE**	        /api/messages/:id	  Deletar mensagem

# 🛡️ Segurança Implementada

✅ Rate Limiting (proteção contra DDoS)

✅ Helmet (headers de segurança)

✅ Sanitização de entrada

✅ Validação com express-validator

✅ CORS configurado

✅ JWT com expiração

✅ Bcrypt para senhas

✅ Proteção contra XSS e SQL Injection

# 📡 WebSocket Events

##Evento	          Descrição
connection	        Nova conexão WebSocket
chat-message	      Envio de mensagem
new-message	        Broadcast de nova mensagem
typing	            Indicador de digitação
user-connected	    Usuário entrou no chat
user-disconnected	  Usuário saiu do chat
users-online	      Lista de usuários online

# 🐳 Docker

bash
# Build da imagem
docker build -t chatmaster .

# Executar container
docker run -p 3000:3000 --env-file .env chatmaster

# 📈 Deploy em Produção

## Com PM2

bash
npm install -g pm2
pm2 start server.js --name chatmaster
pm2 save
pm2 startup

# Com Docker

bash
docker-compose up -d

# 📝 Licença

Este projeto está sob a licença MIT.

# 👨‍💻 Autor

Marcelo Sayle - marcelo_elyas@github.com

# ⭐ Se este projeto te ajudou, deixe uma estrela!

EOF

text

### Criar LICENSE (MIT)

```bash
cat > LICENSE << 'EOF'
MIT License

Copyright (c) 2025 [Seu Nome]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF

# Criar docker-compose.yml

bash
cat > docker-compose.yml << 'EOF'
version: '3.8'

services:
  postgres:
    image: postgres:15-alpine
    environment:
      POSTGRES_DB: chatmaster
      POSTGRES_USER: chatuser
      POSTGRES_PASSWORD: chatpass123
    volumes:
      - postgres_data:/var/lib/postgresql/data
    ports:
      - "5432:5432"
    networks:
      - chat-network

  backend:
    build:
      context: .
      dockerfile: Dockerfile
    environment:
      NODE_ENV: production
      DATABASE_URL: postgresql://chatuser:chatpass123@postgres:5432/chatmaster
      JWT_SECRET: ${JWT_SECRET}
    ports:
      - "3000:3000"
    depends_on:
      - postgres
    networks:
      - chat-network
    volumes:
      - ./logs:/app/logs

  nginx:
    image: nginx:alpine
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ./nginx.conf:/etc/nginx/conf.d/default.conf
      - ./ssl:/etc/nginx/ssl
    depends_on:
      - backend
    networks:
      - chat-network

volumes:
  postgres_data:

networks:
  chat-network:
    driver: bridge
EOF

# Criar Dockerfile

bash
cat > Dockerfile << 'EOF'
FROM node:18-alpine

WORKDIR /app

# Copiar package.json e package-lock.json
COPY package*.json ./

# Instalar dependências
RUN npm ci --only=production

# Copiar código fonte
COPY . .

# Criar usuário não-root
RUN addgroup -g 1001 -S nodejs
RUN adduser -S nodejs -u 1001
USER nodejs

EXPOSE 3000

CMD ["node", "server.js"]
EOF

# 📤 Passo 2: Inicializar o Git e enviar para o GitHub

No terminal, execute:
bash
# Inicializar o Git
git init

# Adicionar todos os arquivos
git add .

# Verificar o que será commitado
git status

# Fazer o primeiro commit
git commit -m "🚀 Initial commit: ChatMaster - Chat em tempo real com Node.js"

# Conectar ao repositório remoto (crie um repositório no GitHub primeiro!)
# Substitua SEU_USUARIO e NOME_DO_REPOSITORIO pelos seus dados
git remote add origin https://github.com/SEU_USUARIO/chatmaster.git

# Enviar para o GitHub
git branch -M main
git push -u origin main

# 🌟 Passo 3: Criar repositório no GitHub

Via interface do GitHub:
Acesse GitHub.com

Clique no botão "New" (ou + → New repository)

Preencha:

Repository name: chatmaster

Description: 💬 Chat em tempo real com Node.js - Projeto completo de aprendizado Back-End

Public ou Private (escolha sua preferência)

Não inicialize com README, .gitignore ou license (já temos)

Clique em "Create repository"

Execute os comandos do passo 2 com a URL do seu repositório

# 📋 Passo 4: Verificar o push

bash
# Ver se tudo foi enviado
git remote -v
git log --oneline

# Se precisar forçar o push (cuidado!)
# git push -u origin main --force

# 🎨 Passo 5: Adicionar Badges ao README (opcional, mas fica bonito)
Adicione no topo do seu README.md:

markdown
![Node.js](https://img.shields.io/badge/Node.js-18+-green)
![Express](https://img.shields.io/badge/Express-4.x-blue)
![Socket.io](https://img.shields.io/badge/Socket.io-4.x-lightgrey)
![SQLite](https://img.shields.io/badge/SQLite-3.x-blue)
![JWT](https://img.shields.io/badge/JWT-Auth-orange)
![Docker](https://img.shields.io/badge/Docker-24.x-blue)
![License](https://img.shields.io/badge/License-MIT-green)

# 📁 Estrutura final do repositório
text
chatmaster/
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   └── database.js
│   │   ├── middleware/
│   │   │   ├── auth.js
│   │   │   └── security.js
│   │   ├── models/
│   │   │   ├── User.js
│   │   │   └── Message.js
│   │   ├── routes/
│   │   │   ├── auth.js
│   │   │   └── messages.js
│   │   └── services/
│   │       └── websocket.js
│   ├── frontend/
│   │   └── public/
│   │       ├── index.html
│   │       └── dashboard.html
│   ├── .env.example
│   ├── .gitignore
│   ├── docker-compose.yml
│   ├── Dockerfile
│   ├── package.json
│   ├── server.js
│   └── chat.db
├── README.md
└── LICENSE

#🔐 Passo 6: Criar .env.example (modelo)

bash
cat > .env.example << 'EOF'
# Ambiente
NODE_ENV=development
PORT=3000

# Segurança
JWT_SECRET=sua_chave_super_secreta_aqui
CORS_ORIGIN=http://localhost:3000

# Rate Limiting
RATE_LIMIT_MAX=100

# Banco de Dados (SQLite)
# DB_PATH=./chat.db

# PostgreSQL (se usar)
# DATABASE_URL=postgresql://usuario:senha@localhost:5432/chatmaster
EOF
📊 Passo 7: Comandos úteis para o GitHub
bash
# Ver status
git status

# Adicionar mudanças
git add .
git add -A

# Commit com mensagem
git commit -m "📝 descrição das mudanças"

# Push
git push origin main

# Ver histórico
git log --oneline --graph --all

# Criar tag de versão
git tag -a v1.0.0 -m "Versão 1.0.0 - Lançamento inicial"
git push origin v1.0.0

# 🎯 Pronto!
Seu projeto agora está no GitHub com:

✅ Código completo e organizado

✅ README profissional

✅ LICENSE MIT

✅ .gitignore configurado

✅ Docker e docker-compose

✅ Variáveis de ambiente de exemplo

Parabéns! 🎉 Você tem agora um portfólio completo no GitHub mostrando todas as habilidades de back-end que aprendeu!

