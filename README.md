# DevOps Tools Deployment on Kubernetes

Welcome to the **DevOps Tools Deployment** project! This repository offers automated, ready-to-use Kubernetes manifests and example CI/CD pipelines for essential DevOps tools. Get your DevOps environment up and running in minutes without the headache of manual setup.

***

## 🚀 Included Tools

- **Jenkins** — The industry-leading open-source automation server to build, test, and deploy your applications efficiently.
- **Gitea** — A lightweight, self-hosted Git service that makes managing your source code easy and scalable.

***

## 🔧 Quick Deployment Guide

1. **Prepare your Kubernetes cluster**
Ensure you have a Kubernetes cluster ready to deploy these tools.
2. **Clone this repository locally:**

```bash
git clone https://github.com/shailesh-vaidya/devops-setup
cd devops-setup
```

3. **Customize your setup**
Edit `k8s/kustomization.yaml` to:
    - Update `hostPathPath` values for persistent data storage on your machine.
    - Set secure admin passwords for `gitea-admin-config` and `jenkins-admin-config`.
4. **Deploy all manifests:**

```bash
kubectl apply -k k8s/
```

5. **Verify pods are running:**

```bash
kubectl get pods -A
```

6. **Access the services:**
    - **Gitea:** Visit [http://localhost:30080/](http://localhost:30080/). Log in as admin to start managing your repositories. A demo repo with sample scripts and Jenkinsfile is ready.
    - **Jenkins:** Head to [http://localhost:32080/job/demo-pipeline/](http://localhost:32080/job/demo-pipeline/). Log in with admin and trigger the demo pipeline to see it in action.

***

## 🎯 Project Goals

- Simplify the DevOps toolchain setup on Kubernetes.
- Provide fully automated deployment manifests and example pipelines.
- Enable fast onboarding for developers and DevOps teams.
- Ensure persistence and configuration flexibility with minimal manual edits.

***

## 🌟 Features

- Production-ready YAML manifests using Kustomize.
- Secure, customizable admin passwords.
- Preloaded demo repositories and pipelines for quick demos.
- Lightweight, scalable, self-hosted Git and CI/CD services.

***

## 🤝 Contributing

Contributions are welcome! Whether it’s bug fixes, new features, improved docs, or examples:

1. Fork the repository.
2. Create your feature branch.
3. Submit a pull request describing your changes.

Let’s make DevOps easier together!

***

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

***

## 🙋 Support \& Help

For issues or questions, please open an issue on the GitHub repository.

***

Enjoy a seamless DevOps experience on Kubernetes — fast, flexible, and fully automated!