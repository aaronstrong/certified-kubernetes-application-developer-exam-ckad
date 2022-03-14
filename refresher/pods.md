# Pods

* Smallest object you can create in Kubernetes

## kubectl
Command will deploy a docker container running nginx in a kubernetes cluster

```
kubectl run nginx --image nginx
```

* `--image nginx` tells kubectl from where to get the image like Dokcer Hub in this example



```
kubectl get pods
```
Gets a list of pods running in the cluster



## Pod with Yaml
 Kubernetes input language is `YAML` constructed in a manifest file like `pod-definition.yaml` file.

All pod yaml manifest consists for 4 main top level fields that are **REQUIRED**.

```yaml
apiVersion:
kind:
metadata:

spec:
```
| field  | Description |
| --- | --- |
| `apiVersion` | The version of the api. |
| `kind` | Type of object you're trying to create.<br>Other values include: `service`, `replicaSet`, and `Deployment` |
| `metadata` | Data about the object like name, labels. |
| `spec` | additional information pertaining to the object. |


### Full Yaml example

```yaml
# pod-definition.yaml
apiVersion: v1   # <------------------ String
kind: Pod        # <------------------ String
metadata:
  name: my-pod   # \
  labels:        #  }-- Dictionary
    app: myapp   # /

spec:
  containers:    # <------------------ List Array
    - name: nginx-container
      image: nginx
```
From the cluster, deploy the pod with the command below:
```kubectl
kubectl create -f pod-defintion.yaml
```