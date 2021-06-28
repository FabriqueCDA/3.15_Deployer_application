
# Exposer une application


## Création d'un Pod deployer une image depuis google 
kubectl create deployment kubernetes-bootcamp --image=gcr.io/google-samples/kubernetes-bootcamp:v1

ou un node.js Hello World
kubectl create deployment hello-world1 --image=bonomat/nodejs-hello-world
https://hub.docker.com/r/bonomat/nodejs-hello-world
https://github.com/bonomat/nodejs-hello-world-docker/blob/master/Dockerfile


## Exposer une application

Cela consiste à permettre d'accéder à l'application par un port, donc d'exposer un port.

### Lister les déploiement
    kubectl get deployments

### Maintenant créer un service pour exposer le port de du déploiement que vous voulez exposer

    kubectl expose deployment/<nom_du_deploiement> --type="NodePort" --port <port_de_l_application>

### Lister les services, il devrait être dans la liste

   kubectl get service

### Afficher les informations sur le service

   kubectl describe services/<nom_du_service>

Veuillez retenir la valeur de <NodePort> et tester si l'application est accessible par ce port avec curl

   curl $(minikube ip):<NodePort>

Vous pouvez tester dans votre navigateur cette adresse:

   $(minikube ip):<NodePort>



## Les labels

### Vous pouvez-voir les noms des labels avec:

    kubectl describe deployment

### Lister les pods par leur label

   kubectl get pods -l app=<nom_label>

### Lister les services par le label

    kubectl get services -l app=<nom_label>

### Ajouter un label "version v1" au pod

    kubectl label pods <nom_du_pod> version=v1


### Vérification du label version

    kubectl get pods -Lapp -Lversion
