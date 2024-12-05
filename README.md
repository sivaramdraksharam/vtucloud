### **Student Activity: Introduction to Google Kubernetes Engine (GKE)**

Welcome to this hands-on activity session on **Google Kubernetes Engine (GKE)**! In this activity, you will practice setting up and managing Kubernetes clusters using GKE. Follow the steps below to gain practical experience with GKE. Each section includes examples to help reinforce your understanding.

---

### **1. Understanding GKE and Kubernetes**

#### **Example 1: Basic Concepts**

- **Kubernetes**: An open-source platform for automating the deployment, scaling, and management of containerized applications.
- **GKE**: A managed service by Google Cloud that simplifies running Kubernetes clusters.

#### **Example 2: Kubernetes Components**

- **Pods**: The smallest deployable units in Kubernetes, which can contain one or more containers.
- **Nodes**: Machines (virtual or physical) that run your applications and are managed by the Kubernetes control plane.

#### **Example 3: Kubernetes Control Plane**

- **API Server**: Exposes the Kubernetes API.
- **Scheduler**: Assigns workloads to nodes.
- **Controller Manager**: Ensures the desired state of the cluster is maintained.

---

### **2. Why Choose GKE for Orchestration?**

#### **Example 1: Managed Service Benefits**

- **Automatic Updates**: GKE keeps your clusters up-to-date with the latest Kubernetes versions.
- **Simplified Management**: Google handles infrastructure setup and maintenance.

#### **Example 2: Integration with Google Cloud Services**

- **Google Cloud Storage**: Seamlessly store and retrieve data.
- **Google Cloud Pub/Sub**: Enable messaging between microservices.

#### **Example 3: Cost Efficiency**

- **Pay-as-you-go Pricing**: Only pay for the resources you use.
- **Autoscaling**: Automatically adjust resources based on demand.

---

### **3. GCP Setup and Navigation**

#### **Example 1: Creating a GCP Account**

- Visit the [Google Cloud website](https://cloud.google.com/) and sign up for a free account.
- Utilize the $300 in credits provided by the free tier.

#### **Example 2: Navigating the GCP Console**

- Familiarize yourself with the navigation menu on the left-hand side.
- Locate the **Kubernetes Engine** section to manage your clusters.

#### **Example 3: Enabling APIs**

- Enable necessary APIs like the **Kubernetes Engine API** to start using GKE.

---

### **4. Creating a Kubernetes Cluster on GKE**

#### **Example 1: Enabling the Kubernetes Engine API**

- Navigate to the **Kubernetes Engine** section and click on **Enable API**.

#### **Example 2: Creating a Cluster**

- Choose a cluster name and region.
- Select the number of nodes for your cluster.

#### **Example 3: Configuring Node Pools**

- Create node pools with different configurations for varied workloads.

---

### **5. Connecting to Your Cluster Using kubectl**

#### **Example 1: Installing kubectl**

- Follow the [Kubernetes documentation](https://kubernetes.io/docs/tasks/tools/install-kubectl/) to install kubectl.

#### **Example 2: Connecting to Your Cluster**

- Use the command:
  ```bash
  gcloud container clusters get-credentials [CLUSTER_NAME] --zone [ZONE]
  ```

#### **Example 3: Verifying Connection**

- Run `kubectl get nodes` to ensure you are connected to your cluster.

---

### **6. Deploying a Simple Web Application on GKE**

#### **Example 1: Creating a Deployment**

- Write a manifest file for your application, e.g., using an Nginx image.

#### **Example 2: Applying the Manifest**

- Deploy the application with:
  ```bash
  kubectl apply -f deployment.yaml
  ```

#### **Example 3: Verifying Deployment**

- Check the status of your deployment with `kubectl get deployments`.

---

### **7. Exposing the Application with a LoadBalancer**

#### **Example 1: Creating a Service**

- Write a manifest file for a LoadBalancer Service.

#### **Example 2: Applying the Service Manifest**

- Create the Service with:
  ```bash
  kubectl apply -f service.yaml
  ```

#### **Example 3: Accessing the Application**

- Retrieve the external IP address of the LoadBalancer and access your application.

---

### **8. Monitoring and Logging with Google Cloud's Built-in Tools**

#### **Example 1: Setting Up Monitoring**

- Use Google Cloud Monitoring to track application performance.

#### **Example 2: Configuring Alerts**

- Set up alerts for critical metrics like CPU and memory usage.

#### **Example 3: Analyzing Logs**

- Use Google Cloud Logging to view and analyze logs from your applications.

---

By completing these activities, you should have a practical understanding of how to use GKE to manage Kubernetes clusters on Google Cloud. If you have any questions or need further clarification, feel free to ask!
