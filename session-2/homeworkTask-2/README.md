# Kubernetes Service Account Task

# Namespace
kubectl create namespace cloud-engineering

# Service Account
kubectl create serviceaccount cloud-engineers -n cloud-engineering

# Deployment
kubectl create deployment internal-app --image=nginx -n default

# Update Deployment
kubectl patch deployment internal-app -n default \
  --type='json' \
  -p='[{"op": "add", "path": "/spec/template/spec/serviceAccountName", "value":"cloud-engineers"}]'

