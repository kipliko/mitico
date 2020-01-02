Create Build
`docker build -t mlflow-docker-example -f Dockerfile .`{{execute}}

Create the Docker network that is used to run the Confluent containers.
`mlflow run . --backend kubernetes --backend-config examples/docker/kubernetes_config.json`{{execute}}

Varie:
Lista dei nodi: `kubectl get nodes`{{execute}}
Lista dei pods: `kubectl get pods`{{execute}}
Lista dei services: `kubectl get services`{{execute}}