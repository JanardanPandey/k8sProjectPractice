# Below Are The Steps That Help To Deploy a applicaiton using kubernets
## This Practice is done with help of https://gitlab.com/nanuchi/k8s-in-1-hour/-/blob/master/mongo-secret.yaml?ref_type=heads

## Install minikube
- sudo install minikube-linux-amd64 /usr/local/bin/minikube
- minikube config set driver docker
- minikube start
- docker info --format '{{.OSType}}'
- minikube start --driver=docker
- alias kubectl="minikube kubectl --"
- kubectl get po -A
- minikube dashboard
  ##  Creating deployments .yaml file inside the kud-demo folder
  - ## First Create *kub-demo* folder and the clone this service inside the folder

- mkdir kub-Demo
- cd kub-Demo
  ### changin the password into the base64 and copy the generated password and past into the mongo-secret file
- echo -n mongopassword | base64
- minikube kubectl -- get pods -A
- sudo minikube kubectl -- get pods -A
- kubeclt get pod
- kubectl apply -f mongo-config.yaml
- kubectl apply -f mongo-serete.yaml
- kubectl apply -f mongo.yaml
- kubectl apply -f webapp.yaml
- kubectl get configmap
- kubectl get secret
- kubectl get log web-deployment-698b9c8545-drzg8 -f
- kubectl log web-deployment-698b9c8545-drzg8 -f
- kubectl logs web-deployment-698b9c8545-drzg8 -f
- kubectl logs web-deployment-698b9c8545-rswlf -f
- minikube get node -o wide
- kubectl get svc
- kubectl get all
- kubectl describe service web-service
- minikube ip
