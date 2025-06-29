# 🧰 1. Cluster Info & Configuration
Description	Command
Show cluster info	kubectl cluster-info
List nodes in the cluster	kubectl get nodes
View node details	kubectl describe node <node-name>
Switch context (if multiple)	kubectl config use-context <context>
List all contexts	kubectl config get-contexts

 # 📦 2. Workloads (Pods, Deployments, ReplicaSets)
Description	Command
List all pods	kubectl get pods
List pods in a specific namespace	kubectl get pods -n <namespace>
Describe a pod	kubectl describe pod <pod-name>
Delete a pod	kubectl delete pod <pod-name>
Logs of a pod	kubectl logs <pod-name>
Logs of a pod container	kubectl logs <pod-name> -c <container-name>
List deployments	kubectl get deployments
Describe a deployment	kubectl describe deployment <name>
Create from YAML	kubectl apply -f <file.yaml>
Update a deployment image	kubectl set image deployment/<name> container=image:tag
Scale a deployment	kubectl scale deployment <name> --replicas=3
Rollback a deployment	kubectl rollout undo deployment/<name>
Check rollout status	kubectl rollout status deployment/<name>
List ReplicaSets	kubectl get rs

# 🔁 3. Services, Ingress, Networking
Description	Command
List services	kubectl get svc
Describe a service	kubectl describe svc <name>
Get external IP for LoadBalancer	kubectl get svc <name>
List Ingress resources	kubectl get ingress
Describe ingress	kubectl describe ingress <name>
Port-forward a pod	kubectl port-forward pod/<pod-name> 8080:80

# 🗂️ 4. Namespaces & Contexts
Description	Command
List namespaces	kubectl get namespaces
Use specific namespace	kubectl config set-context --current --namespace=<ns>
Run a command in a namespace	kubectl get pods -n <namespace>

# 🧱 5. Persistent Storage (PV, PVC)
Description	Command
List PVCs	kubectl get pvc
Describe a PVC	kubectl describe pvc <name>
List PVs	kubectl get pv

# 🔐 6. Secrets & ConfigMaps
Description	Command
Create a secret from literal	kubectl create secret generic my-secret --from-literal=key=value
List secrets	kubectl get secrets
Describe a secret	kubectl describe secret <name>
Create a ConfigMap	kubectl create configmap my-config --from-literal=env=dev
List ConfigMaps	kubectl get configmap
Describe a ConfigMap	kubectl describe configmap <name>

# 🧪 7. Debugging & Logs
Description	Command
Logs from a pod	kubectl logs <pod-name>
Logs from a container in a pod	kubectl logs <pod-name> -c <container-name>
Watch pod events	kubectl get pods --watch
View cluster events	kubectl get events
Exec into a running container	kubectl exec -it <pod-name> -- /bin/sh
Dry run before applying	kubectl apply -f app.yaml --dry-run=client

# 📋 8. Taints, Tolerations, and Node Affinity
Description	Command
Add taint to node	kubectl taint nodes <node> key=value:NoSchedule
Remove taint from node	kubectl taint nodes <node> key-
Label a node	kubectl label nodes <node> env=prod
View node labels	kubectl get nodes --show-labels

# 🔄 9. Helm (Bonus for AKS/DevOps)
Description	Command
Add Helm repo	helm repo add <name> <url>
Install a Helm chart	helm install <release> <chart>
Upgrade a release	helm upgrade <release> <chart>
Uninstall a release	helm uninstall <release>
List all releases	helm list
Dry run a chart	helm install <release> <chart> --dry-run

# 📁 10. YAML Management
Description	Command
Generate pod YAML	kubectl run nginx --image=nginx --dry-run=client -o yaml
Export live config	kubectl get deploy <name> -o yaml

