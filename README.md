Last login: Wed Jul 10 11:53:40 on ttys004
abdulmalik@192 ArgoCD_proj % cd
abdulmalik@192 ~ % 
abdulmalik@192 ~ % cd Documents 
abdulmalik@192 Documents % 
abdulmalik@192 Documents % 
abdulmalik@192 Documents % cd argocd
abdulmalik@192 argocd % 
abdulmalik@192 argocd % 
abdulmalik@192 argocd % ls
ArgoCD_proj		argocd-app-config
abdulmalik@192 argocd % 
abdulmalik@192 argocd % 
abdulmalik@192 argocd % 
abdulmalik@192 argocd % cd ArgoCD_proj 
abdulmalik@192 ArgoCD_proj % 
abdulmalik@192 ArgoCD_proj % 
abdulmalik@192 ArgoCD_proj % 
abdulmalik@192 ArgoCD_proj % ls
ArgoCD_proj		README.md		application.yaml	dev
abdulmalik@192 ArgoCD_proj % 
abdulmalik@192 ArgoCD_proj % 
abdulmalik@192 ArgoCD_proj % 
abdulmalik@192 ArgoCD_proj % vi README.md 

















#### Commands

```bash
# install ArgoCD in k8s
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# access ArgoCD UI
kubectl get svc -n argocd
kubectl port-forward svc/argocd-server 8080:443 -n argocd

# login with admin user and below token (as in documentation):
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo

# you can change and delete init password

```
</br>

#### Links

* Config repo: [https://gitlab.com/nanuchi/argocd-app-config](https://gitlab.com/nanuchi/argocd-app-config)

* Docker repo: [https://hub.docker.com/repository/docker/nanajanashia/argocd-app](https://hub.docker.com/repository/docker/nanajanashia/argocd-app)

* Install ArgoCD: [https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)

* Login to ArgoCD: [https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli](https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli)

* ArgoCD Configuration: [https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/](https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/)
~                                                                                                                                              
~                                                                                                                                              
~                                                                                                                                              
~                                                                                                                                              
~                                                                                                                                              
~                                                                                                                                              
"README.md" 30L, 1330B

