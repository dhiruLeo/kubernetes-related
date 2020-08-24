# mstackxtask
1. Created a Kubernetes cluster GKE from a trial Account.

2. Create Custom Domain name for name based routing for services. 

3. Install helm on kubernetes Cluster.

4. Deploy Nginx-Ingress Controller on Kubernetes cluster
 
5. Two Yamls mstackxProd.yaml & mstackxStage.yaml will create 2 namespaces i.e. stage & prod with other resources in respective namespaces

6. Script.sh which will automate the above steps.

7. When you run kubectl run -i --tty load-generator --image=busybox /bin/sh it will give u a command prompt enter the following command

# To Apply load on prod frontend service
while true; do wget -q -O- http://frontend.prod.svc.cluster.local; done   

# To Apply load on stage frontend service

while true; do wget -q -O- http://frontend.stage.svc.cluster.local; done

In the context of above test, please explain the following:

1. What was the node size chosen for the Kubernetes nodes? And why?
I created a 3 Node GKE Cluster and node type "n1-standard" which has 6GB of RAM 

2. What method was chosen to install the demo application and ingress controller on the cluster, justify the method used?

Using Kubectl command Line from Yaml File
kubectl create -f mstackxProd.yaml

4. What would be your chosen solution to monitor the application on the cluster and why?
Prometheus & Grafana Beacause it's open-source

5. What additional components / plugins would you install on the cluster to manage it better?
RBAC to secure Kubernetes Cluster access from unauthenticated users.
