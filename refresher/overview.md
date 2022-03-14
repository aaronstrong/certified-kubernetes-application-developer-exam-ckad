## Kubernetes Architecture

## Nodes
* Physical or virtual machine
* Worker machine that launches pods

## Cluster
* Set of nodes grouped together. If one node fails, app still lives.
* Helps sharing load

## Cluster Management (Master)
* Another node, configured as the "master"
* Watches over nodes in the cluster
* orchestrates the pods on the nodes

## Components
* API server
* etcd
* kubelet
* Container Runtime
* Controller
* Scheduler

### API Server
* Frontend for the K8.
* Users, CLI, all interact with API server

### etcd
* Distributed key value store, used to store data to manage cluster.
* Multiple master/nodes - all data is stored in etcd.
* Handles logs and no conflict between masters

### kubelet
* AGent that is ran on each node.
* Makes usre containers are running as expected

### Container Runtime
* Software used to run containers
* Like Docker

### Controller
* Brains behind orchestration.
* Nodes/containers/endpoints uptimes.
* It's responsible for bringing up new nodes/containers/pods 

### Scheduler
* Schedule pods across nodes.


## Master vs Worker Nodes
### Worker Nodes
* Has the container runtime installed
* Kubelet is also installed on a node

### Master Nodes
* Has kube-apiserver installed
* etcd is installed on a master node
* Controller and Scheduler is installed