# Kubernetes

## Main commands
@tags: kubernetes kubectl

```
# Show all pods
$ kubectl get pods --all-namespaces

# Show all pods from one namespace
$ kubectl -n orderer get pods

# Show logs
$ kubectl -n orederer logs <pod name>

# Delete a namespace
$ kubectl delete namespace <namespace>

# Show all ressources
$ kubectl ge all --all-namespaces

# Show env variables
$ kubectl describe pods <pod name> -n org-1
```
