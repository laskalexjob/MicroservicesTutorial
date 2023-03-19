# MicroservicesTutorial

// Link to the Ingress Nginx controller
https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.48.1/deploy/static/provider/cloud/deploy.yaml

DOCKER

docker build -t user-management-debug -f UserManagementService_Dockerfile_Debug .
docker build -t identity-server-debug -f IdentityServer_Dockerfile_Debug .
docker build -t orders-debug -f OrdersService_Dockerfile_Debug .
docker build -t articles-debug -f ArticlesService_Dockerfile_Debug .
docker build -t api-service-debug -f ApiService_Dockerfile_Debug .
docker run -p 5001:5001 identity-server-debug
docker run -p 5002:5002 user-management-debug
docker run -p 5004:5004 orders-debug-debug
docker run -p 5006:5006 articles-debug-debug
docker run -p 5008:5008 api-service-debug-debug

https://www.youtube.com/watch?v=wi3nf99w_4g&list=WL&index=18&ab_channel=AndreyShyrokoriadov

Полезные ссылки:
Докер файл: https://docs.docker.com/engine/refere...
https://stackoverflow.com/questions/5...
https://stackoverflow.com/questions/6...
https://stackoverflow.com/questions/5...
https://jwt.io/


KUBERNETES

kubectl get ingress

kubectl logs -n nginx-ingress ingress-nginx-controller-6b94c75599-9zg9k  -> show logs for pod in namespace

kubectl config set-context --current --namespace=ingress-nginx  -> change context ('default' is default context)