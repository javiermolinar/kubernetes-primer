## Service hostname

```
kubectl get service/zendesk-service -o jsonpath='{.status.loadBalancer.ingress[0].hostname}'
```

## Namespaces

- Create a namespace: `kubectl create namespace <<name>>`
- Delete a namespace: `kubectl delete namespace <<name>>`
