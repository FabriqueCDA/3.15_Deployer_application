
# Minikube
> Compétences : 

## Commandes de base
https://minikube.sigs.k8s.io/docs/commands/

### Version

    minikube version


### Démarrer le custer Kubernetes

    minkube start

### Informations

    minikube status


### Démarrer le dashboard

Ouvrir un nouveau terminal pour lancer le dashboard

    minikube dashboard


### Pause de Kubernetes

    minikube pause

### Unpause de Kubernetes

    minikube unpause


### Arrêt de Kubernetes

    minikube stop



### Supprime le cluster local

    minikube delete


### Supprime l'ensemble des clusters locaux

    minikube delete


### Supprime l'ensemble des clusters locaux

    minikube delete --all


### Connaitre l'ip du cluster

    minikube ip


### Liste des AddOns

    minikube addons list

Pour spécifier le nom du cluster

    minikube addons -p NomDuCluster list

### Activer l'AddOn des metrics

    minikube addons enable metrics

Les metrics sur les Nodes seront visible dans le Dashboard
