# Overview
This Pod demonstarates how to configure liveness and readiness for an application running on Kubernetes.

# Requirements / What Was Done
- Pod name: application-probe
- Image: nginx
- Readiness probe calling /started on port 5000
- Liveness probe calling /health on port 5000
- Probes restart or remove the Pod based on HTTP status code

# Probes Explained
Liveness Probe
Check if the application healthy
If /health returns 500 -> Pod is restarted

Readiness Probe
Checks if the application is ready to receive traffic
If /started returns 500 -> Pod is removed from service endpoints.

# How to Apply
kubectl apply -f application-probe.yml
kubectl describe pod application-probe