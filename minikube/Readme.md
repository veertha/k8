# ** Installation of minikube**

Installation works on instance with MIN CPU utilisation 2 Core.

## _1. Install docker_
     sudo apt update & sudo apt upgrade
     sudo apt install apt-transport-https curl -y
     sudo apt install docker.io -y
     sudo systemctl enable docker
     sudo systemctl start docker
     docker version

## _1. Install Minikube_
    curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    sudo install minikube-linux-amd64 /usr/local/bin/minikube
    minikube version

## _3. Install Kubectl_
    curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.29.0/2024-01-04/bin/linux/amd64/kubectl
    chmod +x ./kubectl
    mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH
    echo 'export PATH=$HOME/bin:$PATH' >> ~/.bashrc
    kubectl version --client

## _4. Start the minikube Cluster_
    minikube start — driver=docker --force

## _5. Start the minikube Cluster_
    minikube stop
