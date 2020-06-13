# How To Develop Applications on Kubernetes with Okteto

https://www.digitalocean.com/community/tutorials/how-to-develop-applications-on-kubernetes-with-okteto

## Setup

    # Setup kubectl/doctl
    # https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-macos
    brew install kubectl
    brew install doctl

    # Create cluster https://cloud.digitalocean.com/kubernetes/
    doctl kubernetes cluster kubeconfig save hello-world

     kubectl apply -f k8s
     kubectl get service hello-world
     # => Adding cluster credentials to kubeconfig file found in "/Users/nicholas/.kube/config"
     # => Setting current-context to do-nyc1-hello-world

     # Visit http://{external IP address}

     brew install okteto
     okteto up

## Important Links

* https://www.digitalocean.com/docs/kubernetes/quickstart/
* https://www.digitalocean.com/docs/kubernetes/how-to/connect-to-cluster/