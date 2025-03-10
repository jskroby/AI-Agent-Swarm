## AI-Agent-Swarm Project Repository

## 🇨 Getting Started

Please start by following these steps:

### 1💭 Install Dependencies

All necessary dependencies can be installed using:
```sh
pip install -r requirements.txt
```

### 2📴 Run Locally

```sh
python3 src/swarm.py
```

### 3🜰Run with Docker

```sh
docker build -t ai-agent-swarm \
 docker run --rm -p 80:80 ai-agent-swarm
```

### 4���� Deploy to Kubernetes

```sh
kubectl apply -f deployments/configmap.yaml
kubectl apply -f deployments/deployment.yaml
kubectl apply -f deployments/service.yaml
```

## 🟏  Debugging

<## 🗤 Check Logs
```sh
kubectl logs -f <pod_name>
```

## 🗤 Enter Docker Container
```sh
docker exec -it <container_id> /bin/bash
```

## 🟒 Check Kubernetes Events

```sh
kubectl get events --sort-by=.metadata.creationTimestamp
```

## 🟐 Restart Pods

Scale down and restart for a new deployment:
```sh
kubectl Scale Deployment ai-agent-swarm --replicas=0
kubectl Scale Deployment ai-agent-swarm --replicas=3
```
