# testDevOps

#Instalación de Docker
sudo apt-get install docker.io

#inicializar y habilitar docker
systemctl start docker
systemctl enable docker

#Crear usuario para agregarlo al grupo de docker
adduser paulamoreno

#Agregar el usuario al grupo docker y sudo
usermod -aG sudo $paulamoreno
usermod -aG docker $paulamoreno

#Entrar al usuario
su - paulamoreno

#Descargar imagen nginx version alpine
docker pull nginx:alpine

#Correrla en el puerto 80
docker run -d -p 8080:80 nginx:alpine

#checar los contenedores que están corriendo y ahí estará la imagen
docker ps
