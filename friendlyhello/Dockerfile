# Usamos la imagen base oficial de Python 3 (slim es una versión ligera)
FROM python:3-slim

# Establecemos el directorio de trabajo dentro del contenedor donde se ejecutará nuestra aplicación
WORKDIR /app

# Copiamos todos los archivos del directorio local (build context) al directorio de trabajo /app dentro del contenedor
COPY . /app

# Instalamos las dependencias listadas en el archivo requirements.txt dentro del contenedor usando pip
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Indicamos que el contenedor debe escuchar en el puerto 80 cuando esté en ejecución
EXPOSE 80

# Definimos una variable de entorno llamada NAME que tendrá el valor "World" por defecto
ENV NAME World

# Especificamos el comando que se ejecutará cuando se inicie el contenedor, en este caso ejecutaremos el script "app.py" con Python
CMD ["python", "app.py"]
