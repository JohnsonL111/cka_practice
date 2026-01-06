### MISC Notes for lab 2 on replica sets
- helpful cli commands in lab

```bash
# get number of replicasets in current namespace
kubectl get rs
# output is 1 rs overseeing 4 pods
# NAME              DESIRED   CURRENT   READY   AGE
# new-replica-set   4         4         0       30s

# get image details (look at its template)
kubectl describe replicaset

# create replicaset
kubectl create -f /root/replicaset-definition-1.yaml

# scale expected pods
kubectl scale --replicas=5 replicaset new-replica-set
```