# Compute Power and Storage 💻
Imagine you have a machine (Computer) with 8GB of RAM and slowly memory starts to get more and more utilized. With time as you start using more and more software and operations on that memory, you may need more computing power. There will be a time when your system can not handle all this.

In cloud computing, you can add or remove computing power as you need it and you only pay for the resources that you use.

You may also need some cloud storage as an addition to your computing power. Cloud storage provides a secure and scalable way to store and access your data from anywhere. With cloud storage, you can easily expand your storage capacity as your needs grow, without having to worry about managing physical storage devices. 
This allows for greater flexibility and cost-efficiency in managing your data.

# Shared Responsibilities 🤝
![2023-04-03 13_34_50-cloud_computing-cc_101_shared_responsibility_model-f png (1200×780) - Brave](https://user-images.githubusercontent.com/69891912/229449009-a314b15a-95b0-43ac-aed1-8b9436504904.png)

- You’ll always be responsible for the information and data that you store in the cloud.
- The cloud provider will be always responsible for the Physical data center, network and hosts.
- Different service models determine responsibilities for OS, network controls, and applications.

# Service Level Agreement 👍
Service Level Agreement is a formal agreement or a commitment between a service provider and a client. 
It outlines the level of service that the client can expect. It could also be between the IT department and the business.

**For example:**

SLA can provide 99% of availability or we can say "uptime of 99%" or 99.91% or 99.95% as well. 

Different SLAs provide different % of uptime (availability of services)

Is there a difference between 99% and 99.9% uptime? well yes in fact it's a big one.

-> 99% uptime = 1% downtime which is 1.6 hours of downtime per week.

-> 99.9% uptime = 0.1% downtime which is 10 mins of downtime per week.

![18e4c8d9-1556-4144-8fa5-b999027082eb](https://user-images.githubusercontent.com/69891912/229446018-ef8f3079-84b5-4cb4-b23c-4a2f4d67efb6.jpg)

# Scalability ⚖
Scalability means the ability to adjust resources when demand is higher. If the business suddenly experiences peak traffic and the systems are overwhelmed, the ability to scale means you can add more resources to better handle the increased demand. Scaling can be of two types:

![167f7f14-b87f-4553-9a56-187933727d05](https://user-images.githubusercontent.com/69891912/229446726-310fee90-a8a6-4ece-9fd9-09951ecdcf11.jpg)

- **Vertical:** Scaling up and down to add more or remove CPUs or RAM to the virtual machine.

- **Horizontal:** Adding more instances of machines or it can be defined as spreading out the resources and increasing the utilization by diving the processing power into several smaller units of servers. This is a better approach when it comes to the utilization of computing power.

# Bare metal 🧲
In the Bare metal approach, an operating system is directly installed on the hardware and can offer better performance for certain workloads because it can utilize the full power of that hardware.

![853a25bf-7e1f-4f36-8959-cfcc8fad0d59](https://user-images.githubusercontent.com/69891912/229447449-34e2f916-b2a3-4550-85b5-0ffc78b4db64.jpg)

# Virtualization 📳
This is a key technology used in cloud computing that allows the creation of virtual computing environments with hardware, os, storage, networking and more capabilities. It allows sharing of physical computing resources among multiple users, applications, and services by abstracting them into virtual entities or virtual machines.

Mainly Virtualization means, running multiple operating systems on a single machine but sharing all the hardware resources. Virtualization allows better utilization of your underlying hardware.

![75dcad62-c494-44e7-afe7-01252c69c74d](https://user-images.githubusercontent.com/69891912/229447766-6df9a520-2f9a-4cd5-85bc-15bd48e5ccb7.jpg)

**The benefits of Virtualization**

- Allows dynamic flexibility
- Better utilization of resources and processing
- Big servers are divided into smaller chunks to utilize the resources properly (Horizontal Scaling)
- Quick addition of more servers without delay

**Business perspective**

- More utilization means more demand is utilized
- It allows the ability to pay for computing resources on a short-term basis when needed.

**Technological perspective**
- Partitions of physical storage and memory can be done
- Better Isolation from the host computer
- Allows encapsulation
- Overall flexibility

**Drawbacks**

- Amplified physical failure i.e, if the host machine fails then all the virtual machines running on it fail as well
- Virtualization involves creating a complete VM that includes an operating system, applications, and required libraries. This process requires a lot of resources such as CPU, memory, and storage, which can increase the cost of deploying and managing applications.
- Setting up the virtual environment requires skills
- Estimation of the number of VMs running per host machine is not easy
- Performance reduces with each layer added between hardware and applications.

# Buckets 🍜
Buckets are a way to organize and manage virtual resources in a virtualized environment. In a bucket, resources such as CPU, memory, and storage are allocated and managed as a single unit. This allows for more efficient use of resources and better management of workloads.

# Next-gen Virtualization 🎛
- Gives predefined or on-demand buckets.
- Virtualization had some drawbacks and therefore isn't the right solution. We need something better.
- The overall idea of a VM is to run more applications, give applications their environment to work properly and create a sandbox so other vms don't overlap.

# Containerization 📦
Containerization refers to the process of packaging an application and its dependencies into a container that can be easily deployed and run consistently across different environments. 
Containerization takes care of all the drawbacks of Virtualization.

![2c2290f1-af60-42a9-9f7d-fe467a3259e4](https://user-images.githubusercontent.com/69891912/229449674-9d47b413-8199-4e61-a90e-c09fcfcc2fa7.jpg)

**Benefits of Containers:**
- Application focused bundling
- Packaged with all the dependencies that are required including the environment (OS, Libraries, etc)
- This bundle of applications is deployable in any environment of my choice or any machine of any cloud provider which makes it super portable
- Faster load time compared to a VM
- A container is also called a Linux Container (LXC)

# Containers vs. VMs 📦📳
If you look closely at the above diagram image of the VM and Containers you can see that certain things are getting repeated again and again such as guest os, runtime, libraries etc. This is not an efficient or optimal approach. A better approach would be to pack the application inside a container so that it has its dependencies and environment to work properly.
Containers have commonality and flexibility.

**If you compare the containers and VM you can see that**
- Containers are more lightweight and efficient than virtual machines
- Containers offer faster start-up times and greater flexibility because they can easily be moved between different environments
- Containers are easier to manage and deploy than virtual machines
- Containers provide better scalability than virtual machines because they can be easily replicated and distributed across multiple hosts

**So when should we consider containers over VMs?**

Answer: When applications needed to be deployed on the same os, runtime environment etc. (Hint: PaaS)

**Faceoff**

- If all apps need to be deployed on the same os image, then use containers (PaaS)
- VM is a good approach for IaaS as it can give choices for operating systems
- Containers have less isolation compared to VMs but they are faster to load
- Specific choices that require only runtime dependencies = Containers
- Need low-level infrastructure = VM

# Infra Automation ♾
Infrastructure automation is the process of using software and tools to automate the management and deployment of IT infrastructure, including servers, networks, and storage. It involves the use of configuration management tools and cloud orchestration platforms to automate the creation, deployment, scaling, and management of infrastructure resources.
There are benefits of using Infra Automation such as less prone to errors, reduced manual work, faster deployment, no scalability issues, etc.
Infrastructure automation is a key component of DevOps, as it involves automating the deployment, configuration, and management of the underlying infrastructure on which software applications run. This can include servers, databases, networking, and storage resources, among other things.

**DevOps** teams often use tools like configuration management tools (such as Ansible, Chef, and Puppet), infrastructure-as-code tools (such as Terraform and CloudFormation), and containerization technologies (such as Docker and Kubernetes) to automate the provisioning and management of infrastructure resources.

![devops-logo (1)](https://user-images.githubusercontent.com/69891912/229453535-254ae001-f3f9-45cb-bf8f-508af526b522.jpg)

**Some popular tools for infrastructure automation include:**
- Ansible
- Puppet
- Chef
- Terraform
- Kubernetes

To know about more tools check out this awesome article: https://spacelift.io/blog/devops-automation-tools

# Resources
- learn.microsoft.com
- olympus.mygreatlearning.com
- wikipedia.com
