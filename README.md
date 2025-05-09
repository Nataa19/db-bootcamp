# db-bootcamp
Proyecto de Base de Datos Postgres conformado en Docker-Compose 

1. **Creamos una carpeta llamada "db-bootcamp"**

`mkdir db-bootcamp`
`cd db-bootcamp`

2. **Crea un archivo llamado docker-compose.yml en el directorio.**

`vim compose.yaml`

3. Configurar el servicio **postgres** de base de datos con una imagen de PostgreSQL dentro de docker-compose.yml para poder utilizarlo e interactuar con el contenedor.

Usaremos el siguiente compose:

	`services:`
	  `postgres:`
	    `image: postgres:latest`
	    `restart: no`
	    `shm_size: 128mb`
	    `environment:`
	      `POSTGRES_DB: natadb`
	      `POSTGRES_USER: nata`
	      `POSTGRES_PASSWORD: nata`
	    `volumes:`
	      `- postgres_data:/var/lib/postgresql/data`
	
	`volumes:`
	  `postgres_data:`

