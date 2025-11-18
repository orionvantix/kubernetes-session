# Kubernetes Service Account Task

# 1. Namespace
Created the namespace:
kubernetes create namespace cloud-engineering

# 2. Service Account
Created the service account:
kubectl create serviceaccount cloud-engineering -n cloud-engineering

# 3. Deployment
Created the deployment in the default namespace:
kubectl create deployment internal-app --image=nginx -n default

# 4. Update Deployment
Mover
