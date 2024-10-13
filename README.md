# Ansible K8s
This playbook automates the installation and configuration of a Kubernetes cluster. The default configuration implements a cluster consisting of 4 nodes:
- admin node
- master node
- two worker nodes

![kubernetes_scheme](https://github.com/user-attachments/assets/6e639fb2-e621-4118-a4ae-dfb4f2c95fd8)

## Administration node
In this example, the administration node will be used as a control point for the Cybernet cluster. 
This node will also be used to create certificates for cluster nodes and components.

## Master node

### etcd 
etcd is a secure storage that stores all configuration and state data for a cluster. 
This distributed key/value store ensures data consistency across the cluster, helping with recovery and managing its state.

## Worker node




