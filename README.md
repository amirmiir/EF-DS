# EF-DS
---
## Estructura del proyecto
```bash
.
├── initdb
├── kubernetes
├── legacy-app
├── logs
├── new-microservice
├── operate.sh
└── README.md
```

---
## Instrucciones para inicializar el proyecto
Archivo ejecutable para ejecutar el orquestrador k8s

```bash
chmod +x operate.sh
bash operate.sh # o ./operate.sh
```
---
## Documentación
### Directorio `/legacy-app`:
Para este directorio tenemos la siguiente estructura:
```bash
.
├── Dockerfile
├── legacy-app.py
└── requirements.txt
```
En este directorio tenemos una simulación de aplicación en Python, un archivo Dockerfile y los requerimientos para ejecutar nuestra aplicación.

El flujo de trabajo del Dockerfile [1] es crear una instancia de python:3.9-slim, [2] cambiar de directorio, [3] instalar las dependencias copiadas y [4] levantar la aplicación.

### Directorio `new-microservice`:
Para este directorio tenemos la siguiente estructura:
```bash
.
├── Dockerfile
└── new-app.py
```
En este directorio tenemos una simulación de aplicación en Python y un archivo Dockerfile. Notemos que también se puede agregar un archivo de requisitos, pero este requeriría instalar `pip`, a través de `RUN python3 -m ensurepip`. Dado que queremos mantener la imagen lo más pequeña posible, evitamos este paso.

### Directorio `/initdb`:
Para este directorio tenemos la siguiente estructura:
```bash
.
├── Dockerfile
└── new-app.py
```

Estamos trabajando con una base de datos en Postgres.


### Directorio `/kubernetes`:

### Directorio `/.github/workflows`:
### Directorio `/logs`:
