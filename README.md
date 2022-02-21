# Instructions

You will need kubectl and minikube.

```bash
$ kubectl create -f nginx-deployment.yaml
```

```bash
$ kubectl get deployments
```

```bash
$ kubectl describe deployments nginx-deployment
```

```bash
$ kubectl get services
```

```bash
$ kubectl describe services nginx-service
```

```bash
$ minikube ip
```

```bash
$ curl iphere:porthere/
```

Then head to the url in your browser to see a fresh Nginx service running.

## Dashboard

Minikube command for accessing the Kubernetes dashboard running within the Minikube cluster.

```bash
$ minikube dashboard
```

### Troubleshooting

By default, your clusterrolebinding has system:anonymous set which blocks the cluster access.

Execute the following command, it will set a clusterrole as cluster-admin which will give you the required access.

```bash
$ kubectl create clusterrolebinding cluster-system-anonymous --clusterrole=cluster-admin --user=system:anonymous
```
