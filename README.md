### Informacion personal

Nombre: Alex Vega Bendezu

Correo institucional: alex.vega.b@uni.pe

### Informacion del proyecto

Titulo: Observabilidad de clúster Kubernetes local (mini-monitoring)

Url del repositorio grupal: [https://github.com/grupo10-CC3S2/Proyecto7-PC4](https://github.com/grupo10-CC3S2/Proyecto7-PC4)



### Instrucciones

- Clonar el repositorio individual

```sh
git clone https://github.com/axvg/pc4-proyecto07-alexvega
cd pc4-proyecto07-alexvega
```

- Para la facilidad de ejecucion y despliegue de pods de Kubernetes se puede usar Makefile.

- Para el **sprint 1**, se debe ejecutar:

Crear la imagen con el tag correcto:

```sh
docker build -t timeserver:latest archivos/sprint1/app
```

Luego crear los recursos de Kubernetes:

```sh
kubectl cluster-info
kubectl apply -f k8s/
kubectl get pods
```


- Para el **sprint 2**, se debe ejecutar los comandos del archivo makefile:

```sh
make setup
```
Para el uso de fluxcd:

```sh
make flux-init
make flux-creater
make flux-createk
```

Esto creara los archivos de configuracion de fluxcd y los aplicara al cluster.
Nota: se debe cambiar la variable repo al repositorio actual.

- Para el **sprint 3**, se debe ejecutar pytest dentro de entorno virtual:

```sh
python3 -m venv .venv
source .venv/bin/activate
pytest
```

Como se usa un archivo de configuracion de pytest `pytest.ini`, este no necesita ningun argumento.