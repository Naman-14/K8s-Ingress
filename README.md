The NGINX Ingress Controller for Kubernetes works with the NGINX webserver (as a proxy).

COMMANDS TO FOLLOW: - (WITH USING NGINX Ingress Controller)

STEP 1 - Change your Kubectl config to docker desktop.

kubectl config get-contexts
kubectl config use-context docker-desktop
STEP 2 - Applying ingress-nginx Controller to proceed.

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.0.0/deploy/static/provider/cloud/deploy.yaml
STEP 3 - Now, Run basic commands.

kubectl apply -f deployment.yaml
kubectl get deployment -n ingress-nginx
kubectl get pods --all-namespaces -l app.kubernetes.io/name=ingress-nginx
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
kubectl get ing -n ingress-nginx
STEP 4 - Lastly, Open Powershell -> Run following commands and edit your host file.

cd driver
cd etc
notepad.exe hosts
Add your xyz.com below this

![image](https://github.com/Naman-14/NamanK8s-Ingress/assets/78831583/6b1c8e58-9c90-4a3f-b8ab-e87d40352b5e)

