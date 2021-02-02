# install doku wiki to test 
helm repo add bitnami https://charts.bitnami.com/bitnami
helm uninstall dokuwiki
helm install dokuwiki bitnami/dokuwiki \
    --set podSecurityContext.fsGroup=1000580000 \
    --set containerSecurityContext.runAsUser=1000580000 \
    --set ingress.enabled=true \
    --set ingress.hostname="127.0.0.1.xip.io" \
    --set service.type=""

# url for the openshift ingeress and routes 
https://docs.openshift.com/container-platform/4.6/networking/routes/route-configuration.html#nw-ingress-creating-a-route-via-an-ingress_route-configuration


https://medium.com/@myte/kubernetes-nfs-and-dynamic-nfs-provisioning-97e2afb8b4a9

# odo 
curl -L https://mirror.openshift.com/pub/openshift-v4/clients/odo/latest/odo-darwin-amd64 -o /usr/local/bin/odo
chmod +x /usr/local/bin/odo

