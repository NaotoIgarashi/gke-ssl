# Gettig started

## Create k8s cluster, deployment and service

```
gcloud container clusters create https-demo-cluster --zone asia-northeast1-a --machine-type g1-small --num-nodes 1
kubectl apply -f .\deployment.yaml
kubectl apply -f .\service.yaml
```

## Create ip address

```
gcloud compute addresses create https-demo-ip --global
gcloud compute addresses list
```

## Create managed SSL certificate

```
kubectl apply -f .\certificate.yaml
```

## Apply ingress

```
kubectl apply -f .\ingress.yaml
```