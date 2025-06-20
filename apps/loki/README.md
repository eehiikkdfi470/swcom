#Deploying Loki with Argo CD

This guide explains how to bootstrap **Loki** using Argo CD in a clean GitOps flow.

---
#Folder Structure

Kind:Application of argocd for Loki apllication is located at **/overlays/dev/loki-application.yaml ** 

In case of Production - refer to loki-application.yaml file in production under overlays directory .

**Create DEV Loki Application in Argo CD**

#Apply the Application manifest to register Loki in Argo CD:

**kubectl apply -f apps/loki/overlays/dev/loki-application.yaml**

Sync Loki from ArgoCD

#Verify Loki is running
kubectl get pods -n loki

        OR
        
kubectl get application -n argocd
NAME       SYNC STATUS   HEALTH STATUS
loki-dev   Synced        Healthy
