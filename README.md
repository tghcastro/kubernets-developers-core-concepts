# [Kubernetes for Developers: Core Concepts](https://app.pluralsight.com/library/courses/bea52e4a-38de-4ba1-8aa4-7787e2edb9a6/table-of-contents)

## About

Content from Pluralsigh's course "Kubernetes for Developers: Core Concepts"

## Commands:

    kubectl get all # Lists Pods, Deployments and ReplicaSets

    kubectl get pods

    kubectl run [pode-name] --image=[image-name]

    kubectl get pod [pode-name]

    kubectl port-forward [pode-name] [external-port]:[internal-port]

    kubectl delete pod [pod-name]  #recreates the Pod

    kubectl delete deployment [deployment-name]

### Examples (alias 'kb'):

    kb run firstpod --image=nginx:alpine

    kb get pod firstpod-6f6b4567c4-4tk8d

    kb port-forward firstpod-6f6b4567c4-4tk8d 8080:80

    kb delete pod firstpod-6f6b4567c4-4tk8d

    kb delete deployment firstpod



