# README

---------------------
Deploying the cluster =>
---------------------
Here I have gone with deploying an EKS cluster using AWS EKS.
The utility I have used to deploy the cluster is called "eksctl" => https://eksctl.io/

Kindly find the eksctl manifest I have configured, which can be found in the directory "assignment/eksctl/eksctl.yaml"
This will deploy a managed K8ts cluster using AWS cloudFormation, where AWS manages the control plane and we can access and manage the workers instances.


-----------------------------------
Deploying the ElasticSearch cluster =>
-----------------------------------
There are 3 primary Files here =>   
  
1) assignment/k8ts/es-k8ts-manifests/rbac.yaml: 
This to ensure the there is well setup Authentication and Authorization in place while accessing the cluster resources.

2) assignment/k8ts/es-k8ts-manifests/stateful-set.yaml:
This will deploy the ElasticSearch cluster as a stateful set. Kindly look into the comments on the manifest which should explain in detail, what these configurations do.

3) assignment/k8ts/es-k8ts-manifests/nodeport-service.yaml:
Exposing the pods using service type nodeport, so that pods can be accessed from outside the EKS cluster
