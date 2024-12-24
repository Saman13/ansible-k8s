# Ansible K8s
This playbook automates the installation and configuration of a Kubernetes cluster. The default configuration implements a cluster consisting of 4 nodes:
- admin node
- master node
- two worker nodes

![kubernetes_scheme](https://github.com/user-attachments/assets/6e639fb2-e621-4118-a4ae-dfb4f2c95fd8)

## Administration node
In this example, the administration node will be used as a control point for the Kubernetes cluster. 
This node will also be used to create certificates for cluster nodes and components.


## Master node
### API Server
The API server is the central component of the cluster that exposes the Kubernetes API.
End users and other cluster components interact with the cluster through the API server.
Communication between the API server and other components in the cluster occurs over TLS to prevent unauthorized access to the cluster.
### etcd 
etcd is a secure storage that stores all configuration and state data for a cluster. 
This distributed key/value store ensures data consistency across the cluster, helping with recovery and managing its state.
### Kube-Proxy
Kube-proxy manages network communication within the cluster, directing calls to the right recipient. 
It ensures the transfer of information between services and pods, which is critical for the efficient communication of applications running in Kubernetes.
### Controller-Manager
The Controller Manager is responsible for ensuring that the current state of the cluster matches the desired state specified by the user. 
It manages various controllers such as the Node Controller, Replication Controller, and Endpoints Controller, each of which is responsible for different aspects of cluster management. These controllers monitor changes and act to correct any deviations from the desired state.
### Scheduler
The scheduler is responsible for assigning work or modules to different nodes.
It analyzes the current cluster load and places modules on nodes that have the required resources and are best suited in terms of efficiency and workload balance.


## Worker node
