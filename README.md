# java-bank
This is  a repo contains opensource java based source code for banking application

####  Note: Either use 'deploy_to_AKS' Job or ArgoCD for deployment to AKS
####  Note: Kubeconfig is used for deployment via pipeline in realrime scenarios. (deploy_to_AKS)

# Install ArgoCD Deployment: 
- kubectl create namespace argocd
- kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
- Update "argocd-server" service to LoadBalancer type to access ArgoCD UI externally.
- Collect the admin initial password using: (Username: admin)
- kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
- Access ArgoCD UI using: http://<EXTERNAL-IP> & update ur password (In org you will get an URL)
- Add your repository in "Settings" & Create your application.