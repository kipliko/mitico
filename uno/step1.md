Clone MLFlow project
`git clone https://github.com/kipliko/mlflow-test.git`{{execute}}

`cd mlflow-test`{{execute}}

Create Build
`docker build -t mlflow-docker-example -f Dockerfile .`{{execute}}

Install MLFlow
`pip install mlflow`{{execute}}


Create the Docker network that is used to run the Confluent containers.
`mlflow run https://github.com/kipliko/mlflow-test.git --backend kubernetes --backend-config examples/docker/kubernetes_config.json`{{execute}}

Varie:
Lista dei nodi: `kubectl get nodes`{{execute}}

Lista dei pods: `kubectl get pods`{{execute}}

Lista dei services: `kubectl get services`{{execute}}