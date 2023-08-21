## Ansible and Minikube configuration for provisioning a Minikube cluster, and starting an nginx image in the Cluster.

# Ansible Documentation
    - [Ansible Kubernetes documentation](https://docs.ansible.com/ansible/latest/collections/kubernetes/core/k8s_module.html#ansible-collections-kubernetes-core-k8s-module)
    - Install kubectl locally
    - Install python locally
    - Install pyYAML locally
    - Install jsonpatch locally

## Prerequisites

Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html)

Install [Docker Desktop](https://docs.docker.com/desktop/)

Start Docker Desktop, [enable Kubernetes on Docker Desktop](https://docs.docker.com/desktop/kubernetes/),
a kubeconfig file is created in your home directory.

Install [Minikube](https://minikube.sigs.k8s.io/docs/start/)

Start Minikube
```
minikube start --driver=docker
```

## Clone the project
```
git clone https://github.com/TomiwaAribisala-git/ansible-k8s-config.git
```

## Go to project directory
```
cd ansible-k8s-config
```

## Execute ansible playbook
```
ansible-playbook deploy-to-k8s.yml
```

## Kubectl commands
```
kubectl get ns
```

```
kubectl get pod -n my-app
```

```
kubectl get svc -n my-app
```

## Access External IP on localhost browser
```
minikube service nginx
```