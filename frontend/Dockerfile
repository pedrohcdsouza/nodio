# Dockerfile para frontend Next.js
FROM node:20-alpine

# Diretório de trabalho
WORKDIR /app

# Copia arquivos de dependências
COPY package.json package-lock.json* pnpm-lock.yaml* yarn.lock* ./

# Instala dependências
RUN npm install

# Copia o restante do código
COPY . .

# Build da aplicação
RUN npm run build

# Expõe porta padrão do Next.js
EXPOSE 3000

# Comando para iniciar o servidor
CMD ["npm", "start"]
