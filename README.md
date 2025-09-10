# k8-deploy-strategies

## recreate strategy
```sh
    git clone https://github.com/geksogen/k8-deploy-strategies.git
    cd ./k8-deploy-strategies/recreate
    kubectl apply -f app-v1.yaml
    # see <IP-Node:31758>
```
### test app
```sh
    while true; do curl http://89.169.149.118:31758; sleep 0.1; done ## delete \ sumbol :)
```

### change version
```sh
   kubectl apply -f app-v2.yaml && watch -n 1.5 kubectl get pod
```

### clear
```sh
   kubectl delete deployment my-app
```

## ramped strategy
```sh
    cd ../ramped
    kubectl apply -f app-v1.yaml
    # see <IP-Node:31758>
```
