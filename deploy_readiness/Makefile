# var 
CMD ?= kubectl apply -f

.PHONY: ccluster namespace deploy service ingress cservice

ccluster:
	kind create cluster --config ./create_cluster.yaml
namespace:
	$(CMD) ./private.yaml
deploy:
	$(CMD) ./deploy.yaml
service:
	$(CMD) ./service.yaml
ingress:
	$(CMD) ./ingress.yaml
cservice:
	kubectl port-forward service/service-private 3011:3011

# cmd after create cluster
# kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
