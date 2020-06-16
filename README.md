# How To Develop Applications on Kubernetes with Okteto

https://www.digitalocean.com/community/tutorials/how-to-develop-applications-on-kubernetes-with-okteto

## Setup

    # Setup kubectl/doctl
    # https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-macos
    brew install kubectl
    brew install doctl

    # Create cluster https://cloud.digitalocean.com/kubernetes/
    doctl kubernetes cluster kubeconfig save hello-world
    # => Adding cluster credentials to kubeconfig file found in "/Users/nicholas/.kube/config"
    # => Setting current-context to do-nyc1-hello-world
    # Or download the file and copy it the root of this application
    kubectl --kubeconfig="kubeconfig.yaml" get nodes


     kubectl apply -f k8s
     kubectl get service hello-world

     # Visit http://{external IP address}

     brew install okteto
     okteto up # or KUBECONFIG=./kubeconfig.yaml okteto up
     go run main.go
     # Don't forget to shut it down
     okteto down

## Running a cluster locally

    # https://kubernetes.io/docs/tasks/tools/install-minikube/
    brew install minikube
    minikube start --driver=hyperkit

## Important Links

* https://www.digitalocean.com/docs/kubernetes/quickstart/
* https://www.digitalocean.com/docs/kubernetes/how-to/connect-to-cluster/