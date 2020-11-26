# MYSQL
## CREATE

```
curl -k -v -XPOST  -H "Accept: application/json" -H "Content-Type: application/json" 'http://127.0.0.1:8080/api/v1/namespaces/default/services' -d @service.json 

curl -XPOST  -H "Accept: application/json" -H "Content-Type: application/json" 'http://127.0.0.1:8080/apis/apps/v1/namespaces/default/deployments' -d @deployment.json 
```

## DELETE

```
curl -k -v -XDELETE  -H "Accept: application/json" -H "Content-Type: application/json" 'http://127.0.0.1:8080/apis/apps/v1/namespaces/default/deployments/wordpress'
```
