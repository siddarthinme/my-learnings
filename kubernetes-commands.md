Below is a comprehensive list of **Kubernetes commands** with a brief explanation of their usage. Commands are categorized by their function for better clarity.

---

### **General Kubernetes Commands**
1. **`kubectl version`**  
   - Displays the Kubernetes client and server version.

2. **`kubectl cluster-info`**  
   - Provides information about the Kubernetes cluster, including master and service endpoints.

3. **`kubectl config view`**  
   - Shows the current Kubernetes configuration.

4. **`kubectl get nodes`**  
   - Lists all nodes in the cluster.

5. **`kubectl describe node <node-name>`**  
   - Displays detailed information about a specific node.

---

### **Namespace Management**
1. **`kubectl get namespaces`**  
   - Lists all namespaces.

2. **`kubectl create namespace <namespace-name>`**  
   - Creates a new namespace.

3. **`kubectl delete namespace <namespace-name>`**  
   - Deletes a namespace and all resources within it.

---

### **Pod Management**
1. **`kubectl get pods`**  
   - Lists all pods in the current namespace.

2. **`kubectl get pods --all-namespaces`**  
   - Lists all pods in all namespaces.

3. **`kubectl describe pod <pod-name>`**  
   - Provides detailed information about a specific pod.

4. **`kubectl logs <pod-name>`**  
   - Retrieves the logs from a specific pod.

5. **`kubectl exec -it <pod-name> -- <command>`**  
   - Executes a command inside a running pod (e.g., bash).

6. **`kubectl delete pod <pod-name>`**  
   - Deletes a specific pod.

---

### **Deployment Management**
1. **`kubectl get deployments`**  
   - Lists all deployments in the current namespace.

2. **`kubectl create deployment <deployment-name> --image=<image-name>`**  
   - Creates a deployment using the specified image.

3. **`kubectl scale deployment <deployment-name> --replicas=<number>`**  
   - Scales a deployment to the desired number of replicas.

4. **`kubectl rollout status deployment <deployment-name>`**  
   - Checks the status of a deployment rollout.

5. **`kubectl delete deployment <deployment-name>`**  
   - Deletes a specific deployment.

---

### **Service Management**
1. **`kubectl get services`**  
   - Lists all services in the current namespace.

2. **`kubectl describe service <service-name>`**  
   - Provides details about a specific service.

3. **`kubectl expose deployment <deployment-name> --type=<type> --port=<port>`**  
   - Exposes a deployment as a service (types: ClusterIP, NodePort, LoadBalancer).

4. **`kubectl delete service <service-name>`**  
   - Deletes a specific service.

---

### **ConfigMap and Secret Management**
1. **`kubectl create configmap <config-name> --from-literal=<key>=<value>`**  
   - Creates a ConfigMap from a literal value.

2. **`kubectl get configmaps`**  
   - Lists all ConfigMaps in the current namespace.

3. **`kubectl describe configmap <config-name>`**  
   - Displays details about a ConfigMap.

4. **`kubectl delete configmap <config-name>`**  
   - Deletes a specific ConfigMap.

5. **`kubectl create secret generic <secret-name> --from-literal=<key>=<value>`**  
   - Creates a generic secret.

6. **`kubectl get secrets`**  
   - Lists all secrets in the current namespace.

7. **`kubectl describe secret <secret-name>`**  
   - Provides details about a specific secret.

---

### **Persistent Volume (PV) and Persistent Volume Claim (PVC)**
1. **`kubectl get pv`**  
   - Lists all persistent volumes.

2. **`kubectl get pvc`**  
   - Lists all persistent volume claims.

3. **`kubectl describe pvc <pvc-name>`**  
   - Provides details about a specific PVC.

4. **`kubectl delete pvc <pvc-name>`**  
   - Deletes a specific PVC.

---

### **Resource Application**
1. **`kubectl apply -f <file.yaml>`**  
   - Creates or updates resources defined in a YAML file.

2. **`kubectl delete -f <file.yaml>`**  
   - Deletes resources defined in a YAML file.

3. **`kubectl edit <resource-type> <resource-name>`**  
   - Edits a resource configuration directly in the editor.

---

### **Resource Monitoring**
1. **`kubectl top nodes`**  
   - Displays CPU and memory usage of nodes.

2. **`kubectl top pods`**  
   - Shows resource usage of pods.

---

### **Role-Based Access Control (RBAC)**
1. **`kubectl get roles`**  
   - Lists all roles in the current namespace.

2. **`kubectl get rolebindings`**  
   - Lists all role bindings in the current namespace.

3. **`kubectl describe role <role-name>`**  
   - Provides details about a specific role.

4. **`kubectl describe rolebinding <rolebinding-name>`**  
   - Provides details about a specific role binding.

---

### **Debugging and Troubleshooting**
1. **`kubectl get events`**  
   - Lists all cluster events.

2. **`kubectl describe <resource-type> <resource-name>`**  
   - Displays details about a resource (useful for debugging).

3. **`kubectl logs <pod-name> -c <container-name>`**  
   - Retrieves logs for a specific container in a pod.

4. **`kubectl port-forward <pod-name> <local-port>:<pod-port>`**  
   - Forwards a local port to a pod port.

5. **`kubectl debug node/<node-name>`**  
   - Debugs a node (requires debugging tools).

---

### **Helm Commands (Optional)**
1. **`helm list`**  
   - Lists all Helm releases.

2. **`helm install <release-name> <chart-name>`**  
   - Installs a Helm chart.

3. **`helm upgrade <release-name> <chart-name>`**  
   - Upgrades an existing Helm release.

4. **`helm uninstall <release-name>`**  
   - Deletes a Helm release.

---

This covers most essential Kubernetes commands. Let me know if you'd like explanations for specific scenarios or advanced commands!
