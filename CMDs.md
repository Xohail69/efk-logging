use this cmd to apply all the elasticsearch.yaml, fluentd.yaml, kibana.yaml files

kubectl apply -f <file_name>.yaml -n istio-system


kubectl apply -f istio-efk-gateway.yaml -n istio-system


command to forward port after all deployments:

kubectl port-forward -n istio-system kibana-59c6b7fd99-wt2hj 8080:5601
