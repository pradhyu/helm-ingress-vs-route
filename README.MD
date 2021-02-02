# install doku wiki to test 
helm repo add bitnami https://charts.bitnami.com/bitnami
helm uninstall dokuwiki
helm install dokuwiki bitnami/dokuwiki \
    --set podSecurityContext.fsGroup=1000580000 \
    --set containerSecurityContext.runAsUser=1000580000 \
    --set ingress.enabled=true \
    --set ingress.hostname="127.0.0.1.xip.io" \
    --set service.type=""

