# Builiding complex web app using K8s

# Project Architecture 

![image](https://user-images.githubusercontent.com/5359534/95662476-ddb95080-0b54-11eb-9505-b37d1f7eaeff.png)

Here we required enviromentment variables / secrets to be configured for the multi-server and multi-worker.In the below image yellow one's are constant values and red onces are constant but are URL's to connect the redis and postgres for multi-server, multi-client.

Go to CompleK8s_WebApp_3

kubectl apply -f k8s

kubectl get pods
 
kubectl get services

kubectl get deployment

kubectl get pv

kubectl get pvc

if we have issue with any object 
kubectl log <pod/deployment/service/pv/pvc> <objectId>

