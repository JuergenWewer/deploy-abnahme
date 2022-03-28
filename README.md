#deployment repository

store the kubernetes admin.conf for the cluster in deploymentagent/admin.conf:
cp /Users/wewer/.kube/master/etc/kubernetes/admin.conf /Users/wewer/workspace/deploy-abnahme/deploymentagent/admin.conf
configure deployment repository in:

deploymentagent/playbooks.yaml
deploymentagent/deployment.yaml
deploymentagent/host/group_vars/all

the host directory contains the hosts and the variables in all

deploy the agent to the cluster:
export KUBECONFIG=/Users/wewer/.kube/master/etc/kubernetes/admin.conf

kubectl create -f deploymentagent/deployment.yaml
kubectl delete -f deploymentagent/deployment.yaml