# Practica 8: Uso de Ansible para automatizar tareas en servidores

## Objetivo

Crear 5 servidores Ubuntu (contenedores Docker con SSH) y usar Ansible para automatizar: actualizar el cache de APT, crear el usuario itla, crear la carpeta app con el archivo hola.txt, e instalar cowsay y htop.

## Iniciar los servidores

```bash
docker compose up -d --build
docker ps
```

## Probar la conexion

```bash
docker exec -it ansible-control ansible all -m ping
```

## Ejecutar el playbook

```bash
docker exec -it ansible-control ansible-playbook playbook.yml
```

## Captura de la ejecucion exitosa

![Ejecucion exitosa del playbook](captura.png)

## Limpiar

```bash
docker compose down
```