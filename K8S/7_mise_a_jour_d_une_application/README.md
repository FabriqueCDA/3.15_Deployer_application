# Dupliquer une application / Scalabilité


## Création d'un Pod deployer une image depuis google 
kubectl create deployment kubernetes-bootcamp --image=gcr.io/google-samples/kubernetes-bootcamp:v1

ou un node.js Hello World
kubectl create deployment hello-world1 --image=bonomat/nodejs-hello-world
https://hub.docker.com/r/bonomat/nodejs-hello-world
https://github.com/bonomat/nodejs-hello-world-docker/blob/master/Dockerfile


## Lancer 5 fois la même application, donc 5 pods

### Lister les déploiement
    kubectl get deployments

### Afficher le replicaset

    kubectl get rs

### Dupliquer une des image de déploiement
 
    kubectl scale deployments/<nom_image> --replicas=5

Vérification

    kubectl get rs 

Liste des pods avec leurs Ip
    
    kubectl get pods -o wide


## Véririfcation du Load Balancing



## Scale down

### Diminuer le replicas à 3 pods
 
    kubectl scale deployments/<nom_image> --replicas=3

Vérification

    kubectl get rs 

Liste des pods avec leurs Ip
    
    kubectl get pods -o wide