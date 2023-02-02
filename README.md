# airflow2.5

### Kubenetes namespaces:

Namespaces provides a mechanism to isolate and use groups of resources in a shared cluster. Within a namespace: name resources have to be unique and namespace-scoping is applicable for namespace objects like deployments, services, etc. but not for clusterwide objects suck as Nodes, PersistentVolumes, etc.

Kubernetes starts with 4 namespaces: default, kube-node-lease, kube-public and kube-system.

#### Viewing namespaces:

       `kubectl get namespaces`
    or for a specific namespace:
       `kubectl get namespaces <name>`
    For more detailed information:
       `kubectl describe namespaces <name>`

#### Creating namespaces

1. Create a `my-namespace.yaml` with contents:

        `apiVersion: v1
        kind: Namespace
        metadata:
        name: <insert-namespace-name-here>`
    
Then run: 

        `kubectl create -f ./my-namespace.yaml`

2. Alternatively, use the below command:

        `kubectl create namespace <insert-namespace-name-here>`
        
