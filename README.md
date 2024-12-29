# Kubernetes-Toturial

## **1. Introduction to Kubernetes**

### **What is Kubernetes?**
- Open-source container orchestration platform.
- Automates deployment, scaling, and management of containerized applications.

### **Key Features:**
- Scalability, fault tolerance, self-healing, and rollouts.

### **Core Components:**
- **Cluster**: A set of nodes managed by Kubernetes.
- **Nodes**: Worker machines running containerized apps.
- **Pods**: Smallest deployable units in Kubernetes.

---

## **2. Kubernetes Architecture**

### **Master Node Components:**
- **API Server**: Interface for Kubernetes.
- **Controller Manager**: Handles node lifecycle, replication, and endpoints.
- **Scheduler**: Assigns Pods to nodes based on resources and policies.
- **etcd**: Key-value store for cluster data.

### **Worker Node Components:**
- **Kubelet**: Ensures containers are running in Pods.
- **Kube-proxy**: Manages networking and load balancing.
- **Container Runtime**: (e.g., Docker, containerd).

---

## **3. Key Kubernetes Objects**

- **Pod**: Smallest, simplest Kubernetes object; encapsulates containers.
- **Service**: Exposes Pods for networking (ClusterIP, NodePort, LoadBalancer).
- **Deployment**: Manages stateless applications.
- **StatefulSet**: For stateful applications requiring persistent storage.
- **ConfigMap** and **Secret**: Manage configuration and sensitive data.
- **Namespace**: Virtual clusters for resource segregation.

---

## **4. Installation**

### **Prerequisites:**
- Docker or compatible container runtime.
- `kubectl` CLI tool.
- Minikube or a managed Kubernetes service.

### **Minikube Setup:**
1. Install Minikube and `kubectl`.
2. Start Minikube: `minikube start`.
3. Verify installation: `kubectl get nodes`.

---

## **5. Basic Commands**

### **Cluster Management:**
- `kubectl cluster-info` - View cluster details.
- `kubectl get nodes` - List nodes.

### **Pod Management:**
- `kubectl get pods` - List Pods.
- `kubectl describe pod <pod-name>` - View Pod details.
- `kubectl logs <pod-name>` - Fetch logs.

### **Deployment:**
- `kubectl apply -f <file.yaml>` - Create or update resources.
- `kubectl delete -f <file.yaml>` - Delete resources.

---

## **6. YAML File Basics**

### **Structure:**
- `apiVersion`: Defines API version (e.g., `v1`, `apps/v1`).
- `kind`: Resource type (e.g., Pod, Service, Deployment).
- `metadata`: Name and labels for the object.
- `spec`: Specification of the desired state.

### **Example: Pod YAML**
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  containers:
    - name: my-container
      image: nginx
```

---

## **7. Scaling and Updates**

### **Scaling:**
- Scale Deployments: `kubectl scale deployment <name> --replicas=<count>`.

### **Rolling Updates:**
- `kubectl set image deployment/<name> <container>=<image>`.

---

## **8. Persistent Storage**

- **Volumes:** Temporary or persistent storage for Pods.
- **Persistent Volumes (PV):** Cluster-level storage abstraction.
- **Persistent Volume Claims (PVC):** Request storage from PV.

---

## **9. Networking in Kubernetes**

### **Networking Basics:**
- Every Pod gets its own IP.
- Pod-to-Pod communication via cluster network.

### **Service Types:**
- ClusterIP, NodePort, LoadBalancer, ExternalName.

---

## **10. Monitoring and Debugging**

### **Monitoring Tools:**
- Prometheus, Grafana, and Kubernetes Dashboard.

### **Debugging Pods:**
- `kubectl exec -it <pod-name> -- /bin/bash` - Access Pod shell.
- `kubectl describe pod <pod-name>` - Detailed Pod info.

---

## **11. Best Practices**

- Use namespaces for resource isolation.
- Use ConfigMaps and Secrets for configuration.
- Implement resource limits (`resources.requests` and `resources.limits`).
- Automate with CI/CD pipelines.

---

Connect for more infornation...!

 
