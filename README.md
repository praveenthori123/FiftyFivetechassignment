# FiftyFivetechassignment

1. first Task : Create a terraform to launch a EKS cluster. /
   
  > terraform init  /n
  > terraform plan
  > terraform apply --auto-approve
  > rm ~/.kube/config
  > aws eks --region us-east-1 update-kubeconfig --name terraform-eks-demo
  > kubectl cluster-config
  > choco install -y aws-iam-authenticator
  > aws-iam-authenticator help


2. Second Task : Deploy Jenkins server on EKS
   file used: jenkins-pv.yaml jenkins-pvc.yaml

  > kubectl create -f jenkins-pv.yaml
  > kubectl create -f jenkins-pvc.yaml
  > helm install jenkins bitnami/jenkins
  >  kubectl get secret --namespace default jenkins -o jsonpath="{.data.jenkins-password}" | base64 -d
  >  kubectl port-forward jenkins-7cb6446c76-bj4s9 9000:8080
 
 3. 
