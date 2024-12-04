GKE

### **Introduction to Google Cloud Platform (GCP)**

**Google Cloud Platform (GCP)** is a suite of cloud computing services offered by Google. It provides a robust and scalable infrastructure for running workloads, managing data, and building modern applications.

---

### **Key Features of GCP**

1. **Scalability**: Dynamically scales compute, storage, and networking resources to meet demand.
2. **Global Infrastructure**: Operates in multiple regions and zones for high availability.
3. **Managed Services**: Offers fully managed solutions like BigQuery, Cloud Run, and Google Kubernetes Engine (GKE).
4. **Machine Learning and AI**: Provides advanced AI/ML tools, including TensorFlow and Vertex AI.
5. **Data Solutions**: Handles data processing, storage, and analytics with tools like Cloud Storage, BigQuery, and Dataproc.
6. **Security**: Built-in security features, such as IAM, encryption, and compliance certifications.

---

### **Popular GCP Services**

| **Service Category**       | **Examples**                                       |
|-----------------------------|---------------------------------------------------|
| **Compute**                | Compute Engine, Google Kubernetes Engine (GKE), App Engine |
| **Storage**                | Cloud Storage, Persistent Disks, Filestore        |
| **Networking**             | Virtual Private Cloud (VPC), Cloud CDN, Cloud DNS |
| **Data and Analytics**     | BigQuery, Dataproc, Dataflow                      |
| **Machine Learning**       | Vertex AI, AutoML, TensorFlow                     |
| **DevOps Tools**           | Cloud Build, Artifact Registry, Cloud Functions   |

---

### **What is Google Kubernetes Engine (GKE)?**

**Google Kubernetes Engine (GKE)** is a managed Kubernetes service on GCP that simplifies container orchestration. It is built on the open-source Kubernetes platform and provides tools for deploying, managing, and scaling containerized applications.

---

### **Why Choose GKE for Orchestration?**

GKE is one of the most powerful and user-friendly platforms for Kubernetes-based orchestration. Here's why it stands out:

---

### **1. Fully Managed Kubernetes Service**

- **Simplified Setup**: GKE automates the provisioning and setup of Kubernetes clusters, reducing operational overhead.
- **Upgrades and Maintenance**: Automatically handles cluster upgrades and security patches, ensuring you're always running a secure and supported version.

---

### **2. Native Integration with GCP Ecosystem**

- **Networking**: Integrates seamlessly with Google Cloud VPC, Cloud Load Balancing, and Cloud CDN for efficient and secure networking.
- **Storage**: Offers persistent storage through Cloud Storage, Persistent Disks, and Filestore.
- **Security**: Features Google’s IAM, Cloud Armor, and Shielded Nodes for robust security.

---

### **3. Scalability**

- **Cluster Autoscaler**: Dynamically adjusts the size of the cluster by adding or removing nodes based on workload demands.
- **Horizontal Pod Autoscaler (HPA)**: Automatically scales application pods based on CPU, memory, or custom metrics.

---

### **4. High Availability**

- **Regional Clusters**: Distribute nodes across multiple zones to ensure high availability and fault tolerance.
- **Load Balancing**: Integrates with Cloud Load Balancing for distributing traffic across multiple instances.

---

### **5. Advanced Features**

| **Feature**                | **Description**                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------|
| **Node Pools**              | Allows clusters to use nodes with different configurations (e.g., machine types, GPUs).            |
| **Preemptible VMs**         | Reduces costs by using short-lived compute resources for non-critical workloads.                   |
| **Anthos Integration**      | Enables hybrid and multi-cloud Kubernetes deployments.                                             |
| **Workload Identity**       | Integrates Kubernetes service accounts with Google Cloud service accounts for secure authentication.|

---

### **6. Cost-Effectiveness**

- **Pay-As-You-Go**: Pay only for the resources you use, with options to optimize costs using preemptible VMs or autoscaling.
- **Sustained-Use Discounts**: Automatically applies discounts for long-running workloads.

---

### **7. Multi-Cloud and Hybrid Cloud Support**

- With **Anthos**, GKE extends Kubernetes capabilities across multiple clouds (e.g., AWS, Azure) and on-premises environments, offering a unified management experience.

---

### **Use Cases for GKE**

| **Use Case**                       | **Description**                                                                                   | **Example**                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Microservices**                  | Deploy and manage microservices-based applications.                                               | An e-commerce platform with services for payments, inventory, and users.                       |
| **CI/CD Pipelines**                | Automate and speed up application development and deployment.                                     | A DevOps pipeline using Jenkins integrated with GKE for testing and production environments.    |
| **AI/ML Workloads**                | Run distributed machine learning workloads on GPUs or TPUs.                                       | Training a large-scale TensorFlow model on Kubernetes using GKE.                               |
| **Hybrid Cloud Deployments**       | Run workloads seamlessly across on-premises and cloud environments.                               | A financial institution deploying workloads on both GCP and on-prem for compliance reasons.     |
| **Real-Time Applications**         | Scale applications dynamically to handle traffic spikes.                                          | A video streaming platform automatically scaling resources during peak viewing hours.           |

---

### **Comparison: GKE vs. Other Kubernetes Platforms**

| **Feature**              | **GKE**                                | **AWS EKS**                          | **Azure AKS**                          |
|---------------------------|-----------------------------------------|---------------------------------------|-----------------------------------------|
| **Setup**                | Fully managed; easy setup.              | Managed; moderate setup complexity.  | Managed; user-friendly setup.           |
| **Scaling**              | Advanced autoscaling (nodes + pods).    | Node autoscaling; limited pod scaling.| Node autoscaling; manual pod scaling.   |
| **Integration**          | Seamless GCP integration.               | AWS services integration.            | Azure ecosystem integration.            |
| **Multi-cloud Support**  | Anthos for hybrid and multi-cloud.      | Limited multi-cloud capabilities.    | Limited multi-cloud capabilities.       |
| **Cost**                 | Flexible with discounts (e.g., preemptible VMs). | Similar pricing structure.           | Slightly higher cost.                   |

---

### **Why GKE is a Popular Choice**

1. **Ease of Use**: GKE abstracts away much of the complexity of managing Kubernetes, making it beginner-friendly while still powerful for experts.
2. **Performance**: Backed by Google’s low-latency global infrastructure.
3. **Innovation**: GKE often introduces cutting-edge Kubernetes features faster than other managed platforms.
4. **Community Support**: Strong community and enterprise support through Google and CNCF.

---

### **Conclusion**

Google Kubernetes Engine (GKE) is a robust and feature-rich platform for container orchestration, offering scalability, high availability, and integration with GCP’s extensive ecosystem. It’s ideal for businesses of all sizes, from startups to enterprises, looking to leverage Kubernetes without the complexity of managing it manually.

---

### **Getting Started with Google Cloud Platform (GCP) and GKE**

This guide will walk you through:

1. **Setting up and navigating GCP**.
2. **Creating a Kubernetes cluster on Google Kubernetes Engine (GKE)**.
3. **Configuring the cluster (node pools, autoscaling, etc.)**.
4. **Connecting to your cluster using `kubectl`**.

---

### **1. GCP Setup and Navigation**

#### **Sign Up for GCP**
- Go to [Google Cloud](https://cloud.google.com/) and create an account.
- New users typically receive free credits (e.g., $300 for 90 days).

#### **Enable Kubernetes Engine API**
1. Navigate to the **Google Cloud Console**: [https://console.cloud.google.com/](https://console.cloud.google.com/).
2. Open the **Navigation Menu** (three horizontal lines in the top-left corner).
3. Go to **Kubernetes Engine** → **Clusters**.
4. If prompted, enable the **Kubernetes Engine API**.

#### **Set Up Billing**
- Ensure you’ve linked a billing account to your project. Navigate to **Billing** in the GCP Console to verify.

#### **Install Google Cloud SDK**
1. Install the [Google Cloud SDK](https://cloud.google.com/sdk/docs/install).
2. Authenticate with your Google Cloud account:
   ```bash
   gcloud auth login
   ```
3. Set the active project:
   ```bash
   gcloud config set project [PROJECT_ID]
   ```

---

### **2. Creating a Kubernetes Cluster on GKE**

#### **Via GCP Console**
1. Navigate to **Kubernetes Engine** → **Clusters**.
2. Click **Create Cluster**.
3. Choose a **Cluster Mode**:
   - **Standard**: Full control and configuration options.
   - **Autopilot**: Fully managed cluster with Google handling configuration and scaling.
4. Configure the cluster:
   - **Cluster Name**: Provide a unique name (e.g., `my-cluster`).
   - **Location Type**:
     - **Zonal**: Nodes are deployed in a single zone (e.g., `us-central1-a`).
     - **Regional**: Nodes are distributed across multiple zones for high availability (e.g., `us-central1`).

#### **Via CLI**
```bash
gcloud container clusters create my-cluster \
    --num-nodes=3 \
    --zone=us-central1-a
```
- `--num-nodes`: Number of nodes in the cluster.
- `--zone`: Specifies the zone for the cluster.

---

### **3. Configuring the Cluster**

#### **Node Pools**
A **node pool** is a group of nodes within a cluster that share the same configuration.

##### **Add a Node Pool**
1. Navigate to your cluster in the GCP Console.
2. Click on the **Nodes** tab → **Add Node Pool**.
3. Configure the node pool:
   - **Machine Type**: Choose the desired VM type (e.g., `e2-standard-4` for general-purpose workloads).
   - **Disk Size**: Specify storage (e.g., 100GB).
   - **Auto-scaling**: Enable/disable autoscaling for this node pool.
4. Save the changes.

##### **Via CLI**
```bash
gcloud container node-pools create my-node-pool \
    --cluster=my-cluster \
    --machine-type=e2-standard-4 \
    --disk-size=100 \
    --num-nodes=3 \
    --zone=us-central1-a
```

---

#### **Autoscaling**
Autoscaling ensures the cluster adjusts resources dynamically based on workload demands.

##### **Enable Cluster Autoscaler**
1. During cluster creation, enable the **Cluster Autoscaler** option.
2. Specify:
   - **Minimum Nodes**: The least number of nodes.
   - **Maximum Nodes**: The upper limit for nodes.

##### **Via CLI**
```bash
gcloud container clusters update my-cluster \
    --enable-autoscaling \
    --min-nodes=1 \
    --max-nodes=5 \
    --zone=us-central1-a
```

##### **Horizontal Pod Autoscaler (HPA)**
HPA automatically scales pods based on CPU, memory, or custom metrics.

1. Deploy an application:
   ```bash
   kubectl create deployment my-app --image=nginx
   ```
2. Enable HPA:
   ```bash
   kubectl autoscale deployment my-app --cpu-percent=50 --min=1 --max=5
   ```

---

#### **Adding Labels to Nodes**
Labels help identify and organize nodes for specific workloads.

```bash
kubectl label nodes [NODE_NAME] environment=production
```

---

### **4. Connecting to Your Cluster Using kubectl**

#### **Step 1: Install kubectl**
- Install `kubectl` if not already installed: [kubectl Installation Guide](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

#### **Step 2: Authenticate kubectl with GKE**
1. Get the credentials for your cluster:
   ```bash
   gcloud container clusters get-credentials my-cluster --zone=us-central1-a
   ```
2. Confirm connection:
   ```bash
   kubectl get nodes
   ```
   - This should list all the nodes in your cluster.

---

#### **Step 3: Managing the Cluster with kubectl**

##### **Basic Commands:**
- **Get Cluster Info**:
  ```bash
  kubectl cluster-info
  ```
- **View Nodes**:
  ```bash
  kubectl get nodes
  ```
- **View Pods**:
  ```bash
  kubectl get pods
  ```

##### **Deploy an Application:**
1. Create a deployment:
   ```bash
   kubectl create deployment nginx --image=nginx
   ```
2. Expose it as a service:
   ```bash
   kubectl expose deployment nginx --type=LoadBalancer --port=80
   ```
3. View the service:
   ```bash
   kubectl get services
   ```

##### **Scale the Deployment**:
```bash
kubectl scale deployment nginx --replicas=5
```

##### **Delete Resources**:
```bash
kubectl delete deployment nginx
kubectl delete service nginx
```

---

### **Conclusion**

By following these steps, you can set up and configure a Kubernetes cluster on GKE, customize it with node pools and autoscaling, and connect to it using `kubectl`. GKE simplifies cluster management, making it ideal for development and production environments.

---

### **Deploying a Simple Web Application on GKE Using Manifests**

In this tutorial, you'll deploy a simple Nginx web application on Google Kubernetes Engine (GKE) using YAML manifests. We'll create:

1. A **Deployment** for managing pods.
2. A **Service** to expose the application internally and externally.
3. A **LoadBalancer** to provide external access.

---

### **Step 1: Prerequisites**

1. **Set Up GKE Cluster**:
   Ensure you have a running GKE cluster. You can follow the steps from [GKE Setup Guide](#).

2. **Connect to the Cluster**:
   Authenticate `kubectl` with your cluster:
   ```bash
   gcloud container clusters get-credentials [CLUSTER_NAME] --zone [ZONE]
   ```

3. **Verify Connection**:
   Confirm you're connected to the cluster:
   ```bash
   kubectl get nodes
   ```

---

### **Step 2: Create a Deployment Manifest**

A Deployment ensures that the desired number of pod replicas is maintained.

**Save the following YAML as `nginx-deployment.yaml`:**

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

**Key Points:**
- **replicas**: Specifies the desired number of pod replicas.
- **image**: Specifies the Docker image for Nginx.
- **containerPort**: Exposes the container's port internally.

---

### **Step 3: Create a Service Manifest**

A Service provides stable networking for the pods. We'll expose this deployment to external users using a `LoadBalancer`.

**Save the following YAML as `nginx-service.yaml`:**

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-service
  labels:
    app: nginx
spec:
  type: LoadBalancer
  selector:
    app: nginx
  ports:
  - protocol: TCP
    port: 80
    targetPort: 80
```

**Key Points:**
- **type: LoadBalancer**: Exposes the service externally using a cloud provider’s load balancer.
- **port**: Exposes the service on port 80.
- **targetPort**: Directs traffic to port 80 inside the pods.

---

### **Step 4: Apply the Manifests**

Use `kubectl` to create the resources defined in the manifests.

1. Deploy the application:
   ```bash
   kubectl apply -f nginx-deployment.yaml
   ```

2. Expose the service:
   ```bash
   kubectl apply -f nginx-service.yaml
   ```

3. Verify the resources:
   - Check deployments:
     ```bash
     kubectl get deployments
     ```
   - Check pods:
     ```bash
     kubectl get pods
     ```
   - Check services:
     ```bash
     kubectl get services
     ```

---

### **Step 5: Access the Application**

1. Get the external IP of the service:
   ```bash
   kubectl get service nginx-service
   ```

2. Open the external IP in your browser:
   - You should see the Nginx default welcome page.

---

### **Step 6: Cleanup Resources**

When you're done, delete the resources to save costs and free up cluster space:

1. Delete the service:
   ```bash
   kubectl delete -f nginx-service.yaml
   ```

2. Delete the deployment:
   ```bash
   kubectl delete -f nginx-deployment.yaml
   ```

---

### **Understanding the Workflow**

1. **Deployment**:
   - Ensures that 3 Nginx pods are always running.
   - Handles updates and rollbacks automatically.

2. **Service**:
   - Provides stable access to the Nginx pods, even if they are recreated or replaced.

3. **LoadBalancer**:
   - Exposes the service to the internet using GKE’s integrated load balancer.

---

### **Conclusion**

You've successfully deployed a simple Nginx web application on GKE using YAML manifests. This method is foundational for deploying and managing applications in Kubernetes.

---

### **Monitoring and Logging in GKE with Google Cloud Tools**

Google Kubernetes Engine (GKE) integrates seamlessly with **Google Cloud Operations Suite** (formerly Stackdriver) to provide robust monitoring, logging, and debugging capabilities for Kubernetes clusters. These tools help you gain insights into your cluster's performance, troubleshoot issues, and optimize resource utilization.

---

### **1. Introduction to Google Cloud Operations Suite**

**Google Cloud Operations Suite** provides:
1. **Monitoring**: Collects and visualizes metrics from your Kubernetes cluster, including CPU, memory, disk, and custom application metrics.
2. **Logging**: Captures and stores logs from Kubernetes system components (e.g., API Server, Kubelet) and application workloads.
3. **Trace**: Tracks request traces to help debug latency issues.
4. **Profiler**: Identifies resource bottlenecks in your application.

---

### **2. Setting Up Monitoring and Logging in GKE**

GKE has native integration with Google Cloud's monitoring and logging tools, and these can be enabled during cluster creation.

#### **Option 1: Enable During Cluster Creation**
1. **Via Console**:
   - Go to **Kubernetes Engine** → **Clusters** in the Google Cloud Console.
   - During cluster creation, enable **Cloud Monitoring** and **Cloud Logging** under the "Operations" section.
2. **Via CLI**:
   Use the `gcloud` command:
   ```bash
   gcloud container clusters create [CLUSTER_NAME] \
       --zone [ZONE] \
       --enable-stackdriver-kubernetes
   ```

#### **Option 2: Enable for an Existing Cluster**
1. Navigate to your cluster in the Google Cloud Console.
2. Click **Edit** and enable **Cloud Monitoring** and **Cloud Logging**.
3. Save changes and wait for the update to apply.

---

### **3. Exploring Metrics with Cloud Monitoring**

#### **Accessing Cloud Monitoring**
1. Go to the **Monitoring** page in the Google Cloud Console:  
   [https://console.cloud.google.com/monitoring](https://console.cloud.google.com/monitoring)
2. Use the **Metrics Explorer** to visualize metrics for your cluster, such as:
   - Node CPU utilization.
   - Pod memory usage.
   - Network bandwidth.

#### **Key Dashboards for Kubernetes**
- **GKE Workloads Dashboard**: Shows pod-level metrics like CPU, memory, and restarts.
- **Node Dashboard**: Provides metrics for individual nodes in the cluster.
- **Cluster Overview**: Displays health and performance metrics for the entire cluster.

#### **Create Alerts for Metrics**
1. In the Monitoring Console, go to **Alerting** → **Create Policy**.
2. Define a condition (e.g., CPU usage > 80% for 5 minutes).
3. Add notification channels (email, SMS, etc.).
4. Save the policy.

---

### **4. Viewing Logs with Cloud Logging**

#### **Accessing Cloud Logging**
1. Go to the **Logging** page in the Google Cloud Console:  
   [https://console.cloud.google.com/logs](https://console.cloud.google.com/logs)
2. View logs for:
   - Kubernetes system components (e.g., API Server, Kubelet).
   - Application logs from your pods.

#### **Filtering Logs**
- Use the query builder to filter logs:
  ```text
  resource.type="k8s_container"
  resource.labels.cluster_name="[CLUSTER_NAME]"
  logName="projects/[PROJECT_ID]/logs/stdout"
  ```

#### **Exporting Logs**
You can export logs to:
1. **Cloud Storage**: For long-term retention.
2. **BigQuery**: For advanced analytics.
3. **Pub/Sub**: To integrate with other systems.

---

### **5. Enhancing Monitoring and Logging**

#### **Custom Metrics**
- Applications can export custom metrics to Cloud Monitoring using OpenTelemetry or Prometheus.
- Example: Export the number of user logins per minute.

#### **Custom Dashboards**
1. Navigate to **Monitoring** → **Dashboards** → **Create Dashboard**.
2. Add widgets for specific metrics or log-based charts.
3. Save and share the dashboard.

#### **Log-Based Metrics**
1. In the **Logs Explorer**, create a log-based metric (e.g., count of HTTP 500 errors).
2. Use these metrics in dashboards and alerts.

---

### **6. Example Use Cases**

#### **Monitoring Pod Resource Usage**
1. Use the **Workloads Dashboard** to identify pods with high CPU or memory usage.
2. Scale up/down pods or optimize resource requests and limits in deployment manifests.

#### **Detecting Node Failures**
1. Set up alerts for node unavailability.
2. View logs for `kubelet` or system components to identify the issue.

#### **Analyzing Application Errors**
1. Filter logs for your application:
   ```text
   logName="projects/[PROJECT_ID]/logs/stderr"
   severity="ERROR"
   ```
2. Investigate error patterns or spikes in log volume.

---

### **7. Hands-On Commands**

- **View Logs for a Specific Pod**:
  ```bash
  kubectl logs [POD_NAME]
  ```
- **Stream Logs**:
  ```bash
  kubectl logs -f [POD_NAME]
  ```
- **View All Logs in a Namespace**:
  ```bash
  kubectl logs -n [NAMESPACE]
  ```

---

### **8. Conclusion**

By leveraging Google Cloud Operations Suite, you gain powerful tools for monitoring and logging in GKE. These tools provide a comprehensive view of your cluster's performance and help you troubleshoot and optimize applications effectively.
