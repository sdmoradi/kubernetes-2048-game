# Kubernetes 2048 Game

Run 2048 game image with selfsigned certificate and nginx image on kubernetes

### About this Senario

* Make custome nginx docker image with docker file 
* Insert 2048 contents in nginx image
* Kubernetes Deployment manifest with replica 2 and service, ingress, selfsined certificate

### Before run 

* You need deploy nginx ingress in your cluster
* You need deploy certmanager in your cluster


#### 0) For deploy certmanager in your cluster use bellow command

```
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml
```


#### 1) Build docker file

```bash
docker build -t sdmoradi/2048:v1.0 .
```

#### 2) Push to your docker registry

```
docker image push sdmoradi/2048:v1.0
```

#### 3) Deploy manifest in your kubernetes cluster

```bash
kubectl create -f deployment.yaml
```
