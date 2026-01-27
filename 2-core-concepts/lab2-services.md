## Notes

```bash
# get services
kubectl get service

# find target port, labels, # endpoints etc., of service
kubectl describe svc <service name>

```

### Endpoints
- service directs traffic to correct pod via selector-label match (`endpoints` are the pods that match the selector label)

### service types
- `clusterip` : default. permanent ip to expose to pods inside cluster .
- `node port` : expose the worker node to outside the cluster access.