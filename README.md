# k8s-commands

A cheatsheet of kubernetes commands

## GENERAL COMMANDS

`kubectl get all -A | grep -i <something>`


## PODS

`kubectl get pods -n <namespace>`

`kubectl get pods -o wide`

`kubectl describe pod`

`kubectl get pod -o yaml --dry-run=client > <target-file.yaml>`

`kubectl run <pod-name> --image=<image-name> -l=<label-1>=<val1>,<label-2>=<val2>`


## DEPLOYMENTS

`kubectl get deploy`

`kubectl create deploy <deployment-name> --image=<image-name> --replicas=<replica-count> --dry-run=client -o yaml > <target-file.yaml>`


## NAMESPACES

`kubectl get ns`
