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

`kubectl run <pod-name> --image=<image-name> --port=<container-port>`

`kubectl run <pod-name> --image=<image-name> --port=<service-port> --expose` - Create pod and expose using service of type ClusterIP of same name with target port x


## DEPLOYMENTS

`kubectl get deploy`

`kubectl create deploy <deployment-name> --image=<image-name> --replicas=<replica-count> --dry-run=client -o yaml > <target-file.yaml>`


## JOBS

`kubectl create job <job-name> --image <image-name>`


## CRON JOBS

`kubectl create cronjob <cronjob-name> --image <image-name> --scheulde "30 21 * * *"`


## ROLLOUTS + DEPLOYMENTS

`kubectl rollout status deploy/<deploymment-name>`

`kubectl rollout history deploy/<deployment-name>`

`kubectl rollout undo deploy/<deployment-name>`

`kubectl edit deploy <deploy-name>`


## NAMESPACES

`kubectl get ns`


## SERVICES

`kubectl get svc`

`kubectl expose <resource-type> <resource-name> --port=<exposed-port> --name=<service-name>`


## CONFIG MAPS

`kubectl create cm <map-name> --from-literal=key1=value1,key2=value2...`


## SECRETS

`kubectl create secret <secret-type> <secret-name> --from-literal=<key1>=<value1> --from-literal=<key2>=<value2>...`


## NETWORK POLICIES

`kubectl get netpol`


## INGRESS

`kubectl get ingress`


## PERSISTENT VOLUME

`kubectl get pv`


## PERSISTENT VOLUME CLAIM

`kubectl get pvc`


## STORAGE CLASS

`kubectl get sc`
