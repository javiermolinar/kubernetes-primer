## Service hostname

```
kubectl get service/zendesk-service -o jsonpath='{.status.loadBalancer.ingress[0].hostname}'
```

## Namespaces

- Create a namespace: `kubectl create namespace <<name>>`
- Delete a namespace: `kubectl delete namespace <<name>>`

## Deployments

`kubectl describe deployment miro-auth-service`

## Check availability

`kubectl wait pods -n=default -l app=${PROJECT} --for condition=Ready --timeout=30s`

## Create a deployment

`kubectl create deployment first-deployment --image=katacoda/docker-http-server`

## Create a service

`kubectl expose deployment first-deployment --port=80 --type=NodePort`

## Get the yaml of a resource

`k get svc first-deployment -o yaml`

## Get the json of a resource

`k get svc first-deployment -o json`

## JSONPATH

`k get svc first-deployment -o jsonpath='{.spec.ports[0].nodePort}`

## Get exposed port of the new service

`k get svc first-deployment -o yaml | grep nodePort`

`k get svc first-deployment -o jsonpath='{.spec.ports[0].nodePort}`

## How to debug a failing pod
