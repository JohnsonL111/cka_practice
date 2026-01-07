### MISC Notes for lab 2 on deployments
- helpful cli commands in lab

```bash
# GET ALL objects
kubectl get all 

# Apply any manifest changes
kubectl apply -f <manifest>

```

- in the exam try not to waste time scaffolding manifests
- use the cli to generate the spec for you ex:

```bash
# Create an NGINX Pod

kubectl run nginx --image=nginx

# Generate POD Manifest YAML file (-o yaml). Don't create it(--dry-run)
# kubectl run <name> --image=nginx --dry-run=client -o yaml
# -o specifies the output of the manifest (yaml)
# dry run specifies it will create the manifest but not send data the api
kubectl run nginx --image=nginx --dry-run=client -o yaml

# Create a deployment

kubectl create deployment --image=nginx nginx

# Generate Deployment YAML file (-o yaml). Don't create it(--dry-run)

kubectl create deployment --image=nginx nginx --dry-run=client -o yaml

# Generate Deployment YAML file (-o yaml). Don’t create it(–dry-run) and save it to a file.

kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml

# Make necessary changes to the file (for example, adding more replicas) and then create the deployment.

kubectl create -f nginx-deployment.yaml

```