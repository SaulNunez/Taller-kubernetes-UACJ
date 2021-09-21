# Introduccion a Kubernetes

## Glosario
Cluster
Es un grupo de maquinas que corren aplicaciones contenerizadas.

### Node
Asi se le llama a la maquina de Kubernetes, un nodo puede ser virtual o fisico.

Se puede ver nodos ejecutandose en:
```bash
kubectl get nods
```

### Pod
Es la unidad mas pequeña que existe en Kubernetes, un pod contiene una sola instancia de un proceso que corre en el cluster.

Ver pods actuales
```bash
kubectl get pods -o wide
```

Para borrar, cualquiera de los siguientes:
```bash
kubectl delete pod/gpod

kubectl delete -f MI_ARCHIVO.yaml
```
Para manejar deploys:
```bash
kubectl apply -f MI_ARCHIVO.yaml
```

### Volumen
Un directorio que contiene datos y es accesible desde el contenedor

### Container
Es un empaquetado que contiene dependiencias y librerias.

### Image
Es una instantanea de un contenedor

### Docker Hub
Es un repositorio de imagenes, en el cula puedes subir las imagenes que generes

### Kubectl
Cliente o programa usado para gestionar los recursos en Kubernetes.

### Deployment
Se encargan de mantener versiones.

### ReplicaSet
Intenrara mantener un estado deseable, se encarga de la estabilidad de los contenedores. Ej. manejas varios contenedores del mismo tipo para manejar volumenes cambiantes de transacciones.
