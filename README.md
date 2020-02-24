[![Build Status](https://travis-ci.com/muttalebm/cloud-developer-microservices.svg?branch=master)](https://travis-ci.com/muttalebm/cloud-developer-microservices)
# cloud-developer-microservices
## Github link:
``https://github.com/muttalebm/cloud-developer-microservices``
## Dockerhub Link:
```https://hub.docker.com/u/muttalebm```
```https://hub.docker.com/r/muttalebm/udacity-frontend```
```https://hub.docker.com/r/muttalebm/udacity-reverse-proxy```
```https://hub.docker.com/r/muttalebm/udacity-restapi-feed```
```https://hub.docker.com/r/muttalebm/udacity-restapi-user```

## Kubernetes Deployment
Created Kubernetes cluster using minikube

`minikube start --cpu=4 --memory=8192`

Create Your own secret and config file
```
mv udacity-c3-deployment/k8s/samples/aws-secret-sample.yaml udacity-c3-deployment/k8s/aws-secret.yaml
mv udacity-c3-deployment/k8s/samples/env-secret-sample.yaml udacity-c3-deployment/k8s/env-secret.yaml
mv udacity-c3-deployment/k8s/samples/env-configmap-sample.yaml udacity-c3-deployment/k8s/env-configmap.yaml
```
for
Deploy application using services and deployment

```kubectl apply -f udacity-c3-deployment/k8s```

Check Cluster status

```kubectl get all```

Expose frontend and reverse proxy through port forward
```
    kubectl port-forward service/reverseproxy 8080:8080
    kubectl port-forward service/frontend 8100:8100
```