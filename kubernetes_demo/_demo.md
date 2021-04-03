## Create Pod
`kubectl run nginx --image=nginx`

## Create Pod using YAML
### Write YAML to pod.yaml
``` yaml
apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: null
  labels:
    run: nginx
  name: nginx
spec:
  containers:
  - image: nginx
    name: nginx
  restartPolicy: Never
```
###  Step 2 : Deploy YAML
`kubectl create -f pod.yaml`

## Generate Yaml
`kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml > generated_pod.yaml`
