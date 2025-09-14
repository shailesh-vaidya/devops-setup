# DevOps Tools Deployment on Kubernetes

This repository provides automated deployment manifests and sample CI/CD pipelines for popular DevOps tools on Kubernetes clusters. It aims to simplify the setup of a complete DevOps environment with minimal manual intervention.

---

## Included Tools

- Jenkins
- Gitea (Git service)

---

## Deployment Steps

1. Install a Kubernetes cluster.

2. Clone this repository locally and navigate to the repository folder:

```

git clone https://github.com/shailesh-vaidya/devops-setup
cd devops-setup

```

3. Apply the Kubernetes manifests using kubectl:

```

kubectl apply -k k8s/

```

4. Wait until all pods are in the `Running` state:

```

kubectl get pods -A 

```

5. Access the deployed services:

- **Gitea:** Open [http://localhost:30080/](http://localhost:30080/) and sign in as the admin user. You should see a demo repository created with a sample script and Jenkinsfile.

- **Jenkins:** Open [http://localhost:32080/job/demo-pipeline/](http://localhost:32080/job/demo-pipeline/). Log in as the admin user, trigger the `demo-pipeline`, and it should run successfully.

