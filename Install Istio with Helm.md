helm repo add istio https://istio-release.storage.googleapis.com/charts 

helm repo update 

kubectl get ns 

helm install istio-base istio/base -n istio-system --create-namespace –set defaultRevision=default 

 

helm install istiod istio/istiod -n istio-system --wait 

helm ls -n istio-system 

kubectl get deployments -n istio-system -o wide 



-----------------------------------------------------


