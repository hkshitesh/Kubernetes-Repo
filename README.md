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
