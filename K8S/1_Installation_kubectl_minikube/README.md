
# K8S Installation d'un environnement de test
> Compétences : 

## Installation sur Ubuntu 20

### Mise à jour des paquets   

    sudo apt update

### Installer Kubectl
https://kubernetes.io/fr/docs/tasks/tools/install-kubectl/

```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && chmod +x kubectl
sudo cp kubectl /usr/local/bin/.
```

### Installer Minikube
https://minikube.sigs.k8s.io/docs/start/

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
 ```


### Version

    minikube version


Votre environnement de test Kubernetes est installé.