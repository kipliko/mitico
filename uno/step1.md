Clone MLFlow project
`git clone https://github.com/kipliko/mlflow-test.git`{{execute}}

`cd mlflow-test`{{execute}}

Login into DockerHub
`docker login --username=pscarpino --password-stdin`{{execute}}

Create Build
`docker build -t pscarpino/mlflow-docker-example -f Dockerfile .`{{execute}}

Push image on dockerhub.
`docker push pscarpino/mlflow-docker-example`{{execute}}

Install MLFlow
`pip install mlflow`{{execute}}
`pip install kubernetes`{{execute}}

Launch Kubernates job:
`kubectl apply -f mlflow-test/test_kubernetes_job_template.yaml`{{execute}}

Create the Docker network that is used to run the Confluent containers.
`mlflow run https://github.com/kipliko/mlflow-test.git --backend kubernetes --backend-config mlflow-test/kubernetes_config.json`{{execute}}

Varie:
Lista dei nodi: `kubectl get nodes`{{execute}}

Lista dei pods: `kubectl get pods`{{execute}}

Lista dei services: `kubectl get services`{{execute}}