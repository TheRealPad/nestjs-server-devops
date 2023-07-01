# nestjs-server-devops
simple server to train my devops skills

## launch server with docker

```bash
docker build -t {{ name }} .
docker run -p{{ port }}:3000 {{ name }}
```

## Access app using kubernetes

First, you must have your docker image running with the following name : ```nest-cloud-run```

then you can run :

```bash
kubectl apply -f kubernetes/namespace.yaml
kubectl apply -f kubernetes/deployment.yaml -n beta
```

The application is available [here](http://localhost:8000/)
