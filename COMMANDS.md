minikube start

ansible-playbook up.yaml

kubectl get pods

kubectl get svc -n default

kubectl port-forward -n jenkins svc/jenkins 8080:8080

kubectl port-forward -n jenkins svc/ngrok 4040:4040

kubectl exec --namespace jenkins -it $(kubectl get pods --namespace jenkins -l "app=jenkins" -o jsonpath="{.items[0].metadata.name}") -- cat /var/jenkins_home/secrets/initialAdminPassword