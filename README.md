## AI-Agent-Swarm Project Repository

## ð¨ Getting Started

Please start by following these steps:

### 1ð­ Install Dependencies

All necessary dependencies can be installed using:
```sh
pip install -r requirements.txt
```

### 2ð´ Run Locally

```sh
python3 src/swarm.py
```

### 3ð°Run with Docker

```sh
docker build -t ai-agent-swarm \
 docker run --rm -p 80:80 ai-agent-swarm
```

### 4ø· Deploy to Kubernetes

```sh
kubectl apply -f deployments/configmap.yaml
kubectl apply -f deployments/deployment.yaml
kubectl apply -f deployments/service.yaml
```

## ð  Debugging

<## ð¤ Check Logs
```sh
kubectl logs -f <pod_name>
```

## ð¤ Enter Docker Container
```sh
docker exec -it <container_id> /bin/bash
```

## ð Check Kubernetes Events

```sh
kubectl get events --sort-by=.metadata.creationTimestamp
```

## ð Restart Pods

Scale down and restart for a new deployment:
```sh
kubectl Scale Deployment ai-agent-swarm --replicas=0
kubectl Scale Deployment ai-agent-swarm --replicas=3
```
