//minikube version
//minikube start --driver=docker
//minikube status
minikube kubectl -- get pods -A
minikube dashboard
kubectl version --client

minikube automation steps:
minikube start
kubectl create deployment mynginx --image=nginx
kubectl get deployments
kubectl get pods
kubectl describe pods
kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80
kubectl scale deployment mynginx --replicas=4
kubectl get service
kubectl port-forward svc/mynginx 8081:80


http://localhost:8081.


kubectl get svc --output=wide
minikube service mynginx --url


stop nginx deployment:
kubectl delete deployment mynginx
kubectl delete service mynginx
minikube stop


Nagios Automation steps:
docker pull jasonrivers/nagios:latest
docker run --name nagiosdemo -p 8888:80 jasonrivers/nagios:latest
http://localhost:8888
Username: nagiosadmin
Password: nagios
docker ps -a
docker stop nagiosdemo
docker rm nagiosdemo
