
# Laboratorio Ansible con Docker

## Objetivo de la práctica

Crear dos servidores Linux utilizando Docker y administrarlos con Ansible. En esta práctica se automatizan algunas tareas básicas, como consultar información de los servidores, crear directorios y generar archivos.

## Iniciar los contenedores

Para crear e iniciar los dos servidores, ejecutar el siguiente comando:

```bash
docker compose up -d
```

Para comprobar que los contenedores estén funcionando:

```bash
docker ps
```

## Ejecutar el Playbook

Desde la carpeta del proyecto, ejecutar:

```bash
ansible-playbook -i inventory.ini playbook.yml
```

El Playbook realiza las siguientes tareas en ambos servidores:

- Muestra el nombre del servidor y su sistema operativo.
- Crea el directorio `ansible-demo`.
- Genera el archivo `info.txt` con información del servidor.
- Crea las carpetas `logs`, `backup` y `config`.
- Muestra un mensaje cuando detecta que el sistema operativo es Ubuntu.

## Captura de la ejecución

En la siguiente imagen se muestra la ejecucion del Playbook y el resultado en los dos servidores.
[Ejecucion del Playbook](screenshots/ejecucion.png)
