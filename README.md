# Kubernetes-Repo

# Connecting Cluster Nodes

aws eks --region ap-south-1 describe-cluster --name ClusterNine --query cluster.status

# command 2
aws eks --region ap-south-1 update-kubeconfig --name ClusterNine
