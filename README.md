# Kubernetes Practice

## Environment
- [minikube](https://minikube.sigs.k8s.io/docs/start/)
- VirtualBox or Hyper-V or Docker Desktop

### Docker image
Push your image to docker hub
I'm using [this image](https://hub.docker.com/repository/docker/milkcoke/kub-first-app/general)

> Q. Why Do we need pushing docker image to public registry? \
> A. K8S Cluster is separated from local environment. It is required to pull image from public registry like docker hub.


### Quick start
```bash
# Start k8s cluster with driver (You can use also VirtualBox, hyperV)
$ minikube start --driver=docker
# Create deployment using image
$ minikube create deployment first-app --image=[image-name]
```

### View Dashboard
Minikube support dashboard in your local machine with web browser.
```bash
$ minikube dashboard
```

![Dashboard](/assets/minikube-dashboard.png)
