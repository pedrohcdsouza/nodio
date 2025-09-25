# Dockerfile para backend Django
FROM python:3.11-slim

# Instala dependências do sistema
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Cria diretório de trabalho
WORKDIR /app

# Copia arquivos do projeto
COPY src/ ./src/
COPY manage.py ./
COPY requirements.txt ./

# Instala dependências Python
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# Expõe porta padrão do Django
EXPOSE 8000

# Comando para iniciar o servidor
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
