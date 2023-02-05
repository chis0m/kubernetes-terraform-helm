kubectl create namespace dev
kubectl create namespace prod
helm install myweb-dev webapp1/ --values webapp1/values.yaml -f webapp1/values-dev.yaml -n dev
helm install myweb-prod webapp1/ --values webapp1/values.yaml -f webapp1/values-prod.yaml -n prod
helm ls --all-namespaces