## What is this?

A simple Dockerfile with a few debug tools installed based off of alpine

The tools installed:
 - bash
 - netcat
 - netstat
 - tcpdump
 - curl
 - telnet
 - git
 - vim
 - golang

## What is the use?

I use this to quickly debug a Kubernetes cluster for network connectivity

For example, you want to verify connectivity from one Kubernetes cluster to an external service

Just run
```
kubectl apply -f https://raw.githubusercontent.com/MansoorMajeed/k8s-debug/master/kubernetes/deployment.yml
kubectl exec -it k8s-debug-deployment-<pod id> bash
```

## Cleanup
After use, delete the deployment
```
kubectl delete deployment k8s-debug-deployment
```
