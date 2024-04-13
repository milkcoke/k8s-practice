# Kubernetes Practice

## Environment
Docker desktop

### Docker image
Push your image to docker hub
I'm using [this image](https://hub.docker.com/repository/docker/milkcoke/kub-first-app/general)

> Q. Why Do we need pushing docker image to public registry? \
> A. K8S Cluster is separated from local environment. It is required to pull image from public registry like docker hub.


### Quick start
```bash
$ kubectl proxy
```
You can use dashboard on `http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy`

![Dashboard](/assets/minikube-dashboard.png)


# Resources

## Namespace
All resource of k8s has separated by namespace.
![Namespace](/assets/kubernetes-namespace.png)

```bash
$ kubectl apply -f deployment-a.yaml # has namespace 'a'

$ kubectl apply -f deployment-b.yaml # has namespace 'b'

$ kubectl get deployment --all-namespaces
```

```plaintext
NAMESPACE              NAME                        READY   UP-TO-DATE   AVAILABLE   AGE
a                      hello-kaimol-4              1/1     1            1           3m43s
b                      hello-kaimol-4              1/1     1            1           3m38s
```
