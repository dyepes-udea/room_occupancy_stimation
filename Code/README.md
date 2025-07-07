# Paso 1: Construir imagen
docker build -t room-occupancy-notebook .

# Paso 2: Ejecutar el contenedor
docker run -it -p 8888:8888 -v ${PWD}/app:/app room-occupancy-notebook
