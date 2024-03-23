# terraform_demo
## when to use terraform or helm for k8s?
When it comes to managing Kubernetes (K8s) clusters and deploying applications on them, both Terraform and Helm offer powerful capabilities, but they serve different purposes and operate at different layers of the infrastructure and application management stack. Understanding the strengths and use cases of each can help you decide when to use one over the other or how to use them together effectively.

### Terraform with Kubernetes
Terraform is an open-source infrastructure as code (IaC) software tool created by HashiCorp. It allows users to define and provision a datacenter infrastructure using a high-level configuration language known as HashiCorp Configuration Language (HCL), or optionally JSON.

Use Case: Terraform is typically used to manage the infrastructure layer. In the context of Kubernetes, Terraform can be used to provision the Kubernetes cluster itself across different cloud providers (like AWS EKS, Azure AKS, or Google GKE). It can also manage associated resources such as VPCs, security groups, IAM roles, etc.

https://medium.com/@vinoji2005/using-terraform-with-kubernetes-a-comprehensive-guide-237f6bbb0586
https://developer.hashicorp.com/terraform/tutorials/kubernetes/kubernetes-provider

### Helm Charts with Kubernetes
Helm is a package manager for Kubernetes that allows developers and operators to package, configure, and deploy applications and services onto Kubernetes clusters.

Use Case: Helm is focused on the application layer. Once you have a Kubernetes cluster running (possibly provisioned by Terraform), Helm helps in packaging and deploying applications to that cluster. Helm packages, called charts, define all the resources needed to deploy an application, service, or tool on Kubernetes.

### Combining Terraform and Helm
In practice, Terraform and Helm are often used together in a complementary fashion:

Infrastructure Provisioning: Use Terraform to provision and manage the Kubernetes cluster and any related cloud infrastructure (like networks, security rules, etc.).
Application Deployment: Once the infrastructure is ready, use Helm to deploy, manage, and upgrade applications on the Kubernetes cluster.