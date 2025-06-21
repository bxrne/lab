# lab

Homelab for learning kubernetes. Running a single node cluster via minikube.

## Prerequisites

- [minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [docker](https://docs.docker.com/get-docker/) # Cluster runs in a docker container
- [k9s](https://k9scli.io/) (optional) - A terminal UI to interact with Kubernetes clusters


## Usage
1. Start minikube:
   ```bash
   minikube start --driver=docker
   ```
2. Set up kubectl to use the minikube context:
   ```bash
   kubectl config use-context minikube
   ```

3. Apply the resource:
   ```bash
   kubectl apply -f NAME/
   ```

4. Check the status of the pods:
   ```bash
   kubectl get pods
   ```

5. Access the service:
   ```bash
   minikube service NAME --url
   ```

6. Port forwarding:
   ```bash
   kubectl port-forward service/NAME 8080:80
   ```

6. Stop cluster:
   ```bash
   minikube stop
   ```

7. Delete cluster:
   ```bash
   minikube delete
   ```

