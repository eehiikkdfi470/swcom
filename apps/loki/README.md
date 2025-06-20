# Loki overlays structure
Installing Loki - 
#recomended to switch to root directory as per the settigns used in application.yaml file in argocd .
**kustomize build --enable-helm apps/argocd/overlays/dev | kubectl apply -f -**

For future refrence - Kind: Applicationset file will be created .
