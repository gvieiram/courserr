# Use a imagem Python como base
FROM python:3.9

# Instale o FFmpeg
RUN apt-get update && apt-get install -y ffmpeg

# Defina o diretório de trabalho dentro do container
WORKDIR /app

# Copie os arquivos do backend para o diretório de trabalho
COPY . .

# Crie e ative o ambiente virtual
RUN python3 -m venv venv
RUN . venv/bin/activate

# Instale as dependências do Python
RUN pip3 install -r requirements.txt

# Exponha a porta em que o servidor Flask está sendo executado
EXPOSE 5000

# Comando para iniciar o servidor Flask
CMD ["python3", "app.py"]
