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

# Print POD env Variables

 kubectl exec -it firstpod -- printenv


# Service DNS

# Step 1: Verify the Service and Namespace

Ensure the nginx-service exists in the my-namespace namespace:

kubectl get services -n my-namespace

If the service is not listed, create it or check the configuration. Here's an example of how to create a simple nginx service:


apiVersion: v1
kind: Service
metadata:
  name: nginx-service
  namespace: my-namespace
spec:
  selector:
    app: nginx
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80

Apply the service definition:


kubectl apply -f nginx-service.yaml

# Step 2: Verify the DNS Configuration

Ensure the DNS pod (typically coredns) is running in the kube-system namespace:


kubectl get pods -n kube-system -l k8s-app=kube-dns

If the DNS pods are not running, troubleshoot them by describing the pods:

kubectl describe pod <dns-pod-name> -n kube-system

# Step 3: Test DNS Resolution Within the Cluster

Run a temporary pod to test DNS resolution:

kubectl run -i --tty dnsutils --image=infoblox/dnstools --restart=Never --rm

Inside the pod, test DNS resolution:

nslookup nginx-service.my-namespace.svc.cluster.local

# Google Drive Link for Content
https://drive.google.com/drive/folders/1R-U_GaHbdVvG_ammfixX4AkDZxAfilJJ?usp=sharing
