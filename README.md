#deployment repository

store the kubernetes admin.conf in deploymentagent/admin.conf
the host directory contains the hosts and the variables in all

deploy the agent to the cluster:
export KUBECONFIG=/Users/wewer/.kube/master/etc/kubernetes/admin.conf

kubectl create -f deploymentagent/deployment.yaml
kubectl delete -f deploymentagent/deployment.yaml