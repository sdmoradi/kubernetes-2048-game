# Kubernetes 2048 Game

Run 2048 game image with selfsigned certificate and nginx image on kubernetes

### About this Senario

* Make custome nginx docker image with docker file 
* Insert 2048 contents in nginx image
* Kubernetes Deployment manifest with replica 2 and service, ingress, selfsined certificate

### Before run 

* You need deploy nginx ingress in your cluster
* You need deploy certmanager in your cluster




#### 1) build docker file in your worker node

```bash
docker build -t saeedbeast/2048:v1.0 .
```

#### 2) push to my repository

```
docker image push saeedbeast/2048:v1.0
```

#### 3) deploy manifest in your kubernetes cluster

```bash
kubectl create -f deployment.yaml
```
