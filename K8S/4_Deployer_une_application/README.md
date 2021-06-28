
# Déployer une application
https://kubernetes.io/docs/tutorials/kubernetes-basics/

### Image docker google

## Création d'un Pod deployer une image depuis google 
kubectl create deployment kubernetes-bootcamp --image=gcr.io/google-samples/kubernetes-bootcamp:v1

ou un node.js Hello World
kubectl create deployment hello-world1 --image=bonomat/nodejs-hello-world
https://hub.docker.com/r/bonomat/nodejs-hello-world
https://github.com/bonomat/nodejs-hello-world-docker/blob/master/Dockerfile


## Verifier l'état du pods

    kubectl get deployments

## Voir les containers d'un pod et les images utilisées

    kubectl describes pods     

## Voir les logs d'un pod

    kubectl logs <nom_du_pod> 

## Afficher les variable d'environnement du container

    kubectl exec <nom_du_pod> -- env  

## Afficher le bash du container dans le pod

    kubectl exec -ti <nom_du_pod> -- bash  

## Effacer un pod

     kubectl delete pod <nom_du_pod>


## Effacer un deploiement

     kubectl delete deployment <nom_du_deploiement>



## Accéder à l'api de Kubernetes

Ouvrir un nouveau terminal
    kubectl proxy

L'API est maintenant accessible sur le port 8001 en local, afficher la version de l'api kubernetes:

    curl http://localhost:8001/version

