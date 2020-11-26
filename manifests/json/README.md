# Aplicar objetos con CURL

## GET

```
curl -k -v -XGET  -H "Accept: application/json" 'http://127.0.0.1:8080/api/v1/namespaces/hora-de-kubernetes'
```

## FIELD SELECTOR
```
curl -XGET  -H "Accept: application/json" 'http://127.0.0.1:8080/api/v1/namespaces?fieldSelector=metadata.name%3Dhora-de-kubernetes' | jq '.items'
```

## LABEL SELECTOR
```
curl -XGET  -H "Accept: application/json" 'http://127.0.0.1:8080/api/v1/namespaces?labelSelector=speaker%3Dalvin&limit=500' | jq '.items[].metadata.name'
```

## jq
```
curl -XGET  -H "Accept: application/json" 'http://127.0.0.1:8080/api/v1/namespaces' | jq '.items[] | select(.metadata.name == "hora-de-kubernetes")' | jq '.metadata.name'
```

## CREATE
```
curl -k -v -XPOST  -H "Accept: application/json" -H "Content-Type: application/json" 'http://127.0.0.1:8080/api/v1/namespaces' -d @namespace.json
```

## DELETE

```
curl -k -v -XDELETE  -H "Accept: application/json" -H "Content-Type: application/json" 'http://127.0.0.1:8080/api/v1/namespaces/hora-de-kubernetes'
```

## PATCH

```
curl -XPATCH  -H "Accept: application/json" -H "Content-Type: application/merge-patch+json" 'http://127.0.0.1:8080/api/v1/namespaces/hora-de-kubernetes' -d '{
"metadata":{
  "labels":{
    "speaker":"alvin"
  }
}
}
'
```