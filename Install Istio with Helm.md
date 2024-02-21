helm repo add istio https://istio-release.storage.googleapis.com/charts 

helm repo update 

kubectl get ns 

helm install istio-base istio/base -n istio-system --create-namespace –set defaultRevision=default 

 

helm install istiod istio/istiod -n istio-system --wait 

helm ls -n istio-system 

kubectl get deployments -n istio-system -o wide 



-----------------------------------------------------

command to forward port after all deployments:

kubectl port-forward -n istio-system kibana-59c6b7fd99-wt2hj 8080:5601
