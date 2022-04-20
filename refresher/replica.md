# [Controllers](https://kubernetes.io/docs/concepts/architecture/controller/)

Controllers are like the brains in Kubernetes. There are multiple types of controllers that run inside the kube-controller-manager. One of those import controllers is the Replication Controller.


## Replication Controller

A ReplicationController ensures that a specified number of pod replicas are running at any one time (makes sure pods are up).

## Replica Set

ReplicaSet is the next generation of Replication Controller. The replication controller supports equality based selectors whereas the replica set supports equality based as well as set based selectors.

### Manifest Example