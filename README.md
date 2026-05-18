# Examen 3 - Servicio Telemático con Docker

## Descripción
Servicio web desplegado en contenedor Docker usando nginx, corriendo en AWS EC2 con balanceador de carga.

## Requisitos
- Docker instalado en la máquina objetivo
- Git para clonar el repositorio

## Cómo desplegar en un servidor de producción (AWS)

1. **Conectar a la instancia EC2** por SSH

2. **Instalar Docker**:
   ```bash
   sudo apt update && sudo apt install docker.io -y
