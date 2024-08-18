# **Load Balancers in AWS**


# ![aws-load-balancer](../assets/aws/09-aws-load-balancer/aws-load-balancer.png)

## **What is a Load Balancer?**

In AWS, a Load Balancer is a service that automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses. Load Balancers help to ensure that no single server bears too much load, improving application availability, fault tolerance, and responsiveness.

## **Types of Load Balancers in AWS**

AWS offers three types of Load Balancers:

1. **Application Load Balancer (ALB)**  
   * Best suited for HTTP and HTTPS traffic.  
   * Operates at the application layer (Layer 7 of the OSI model).  
   * Supports advanced routing features like host-based, path-based, and content-based routing.  
2. **Network Load Balancer (NLB)**  
   * Ideal for high-performance TCP and UDP traffic.  
   * Operates at the transport layer (Layer 4).  
   * Capable of handling millions of requests per second with ultra-low latency.  
3. **Classic Load Balancer (CLB)**  
   * An older generation load balancer.  
   * Supports basic load balancing for both HTTP/HTTPS and TCP protocols.  
   * Operates at both the application and transport layers.

## **Key Features of AWS Load Balancers**

* **Health Checks**: Monitors the health of registered targets and ensures that traffic is routed only to healthy instances.  
* **SSL Termination**: Offloads SSL/TLS decryption from your instances to the load balancer.  
* **Automatic Scaling**: Works seamlessly with Auto Scaling to adjust the number of instances based on demand.  
* **Cross-Zone Load Balancing**: Distributes incoming traffic evenly across all registered instances in multiple Availability Zones.

## **Setting Up an Application Load Balancer**

### **Step 1: Create a Load Balancer**

1. **Sign in to the AWS Management Console** and go to the EC2 Dashboard.  
2. **Navigate to "Load Balancers"** under the "Load Balancing" section.  
3. **Click "Create Load Balancer"** and select "Application Load Balancer".  
4. **Configure Basic Settings**:  
   * **Name**: Enter a name for your load balancer.  
   * **Scheme**: Choose whether the load balancer will be internet-facing or internal.  
   * **Listeners**: Set up protocols and ports (typically HTTP or HTTPS).  
   * **Availability Zones**: Select the VPC and Availability Zones where your load balancer will operate.

### **Step 2: Configure Security Settings**

1. **Security Groups**: Choose an existing security group or create a new one to control access to the load balancer.  
2. **SSL Certificates** (Optional): If you're using HTTPS, select or upload an SSL certificate for encryption.

### **Step 3: Register Targets**

1. **Target Groups**: Define a target group by specifying the type (instance, IP, or Lambda function).  
2. **Register Instances**: Add the EC2 instances that will receive traffic from the load balancer.  
3. **Health Checks**: Configure health check settings to monitor the health of your targets.

### **Step 4: Review and Create**

1. **Review your configuration**: Ensure all settings are correct.  
2. **Click "Create"** to launch your load balancer.

## **Why Use a Load Balancer?**

* **Improved Availability**: Distributes traffic across multiple instances, reducing the risk of downtime.  
* **Enhanced Performance**: Balances load to prevent any single server from becoming overwhelmed.  
* **Security**: Centralizes SSL/TLS encryption and enhances security with configurable security groups.  
* **Scalability**: Works with Auto Scaling to handle changes in traffic load automatically.

## **Conclusion**


AWS Load Balancers are critical components for building scalable, highly available, and resilient applications. By distributing traffic across multiple instances and managing SSL termination, they ensure that your applications can handle varying loads and stay responsive to user demands.

