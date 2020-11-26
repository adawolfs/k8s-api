# Kubernetes API

Demo de Kubernetes API para la Hora de Kubernetes, esta demo busca demostrar como conectarse al k8s API sin utilizar `kubectl` o alguna libreria.

## Documentacion y Referencias
- [Kubernetes API (Español)](https://kubernetes.io/es/docs/concepts/overview/kubernetes-api/)
- [Kubernetes API Concepts](https://kubernetes.io/docs/reference/using-api/api-concepts/)
- [Kubernetes Supports OpenAPI](https://kubernetes.io/blog/2016/12/kubernetes-supports-openapi/)
- [Kubernetes API Conventions](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md)
- [Kubernetes API Overview](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#-strong-api-overview-strong-)
- https://www.youtube.com/watch?v=dajYTUoCEGw
- https://www.youtube.com/watch?v=QtXHkzLtqZE


## Conectarse al API
Para esto utilizaremos un comando de kubernetes que nos permite crear un proxy entre un pueto local y el Kubernetes API

```
kubectl proxy --port=8080
```

Luego podremos hacer uso de un curl 

```
curl http://localhost:8080/api/
```


## Presentación

[Haz click aquí](https://docs.google.com/presentation/d/1LYIQfoqnA4zedyuxYpQSP-p6ehUwO7lc-IOakHa1JOA/edit?usp=sharing)