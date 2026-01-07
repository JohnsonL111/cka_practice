### MISC Notes for lab 2 on pods
- helpful cli commands in lab

```bash
# list pods in default namespace
kubectl get pods -n default

# list pods in all namespaces
kubectl get pods --all-namespaces

# creates the pod as a deployment
# pod name is nginx
kubectl run nginx-pod --image=nginx 

# create a new pod using nginx image
# --restart=Never flag ensures the pod isn't managed by controller
# pod name is nginx-pod
kubectl run nginx-pod --image=nginx --restart=Never

# pulls up the pod spec
kubectl describe pod <pod-name>

# list node that each pod is on
kubectl get pods -o wide

# delete pod
kubectl delete pod webapp
```
- `ImagePullBackOff` error in pod log means k8 having troubke pulling the container img from registry.
- could be invalid img name, tag, credentials, or netowrk issues