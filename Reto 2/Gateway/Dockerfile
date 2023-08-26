#Usar una imagen base, como una imagen de Python si tu servidor está en Python
FROM python:3.9

#Directorio de trabajo dentro del contenedor
WORKDIR /app

#Copiar los archivos necesarios al contenedor
COPY . /app

#Instalar dependencias si es necesario
#RUN pip install -r requirements.txt
#Exponer el puerto en el que el servidor gRPC escucha
EXPOSE 50051

#Comando para ejecutar el servidor gRPC cuando se inicie el contenedor
CMD ["python", "server.py"]