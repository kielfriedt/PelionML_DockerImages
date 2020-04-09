# PelionML_Dashboard

   install dependencies:
     $ npm install

   run the app:
     $ DEBUG=pelion-rbac:* npm start


# Build docker image 'pelion-rbac'
./build-docker.sh

# Create Kubernetes namepace 'pelion-ml' if not already created
kubectl create namespace pelion-ml

# Deploy RBAC serviceName
kubectl apply -f tools/k8s/pelion-rbac-deployment.yaml --namespace pelion-ml

# Setup Ingress resource
kubectl apply -f tools/k8s/pelion-ml-ingress.yaml --namespace pelion-ml
# PelionML_DockerImages
