# Examen 3 - Servicio Telemático con Docker

## Descripción
Servicio web desplegado en contenedor Docker corriendo en AWS EC2 con balanceador de carga.

## Requisitos
- Docker instalado en la máquina objetivo
- Git para clonar el repositorio

## Cómo desplegar en un servidor de producción (AWS)

1. **Conectar a la instancia EC2** por SSH

2. **Instalar Docker**:
   ```bash
   sudo apt update && sudo apt install docker.io -y

3. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/sofiaespinosab/Examen3.git
   cd Examen3
   
4. **Construir la imagen Docker**:

   ```bash
   sudo docker build -t examen3 .
   
5. **Ejecutar el contenedor (persistente)**:

   ```bash
   sudo docker run -d -p 80:80 --restart unless-stopped --name webapp examen3
6. **Verificar**:

   ```bash
   sudo docker ps
Escalabilidad
El servicio es escalable usando un Application Load Balancer de AWS que distribuye el tráfico entre múltiples instancias con el mismo contenedor.

Autor
Sofia Espinosa Bedoya.
