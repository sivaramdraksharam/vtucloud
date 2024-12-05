# EKS

### **Overview of Amazon Elastic Kubernetes Service (EKS)**

**Amazon Elastic Kubernetes Service (EKS)** is a fully managed Kubernetes service provided by Amazon Web Services (AWS). It simplifies deploying, managing, and scaling containerized applications using Kubernetes, while leveraging AWS's robust cloud infrastructure and services.

---

### **Key Features of Amazon EKS**

| **Feature**                   | **Description**                                                                                   |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| **Managed Kubernetes Control Plane** | AWS manages the Kubernetes control plane, including updates, patches, and high availability.   |
| **Integration with AWS Services**   | Seamlessly integrates with AWS services like IAM, VPC, CloudWatch, ALB, and Auto Scaling.      |
| **Multi-AZ Availability**          | Distributes the control plane across multiple AWS Availability Zones (AZs) for fault tolerance. |
| **Managed Node Groups**            | Automates provisioning and lifecycle management of EC2 instances as Kubernetes nodes.          |
| **EKS Anywhere**                   | Enables Kubernetes deployment on on-premises infrastructure, with consistent management tools. |
| **EKS Fargate**                    | Runs Kubernetes pods on AWS Fargate, a serverless compute engine, eliminating the need to manage EC2 instances. |
| **Support for Hybrid and Multi-Cloud** | Works with AWS Outposts for hybrid deployments and integrates with Kubernetes on other clouds.|
| **Enhanced Security**              | Leverages AWS IAM for authentication and fine-grained permissions, with built-in support for security standards. |
| **Scalability and Performance**    | Handles workloads at any scale with AWS's elastic infrastructure and auto-scaling features.    |
| **Cost Optimization**              | Offers flexible pricing options, including on-demand, reserved, and spot instances.            |

---

### **Why Use EKS on AWS?**

EKS is a robust choice for running Kubernetes workloads on AWS due to its deep integration with AWS services, reliability, and scalability.

#### **1. Fully Managed Kubernetes Service**
- AWS manages the **Kubernetes control plane** (API server, etcd database, and other core components), removing the operational burden from users.
- Control plane updates, patches, and backups are handled automatically.

#### **2. High Availability and Fault Tolerance**
- The control plane is distributed across multiple AZs for redundancy.
- Worker nodes can also be deployed in multiple AZs to ensure application resilience.

#### **3. Seamless Integration with AWS Services**
- **IAM**: Fine-grained access control for users and applications.
- **VPC**: Network isolation for your Kubernetes resources.
- **CloudWatch**: Monitoring and logging for Kubernetes clusters.
- **Elastic Load Balancer (ALB/NLB)**: Automatically integrates with Kubernetes Ingress for scalable load balancing.
- **EBS and S3**: Persistent storage options for Kubernetes applications.

#### **4. Flexible Compute Options**
- Use **Amazon EC2** for full control over worker nodes.
- Opt for **AWS Fargate** for serverless Kubernetes, where AWS provisions and manages compute resources.

#### **5. Security and Compliance**
- Integrates with AWS Key Management Service (KMS) for encryption.
- Compliance with standards like HIPAA, PCI DSS, and ISO.
- Built-in tools like Amazon GuardDuty and AWS Security Hub enhance cluster security.

#### **6. Scalability**
- **Horizontal Pod Autoscaler (HPA)**: Automatically adjusts the number of pods based on CPU/memory usage.
- **Cluster Autoscaler**: Adds/removes EC2 instances based on workload demands.
- Supports large-scale deployments, handling thousands of nodes and pods efficiently.

#### **7. Hybrid and Multi-Cloud Deployments**
- **EKS Anywhere**: Extends Kubernetes clusters to on-premises environments.
- **AWS Outposts**: Brings AWS infrastructure and services to your data center.

#### **8. Cost Efficiency**
- Pay only for the EKS control plane and the underlying compute resources (EC2, Fargate).
- Optimize costs using spot instances for non-critical workloads.

#### **9. Open-Source Kubernetes**
- EKS uses upstream Kubernetes, ensuring compatibility with Kubernetes tools, APIs, and custom resources.

#### **10. Comprehensive Ecosystem**
- Extensive support from the AWS ecosystem, including monitoring, logging, and CI/CD tools.
- Compatible with third-party tools like Helm, Prometheus, Grafana, and more.

---

### **Common Use Cases for Amazon EKS**

| **Use Case**                     | **Description**                                                                                   | **Example**                                                                                      |
|-----------------------------------|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Microservices**                 | Orchestrates independent services for modern application architectures.                          | E-commerce apps with separate services for payments, user management, and inventory.            |
| **CI/CD Pipelines**               | Automates and accelerates application deployment workflows.                                      | Using CodePipeline and CodeBuild for Kubernetes application delivery on EKS.                    |
| **Big Data and Analytics**        | Runs distributed data processing frameworks like Apache Spark on Kubernetes.                    | Processing large datasets using Spark or Flink on EKS.                                          |
| **AI/ML Workloads**               | Supports distributed training and inference pipelines for machine learning models.               | Running TensorFlow or PyTorch jobs on GPU-enabled EKS nodes.                                    |
| **Hybrid Cloud Deployments**      | Enables consistent Kubernetes management across AWS and on-premises.                            | Running sensitive workloads on-prem while leveraging AWS for scaling public-facing APIs.         |
| **Real-Time Applications**        | Scales applications dynamically to handle traffic spikes.                                        | Video streaming platforms or gaming applications with fluctuating user demand.                  |

---

### **Comparison: EKS vs Other Kubernetes Services**

| **Feature**                  | **AWS EKS**                          | **Google GKE**                          | **Azure AKS**                          |
|-------------------------------|---------------------------------------|-----------------------------------------|-----------------------------------------|
| **Ease of Setup**             | Fully managed; moderate complexity.  | Fully managed; user-friendly.           | Fully managed; beginner-friendly.       |
| **Integration**               | Deep AWS services integration.       | Integrates with GCP ecosystem.          | Integrates with Azure ecosystem.        |
| **Hybrid/Multi-Cloud**        | EKS Anywhere, AWS Outposts.          | Anthos for hybrid/multi-cloud.          | Limited hybrid options (Azure Arc).     |
| **Scaling**                   | Supports HPA, cluster autoscaling.   | Advanced autoscaling options.           | Limited pod autoscaling support.        |
| **Cost**                      | Pay for control plane and compute.   | Similar pricing structure.              | Slightly lower cost for small workloads.|

---

### **Advantages of EKS**

| **Advantage**                          | **Explanation**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| **AWS Reliability**                    | Built on AWS's robust, globally distributed infrastructure.                                     |
| **Ease of Operations**                 | Offloads cluster management, allowing teams to focus on applications.                          |
| **Highly Scalable**                    | Efficiently handles workloads ranging from small applications to enterprise-grade deployments. |
| **Flexible Compute Options**           | Choose from EC2, spot instances, or serverless Fargate.                                        |
| **Strong Ecosystem Support**           | Integrates with AWS tools and third-party Kubernetes tools.                                    |

---

### **Challenges of EKS**

| **Challenge**                          | **Explanation**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| **Learning Curve**                     | Kubernetes concepts and AWS-specific integrations can be complex for beginners.                |
| **Cost Management**                    | Misconfigured clusters (e.g., overprovisioned nodes) can lead to high costs.                   |
| **Manual Configuration for Worker Nodes**| Requires effort to configure and manage worker nodes unless using Fargate.                     |

---

### **Conclusion**

Amazon EKS is a powerful and flexible Kubernetes solution for organizations leveraging AWS. It is ideal for running scalable, resilient, and cost-efficient containerized applications while benefiting from AWS's rich ecosystem. 

---

### **Setting Up and Configuring an EKS Cluster**

This guide will walk you through:

1. **Configuring IAM roles and permissions for Kubernetes access**.
2. **Creating an EKS cluster using AWS CLI and eksctl**.

---

### **1. Prerequisites**

#### **AWS CLI and eksctl Installation**
1. **Install AWS CLI**:  
   [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).
2. **Install eksctl**:  
   Follow the [eksctl Installation Guide](https://eksctl.io/introduction/#installation).

#### **Configure AWS CLI**
Run the following command to configure AWS CLI with your credentials:
```bash
aws configure
```
Provide:
- **Access Key ID**
- **Secret Access Key**
- **Region** (e.g., `us-west-2`)
- **Output format** (e.g., `json`)

#### **Install kubectl**
Install kubectl, the Kubernetes command-line tool:  
[Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

---

### **2. Configuring IAM Roles and Permissions**

#### **Create an IAM Role for EKS**
1. Navigate to the **IAM Console** → **Roles** → **Create Role**.
2. Select **EKS** under the trusted entity.
3. Assign the following policies:
   - **AmazonEKSClusterPolicy**
   - **AmazonEKSServicePolicy**
4. Name the role (e.g., `eksClusterRole`) and create it.

#### **Create an IAM Role for Worker Nodes**
1. Go to **IAM Console** → **Roles** → **Create Role**.
2. Select **EC2** under the trusted entity.
3. Assign the following policies:
   - **AmazonEKSWorkerNodePolicy**
   - **AmazonEC2ContainerRegistryReadOnly**
   - **AmazonEKS_CNI_Policy**
4. Name the role (e.g., `eksWorkerNodeRole`) and create it.

#### **Attach the Roles to the Cluster**
eksctl automatically attaches the necessary IAM roles to your EKS cluster and worker nodes. You can skip manual role attachment if using eksctl.

---

### **3. Create an EKS Cluster Using eksctl**

eksctl simplifies the process of creating an EKS cluster by automating resource provisioning.

#### **Basic eksctl Command to Create a Cluster**
```bash
eksctl create cluster \
  --name my-cluster \
  --region us-west-2 \
  --nodegroup-name standard-workers \
  --node-type t3.medium \
  --nodes 3 \
  --nodes-min 1 \
  --nodes-max 5 \
  --managed
```

- **`--name`**: The name of your EKS cluster.
- **`--region`**: The AWS region (e.g., `us-west-2`).
- **`--nodegroup-name`**: Name for the worker node group.
- **`--node-type`**: EC2 instance type for worker nodes (e.g., `t3.medium`).
- **`--nodes`**: Desired number of worker nodes.
- **`--nodes-min`**: Minimum number of nodes for autoscaling.
- **`--nodes-max`**: Maximum number of nodes for autoscaling.
- **`--managed`**: Creates managed node groups.

#### **Verify the Cluster**
After creation, confirm the cluster is up and running:
```bash
kubectl get nodes
```

---

### **4. Create an EKS Cluster Using AWS CLI**

#### **Step 1: Create the EKS Cluster**
```bash
aws eks create-cluster \
  --name my-cluster \
  --region us-west-2 \
  --role-arn arn:aws:iam::[AWS_ACCOUNT_ID]:role/eksClusterRole \
  --resources-vpc-config subnetIds=subnet-abc123,subnet-def456,securityGroupIds=sg-xyz789
```

- **`--role-arn`**: IAM role for the EKS cluster.
- **`--resources-vpc-config`**: Provide the IDs of subnets and security groups.

#### **Step 2: Launch Worker Nodes**
1. Create an Auto Scaling Group for worker nodes using the worker node IAM role.
2. Register the nodes with the EKS cluster:
   ```bash
   aws eks update-kubeconfig --region us-west-2 --name my-cluster
   ```

#### **Step 3: Update `kubeconfig`**
Connect `kubectl` to your EKS cluster:
```bash
aws eks update-kubeconfig --region us-west-2 --name my-cluster
```

---

### **5. Verify the Cluster**

#### **Check Cluster Status**
```bash
eksctl get cluster --name my-cluster
```

#### **Verify Worker Nodes**
```bash
kubectl get nodes
```

#### **Deploy a Test Application**
Deploy an Nginx application:
1. Create a deployment:
   ```bash
   kubectl create deployment nginx --image=nginx
   ```
2. Expose the deployment with a service:
   ```bash
   kubectl expose deployment nginx --type=LoadBalancer --port=80
   ```
3. Get the external IP of the service:
   ```bash
   kubectl get service nginx
   ```
4. Access the application in your browser using the external IP.

---

### **6. Cluster Autoscaling**

EKS supports both **Cluster Autoscaler** and **Horizontal Pod Autoscaler (HPA)**.

#### **Enable Cluster Autoscaler**
1. Install Cluster Autoscaler:
   ```bash
   kubectl apply -f https://raw.githubusercontent.com/kubernetes/autoscaler/master/cluster-autoscaler/cloudprovider/aws/examples/cluster-autoscaler-autodiscover.yaml
   ```
2. Edit the deployment to add the `--balance-similar-node-groups` flag:
   ```bash
   kubectl edit deployment cluster-autoscaler -n kube-system
   ```

#### **Enable Horizontal Pod Autoscaler**
1. Install Metrics Server:
   ```bash
   kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
   ```
2. Enable HPA for a deployment:
   ```bash
   kubectl autoscale deployment nginx --cpu-percent=50 --min=1 --max=5
   ```

---

### **7. Cleaning Up Resources**

To avoid unnecessary charges, delete the cluster and associated resources when done:
```bash
eksctl delete cluster --name my-cluster
```

---

### **Summary**

| **Task**                              | **Tool**                     | **Command/Steps**                                                                                     |
|---------------------------------------|------------------------------|-------------------------------------------------------------------------------------------------------|
| Create EKS cluster (simplified)       | eksctl                       | `eksctl create cluster --name my-cluster --region us-west-2 --managed`                                |
| Configure IAM roles                   | AWS Console or CLI           | Create IAM roles for the cluster and worker nodes.                                                   |
| Connect kubectl to EKS cluster        | AWS CLI                      | `aws eks update-kubeconfig --region us-west-2 --name my-cluster`                                     |
| Verify cluster and nodes              | kubectl                      | `kubectl get nodes`                                                                                  |
| Autoscale worker nodes                | eksctl or Cluster Autoscaler | Use `eksctl` for managed scaling or install Cluster Autoscaler for advanced scaling.                 |

---

### **Deploying a Web Application on EKS**

This guide will walk you through:

1. **Deploying a web application on EKS.**
2. **Managing services and ingress controllers.**
3. **Scaling applications with horizontal pod autoscalers (HPA).**
4. **Using CloudWatch for monitoring and logs in EKS.**
5. **Integrating AWS monitoring tools with EKS clusters.**

---

### **1. Deploying a Web Application on EKS**

#### **Step 1: Create a Deployment Manifest**
Create a `deployment.yaml` file for an Nginx application:
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.23.2
        ports:
        - containerPort: 80
```

#### **Step 2: Apply the Deployment**
Deploy the application using `kubectl`:
```bash
kubectl apply -f deployment.yaml
```

#### **Step 3: Verify the Pods**
Ensure the pods are running:
```bash
kubectl get pods
```

---

### **2. Managing Services and Ingress Controllers**

#### **Step 1: Create a Service**
Create a `service.yaml` file to expose the application:
```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-service
spec:
  type: LoadBalancer
  selector:
    app: nginx
  ports:
  - protocol: TCP
    port: 80
    targetPort: 80
```

Apply the service manifest:
```bash
kubectl apply -f service.yaml
```

#### **Step 2: Set Up an Ingress Controller**
Use an ingress controller (e.g., AWS Load Balancer Controller) to manage external access.

1. **Install the AWS Load Balancer Controller**:
   - Follow the [AWS documentation](https://docs.aws.amazon.com/eks/latest/userguide/aws-load-balancer-controller.html).

2. **Create an Ingress Resource**:
   Example `ingress.yaml`:
   ```yaml
   apiVersion: networking.k8s.io/v1
   kind: Ingress
   metadata:
     name: nginx-ingress
     annotations:
       alb.ingress.kubernetes.io/scheme: internet-facing
   spec:
     rules:
     - host: example.com
       http:
         paths:
         - path: /
           pathType: Prefix
           backend:
             service:
               name: nginx-service
               port:
                 number: 80
   ```
   Apply the manifest:
   ```bash
   kubectl apply -f ingress.yaml
   ```

3. **Update DNS**:
   Point your domain (e.g., `example.com`) to the ALB created by the ingress controller.

---

### **3. Scaling Applications with Horizontal Pod Autoscalers (HPA)**

#### **Step 1: Install Metrics Server**
Install Metrics Server to enable resource-based scaling:
```bash
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

#### **Step 2: Enable HPA**
1. Apply the following command to autoscale pods based on CPU utilization:
   ```bash
   kubectl autoscale deployment nginx-deployment \
     --cpu-percent=50 \
     --min=1 \
     --max=10
   ```

2. Verify the HPA:
   ```bash
   kubectl get hpa
   ```

---

### **4. Using CloudWatch for Monitoring and Logs in EKS**

#### **Step 1: Enable Container Insights**
1. Install the CloudWatch agent for EKS:
   ```bash
   curl https://raw.githubusercontent.com/aws/amazon-cloudwatch-container-insights/master/k8s-deployment-manifest-templates/deployment-mode/daemonset/container-insights-monitoring/aws-cloudwatch-metrics.yaml | kubectl apply -f -
   ```

2. Confirm the agent is running:
   ```bash
   kubectl get pods -n amazon-cloudwatch
   ```

#### **Step 2: View Metrics in CloudWatch**
1. Go to the **CloudWatch Console**.
2. Navigate to **Metrics** → **Container Insights**.
3. View metrics such as CPU usage, memory usage, and network activity for your cluster.

#### **Step 3: Enable Logging**
1. Configure your cluster to send logs to CloudWatch:
   ```bash
   aws eks update-cluster-config \
     --region [REGION] \
     --name [CLUSTER_NAME] \
     --logging '{"clusterLogging":[{"types":["api", "audit", "authenticator"],"enabled":true}]}'
   ```

2. Access logs in the **CloudWatch Console** under **Logs Insights**.

---

### **5. Integrating AWS Monitoring Tools with EKS**

#### **Step 1: Use Amazon CloudWatch Container Insights**
1. **Metrics and Dashboards**:
   - CloudWatch automatically creates dashboards for EKS clusters.
   - Use these dashboards to monitor node utilization, pod health, and cluster performance.

2. **Alerts**:
   - Set up alarms based on metrics (e.g., CPU usage > 80%) using CloudWatch Alarms.

#### **Step 2: Enable Prometheus and Grafana (Optional)**
1. Deploy Prometheus and Grafana for custom monitoring:
   ```bash
   kubectl apply -f https://github.com/prometheus-operator/prometheus-operator/blob/main/bundle.yaml
   ```
2. Expose Grafana as a service to visualize metrics.

#### **Step 3: Use AWS OpenTelemetry**
1. Install the AWS Distro for OpenTelemetry:
   ```bash
   kubectl apply -f https://aws-otel.github.io/docs/setup/install-all-in-one.yaml
   ```
2. Export application metrics and traces to AWS CloudWatch or X-Ray.

---

### **Example Workflow Summary**

| **Task**                               | **Command/Manifest**                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------|
| Deploy application                     | `kubectl apply -f deployment.yaml`                                                                        |
| Expose application via LoadBalancer    | `kubectl apply -f service.yaml`                                                                           |
| Enable ingress controller              | Install AWS Load Balancer Controller and apply `ingress.yaml`.                                            |
| Scale pods dynamically                 | `kubectl autoscale deployment nginx-deployment --cpu-percent=50 --min=1 --max=10`                         |
| Enable CloudWatch monitoring/logging   | Install CloudWatch agent using provided YAML and update cluster logging configuration.                    |
| Visualize metrics in CloudWatch        | Use Container Insights dashboards in the CloudWatch Console.                                              |
| Set up alarms                          | Create alarms in CloudWatch for metrics like CPU usage, memory, or disk space.                            |

---

