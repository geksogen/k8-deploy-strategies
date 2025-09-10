### Building, push and run
```sh
    docker build -t myapp .
    docker tag myapp:latest geksogen/k8-deploy-strategies:v1
    docker push geksogen/k8-deploy-strategies:v1  
    docker run -d --name myapp-container -p 8080:8080 geksogen/k8-deploy-strategies:v1 
    
```