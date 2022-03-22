Get worker nodes:

```
kubectl get nodes
```

Create a deployment:

```
kubectl create deployment --image jbrosas/node-hello-app node-app
```

Scale up to 3 replicas:

```
kubectl scale deployment node-app --replicas 3
```

Expose the deployment as a NodePort replica:

```
kubectl expose deployment node-app --type=NodePort --port 3000
```

Look at the newly created service (and the assigned port):

```
kubectl get services
```

Grab the public IP of one of the worker nodes:

```
kubectl get nodes -o wide
```

Browse to IP:port to test the service
Edit the service:

```
kubectl edit service node-app
```

Replace port: 3000 with port: 80
Replace type: NodePort with type: LoadBalancer
Verify that the service was updated:

```
kubectl get service
```

Shutdown pods:

```
kubectl scale deployment node-app --replicas 0
```

Check the running pods:

```
kubectl get pods
```
