# [Kubernetes for Developers: Core Concepts](https://app.pluralsight.com/library/courses/bea52e4a-38de-4ba1-8aa4-7787e2edb9a6/table-of-contents)

## About

Content from Pluralsigh's course "Kubernetes for Developers: Core Concepts" and [Kubernetes's GitHub](https://github.com/kubernetes/examples)

### Types of Probe

Readiness Probe: When should a container start receiving traffic?

Liveness Probe: When should a container restart?

### Deployment Options (zero downtime deployments)

1. Rolling updates: Create one and then remove one till the end
2. Blue-green deployments
3. Canary deployments
4. Rollbacks

### Services Types

1. ClusterIP: Expose the service on a cluster-internal IP (default)
2. NodePort: Expose the service on each Node's IP at a static port
3. LoadBalancer: Provisioin an external IP to act as load balancer for the service
4. ExternalName: Maps a service to a DNS name

## Commands (kubectl)

    kubectl get all # Lists Pods and Deployments

    kubectl get pods

    kubectl run [pod-name] --image=[image-name]

    kubectl get pod [pod-name]

    kubectl port-forward [pod-name | deployment-name | service-name] [external-port]:[internal-port]

    kubectl delete pod [pod-name]  #recreates the Pod

    kubectl create -f [yml-file]

    kubectl create -f [yml-file] --dry-run --validate=true # Perform a "trial" create and also validate the YAML

    kubectl apply -f [yml-file] # create or update the resource in YAML

    kubectl delete -f [yml-file]

    kubectl describe [pod | deployment] [pod-name | deployment-name]

    kubectl exec [pod-name] -it sh # Enter into the Pod's container

    kubectl get deployments

    kubectl get deployment --show-labels

    kubectl get deployment -l app=nginx

    kubectl delete deployment [deployment-name]

    kubectl delete deployment -f [yml-file]

    kubectl scale -f [yml-file] --replicas=5

    kubectl get services

    kubectl create cm app-settings --from-env-file=settings.config

    kb get cm [configurationMap-name] -o yaml

### Examples (alias 'kb')

    kb run firstpod --image=nginx:alpine

    kb get pod firstpod-6f6b4567c4-4tk8d

    kb port-forward firstpod-6f6b4567c4-4tk8d 8080:80

    kb delete pod firstpod-6f6b4567c4-4tk8d

    kb delete deployment firstpod

    kb create -f nginx.pod.yml --save-config

    kb get pod my-nginx -o yaml

    kb describe pod my-nginx

    kb exec my-nginx -it sh

    kb create -f nginx.deployment.yml --save-config

    kb get deployments -l app=my-nginx

    kb get deployments --show-labels

    kb scale -f nginx.deployment.yml --replicas=4

    kb get services

    kb create cm app-settings --from-env-file=settings.config

    kb get cm app-settings -o yaml

## Another Commands (linux)

    # Install and use curl (Alpine Linux)
    apk add curl




