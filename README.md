# Kubernetes Training

This setup based on:

- [Hello World](https://github.com/cleaniquecoders/docker-php-hello-world.git)
- [Getting Started App](https://github.com/cleaniquecoders/getting-started-app.git)

## Usage

Make sure to install [minikube](https://minikube.sigs.k8s.io/docs/start/).

Start minikube:

```bash
minikube start
```

Run the dashboard:

```bash
minikube dashboard
```

Load Local Image into minikube

```bash
minikube image load getting-started:latest
minikube image load hello-world:php8.3
```

Then do add the deployment and service.

In order to access from your browser, you need to [port forward](https://kubernetes.io/docs/tasks/access-application-cluster/port-forward-access-application-cluster/) the container port:

```bash
kubectl port-forward service/getting-started 3000:3000
kubectl port-forward service/hello-world 8083:80
```
