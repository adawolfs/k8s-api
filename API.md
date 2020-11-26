
## Obtener Cluster API URL

```
kubectl config view --minify -o jsonpath="{.clusters[].cluster.server}"       
```

## Conectarse al API
Para esto utilizaremos un comando de kubernetes que nos permite crear un proxy entre un pueto local y el Kubernetes API

```
kubectl proxy --port=8080
```

Luego podremos hacer uso de un curl 

```
curl http://localhost:8080/api/
```
