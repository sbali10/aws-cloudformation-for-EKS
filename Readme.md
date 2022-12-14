###EKS Cluster with Cloudformation ###

eksctl create cluster -f spot_cluster.yml
eksctl get cluster
aws eks update-kubeconfig --name eks-cluster
kubectl cluster-info
kubectl create namespace eksns
kubectl config set-context --current --namespace=eksns
kubectl config view



###Application Deployment with Kustomize###

kubectl apply -k .   #deploy your application with kustomize




#aws eks update-kubeconfig --name eks-cluster   ---->>>> to switch between clusters

#To solve pv volume attach EBS to your cluster view below link
https://stackoverflow.com/questions/73871493/error-while-installing-mongodb-in-aws-eks-cluster-running-prebind-plugin-volu#:~:text=Working%20commands/steps
