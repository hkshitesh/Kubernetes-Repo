# Kubernetes-Repo

# Connecting Cluster Nodes

aws eks --region ap-south-1 describe-cluster --name ClusterTwo --query cluster.status

# command 2
aws eks --region ap-south-1 update-kubeconfig --name ClusterTwo


#Docker Image Pull

docker run -p 8004:80 -d hkshitesh/kubedemo:1.0


# Access Key

AKIAXJSAYWW2BJ2BEZ7C

# Secret Access key

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

# Short form for K8S Objects

| Short name           | Full name                    |
| -------------------- | ---------------------------- |
|  csr                 |  certificatesigningrequests  |
|  cs                  |  componentstatuses           |
|  cm                  |  configmaps                  |
|  ds                  |  daemonsets                  |
|  deploy              |  deployments                 |
|  ep                  |  endpoints                   |
|  ev                  |  events                      |
|  hpa                 |  horizontalpodautoscalers    |
|  ing                 |  ingresses                   |
|  limits              |  limitranges                 |
|  ns                  |  namespaces                  |
|  no                  |  nodes                       |
|  pvc                 |  persistentvolumeclaims      |
|  pv                  |  persistentvolumes           |
|  po                  |  pods                        |
|  pdb                 |  poddisruptionbudgets        |
|  psp                 |  podsecuritypolicies         |
|  rs                  |  replicasets                 |
|  rc                  |  replicationcontrollers      |
|  quota               |  resourcequotas              |
|  sa                  |  serviceaccounts             |
|  svc                 |  services                    |
