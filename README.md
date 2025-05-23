# kustomize-configs
1. Using overlay, generate k8s resource files ( deployment and service ) for two environments ( dev and stg )
1. Specify namespace, resource-name prefix for respective environment ( dev and stg )

# usage
```
kustomize build mock-email-service/overlays/dev/
kustomize build mock-email-service/overlays/stg/
```
Now, review the generated resources and then Apply

```
kubectl apply -k mock-email-service/overlays/dev/
kubectl apply -k mock-email-service/overlays/stg/
```

