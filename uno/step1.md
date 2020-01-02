Create Build
`docker build -t mlflow-docker-example -f Dockerfile .`{{execute}}

Create the Docker network that is used to run the Confluent containers.
`mlflow run . --backend kubernetes --backend-config examples/docker/kubernetes_config.json`{{execute}}
