# Builiding complex web app using K8s

# Project Architecture 

![image](https://user-images.githubusercontent.com/5359534/95662476-ddb95080-0b54-11eb-9505-b37d1f7eaeff.png)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Here we required enviromentment variables / secrets to be configured for the multi-server and multi-worker.In the below image yellow one's are constant values and red onces are constant but are URL's to connect the redis and postgres for multi-server, multi-worker and white one represent secrets

![image](https://user-images.githubusercontent.com/5359534/95674596-dafb4180-0bce-11eb-8c87-5362f3712021.png)

Example belowimage shows how multiworker connected to redis

![image](https://user-images.githubusercontent.com/5359534/95674838-67f2ca80-0bd0-11eb-9a4d-2944ea761862.png)

Ingress routing rules as below

![image](https://user-images.githubusercontent.com/5359534/95679638-d431f600-0bf1-11eb-9c45-493f9e79ec88.png)

In this we keep postgres password in the secret 

command to create secret : kubectl create secret <sceret type> <secret name> --from-literal <secretkey>=<secret value>
 
 
Setup ingress controller

 
To setup ingress controller run following command
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.40.2/deploy/static/provider/cloud/deploy.yaml

kubectl get pods -n ingress-nginx


Go to CompleK8s_WebApp_3

kubectl create secret generic pgpassword --from-literal PGPASSWORD=12345asdf

kubectl apply -f k8s

kubectl get pods
 
kubectl get services

kubectl get deployment

kubectl get pv

kubectl get pvc

if we have issue with any object 
kubectl log <pod/deployment/service/pv/pvc> <objectId>

access https://localhost

