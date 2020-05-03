# [Kubernetes for Developers: Core Concepts](https://app.pluralsight.com/library/courses/bea52e4a-38de-4ba1-8aa4-7787e2edb9a6/table-of-contents)

## About

Content from Pluralsigh's course "Kubernetes for Developers: Core Concepts"

### Types of Probe:

Readiness Probe: When should a container start receiving traffic?

Liveness Probe: When should a container restart?

## Commands:

    kubectl get all # Lists Pods and Deployments

    kubectl get pods

    kubectl run [pod-name] --image=[image-name]

    kubectl get pod [pod-name]

    kubectl port-forward [pod-name] [external-port]:[internal-port]

    kubectl delete pod [pod-name]  #recreates the Pod

    kubectl delete deployment [deployment-name]

    kubectl create -f [yml-file]

    kubectl create -f [yml-file] --dry-run --validate=true # Perform a "trial" create and also validate the YAML

    kubectl apply -f [yml-file] # create or update the resource in YAML

    kubectl delete -f [yml-file]

    kubectl describe pod [pod-name]

    kubectl exec [pod-name] -it sh # Enter into the Pod's container

### Examples (alias 'kb'):

    kb run firstpod --image=nginx:alpine

    kb get pod firstpod-6f6b4567c4-4tk8d

    kb port-forward firstpod-6f6b4567c4-4tk8d 8080:80

    kb delete pod firstpod-6f6b4567c4-4tk8d

    kb delete deployment firstpod

    kb create -f nginx.pod.yml --save-config

    kb get pod my-nginx -o yaml

    kb describe pod my-nginx

    kb exec my-nginx -it sh