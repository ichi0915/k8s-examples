
# K8s Examples

This repo has some kubernetes config files use to study for the Kubernetes Certified Application Developer (CKAD)

## Common/Useful commands:

Get all the pods, services, statefulsets, etc.
```Bash
kubectl get all
```

Get all the namespaces:
```Bash
kubectl get ns
```

Create a namespace:
```Bash
kubectl create ns <namespace-name>
```

Apply/Create a K8s manifest:
```Bash
kubectl -n <namespace-name> apply -f <file>
kubectl apply -f <file>
kubectl create -f <file>
```

Describe a resource:
```Bash
kubectl -n <namespace-name> describe <kind> <name>
```

Show pod logs:
```Bash
kubectl -n <namespace-name> logs <pod-name>
```

Exec a pod sh:
```Bash
kubectl -n <namespace-name> exec -it <pod-name> -- sh
```

Delete a resource:
```Bash
kubectl -n <namespace-name> delete <kind> <name>
kubectl delete <kind> <name>
kubectl delete -f <file>
```

Get nodes ip:
```Bash
kubectl get nodes -o wide
```

Apply kustomization.yaml:
```Bash
kubectl apply -k .
or
kustomize build . | kubectl apply -f -
```
