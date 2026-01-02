## Checklist for local clusters
### Requirements
- docker desktop (with k8 enabled; point to default `kubeadm` option is fine)
- kubectl
- kind

### Run Local cluster with Kind (k8 in docker)
```bash
# create cluster
kind create cluster --name local-dev

# verify
kubectl get nodes
```

### Apply Manifest
- sends manifest (EX: pod) to k8 api server
```bash
kubectl apply -f pod.yaml   
```

### Check state of Pod
- using nginx as example pod name

- get general pod details
```bash
kubectl describe pod nginx
```
- get the logs of the pod
```bash
kubectl logs nginx
```

### Check local cluster and delete
- pretty self explanatory
```bash
kind get clusters
kind delete cluster --name <cluster-name>
```