# **Socks Shop Microservices-based Application Deployment on Kubernetes using IaC.**

**PROJECT LIVE LINK:** [CAPSTONE PROJECT LINK](http://capstone.vctr.xyz)

##

## **Project Overview:**

The Socks Shop application is a popular microservices-based e-commerce platform that is used as a reference application for demonstrating modern cloud-native technologies. The application is composed of multiple microservices, each of which is responsible for a specific function, such as product catalog, shopping cart, and user authentication. The application is designed to be highly scalable, resilient, and fault-tolerant, making it an ideal candidate for deployment on Kubernetes.

The project will involve deploying the Socks Shop application on a Kubernetes cluster using an Infrastructure as Code (IaC) approach. This will include provisioning the necessary infrastructure resources on AWS, setting up a deployment pipeline, monitoring the performance and health of the application, and securing the infrastructure.

The project will be implemented using Terraform for infrastructure provisioning, GitHub Actions for the deployment pipeline, Kubernetes for container orchestration, Helm for package management, Prometheus for monitoring, ELK Stack for logging, and Ansible for security.

## **This project will include the following components:**

- [Infrastructure Provisioning](#infrastructure-provisioning)
- [Deployment Pipeline](#deployment-pipeline)
- [Monitoring](#monitoring)
- [Logging](#logging)
- [Security](#security)
- [conclusion](#conclusion)
- [References](#references)

## **Project Requirements:**

- Terraform
- AWS Account
- Kubernetes
- Helm
- Prometheus
- ELK Stack
- Let's Encrypt
- Socks Shop Application

  ## **Project Deliverables:**

- Terraform configuration files for provisioning the infrastructure on AWS
- Deployment pipeline configuration using GitHub Actions
- Kubernetes manifests for deploying the Socks Shop application
- Prometheus configuration for monitoring the Socks Shop application
- ELK Stack configuration for centralized logging
- Ansible playbooks for securing the infrastructure
- Documentation on how to run the project

## **Project Structure:**

```
socks-shop-deploy/
├── .github/
│   └── workflows/
│       └── ci-cd.yaml    # GitHub Actions workflow for CI/CD
├── k8s/
│   ├── deployment.yaml   # Kubernetes deployment manifests
│   └── ingress.yaml      # Kubernetes ingress manifest
├── monitoring/
│   ├── prometheus/
│   │   └── values.yaml   # Custom values for Prometheus Helm chart
│   └── grafana/
│       └── values.yaml   # Custom values for Grafana Helm chart
├── logging/
│       ├── elasticsearch.yaml  # Elasticsearch deployment
│       ├── filebeat.yaml       # Fluentd configuration
│       └── kibana-deployment.yaml         # Kibana dashboard configuration
|       └── cronjob.yaml        # Fluentd configuration
|       └── metricbeat.yaml     #  Fluentd configuration
|       └── logstash-deployment.yaml        # Fluentd configuration
├── terraform/
│   ├── main.tf         # Main Terraform configuration for AWS EKS
│   ├── terraform.tf    # Terraform configuration
│   ├── outputs.tf      # Terraform outputs
│   ├── provider.tf     # Provider configuration
│   └── vpc.tf          # VPC configuration
└──README.md
```

The project will be organized into the following directories:

- `Infrastructure`: This directory will contain the Terraform configuration files for provisioning the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster.
- `kubernetes`: This directory will contain the Kubernetes manifests for deploying the Socks Shop application, including deployment and ingress resources.
- `CI/CD`: This directory will contain the GitHub Actions workflow files for setting up a deployment pipeline to build and deploy the Socks Shop application to the Kubernetes cluster.
- `Monitoring`: This directory will contain the configuration files for setting up Prometheus to monitor the performance and health of the Socks Shop application.
- `Logging`: This directory will contain the configuration files for setting up a centralized logging solution, such as ELK stack, to collect and analyze logs from the Socks Shop application.

The project will also include a `README.md` file in each directory to provide detailed instructions on how to set up and configure the components.

## **Prerequisites:**

The following tools and technologies will be used in the project:

- Terraform: Terraform is an open-source infrastructure as code software tool that provides a consistent CLI workflow to manage hundreds of cloud services. It codifies APIs into declarative configuration files, creating infrastructure as code using a high-level configuration language called HCL (HashiCorp Configuration Language).

- AWS Account: An AWS account will be required to provision the necessary infrastructure resources, such as VPCs, subnets, security groups, and EKS cluster.

- GitHub Actions: GitHub Actions will be used to set up a deployment pipeline to build and deploy the Socks Shop application to the Kubernetes cluster.

- Kubernetes: Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications.

- Helm: Helm is a package manager for Kubernetes that provides an easy way to find, share, and use software built for Kubernetes.

- Prometheus: Prometheus is an open-source monitoring and alerting toolkit designed for reliability and scalability. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts if some condition is observed to be true.

- ELK Stack: The ELK Stack is a collection of three open-source products — Elasticsearch, Logstash, and Kibana — all developed, managed, and maintained by Elastic. The ELK Stack is used to collect, search, analyze, and visualize log data in real time.

- Let's Encrypt: Let's Encrypt is a free, automated, and open certificate authority brought to you by the nonprofit Internet Security Research Group (ISRG).

- Docker: Docker is a set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers.

- Socks Shop Application: The Socks Shop application is a popular microservices-based e-commerce platform that is used as a reference application for demonstrating modern cloud-native technologies.

## **Project Objectives:**

The main objectives of the project are as follows:

- Deploy the Socks Shop application on a Kubernetes cluster using an Infrastructure as Code (IaC) approach
- Provision the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster
- Set up a deployment pipeline using GitHub Actions to build and deploy the Socks Shop application to the Kubernetes cluster
- Monitor the performance and health of the Socks Shop application using Prometheus
- Collect and analyze logs from the Socks Shop application using a centralized logging solution, such as ELK stack.

#

## **GETTING STARTED**

Socks Shop Resources: https://github.com/microservices-demo/microservices-demo.github.io

Demo: https://github.com/microservices-demo/microservices-demo/tree/master

## **Infrastructure Provisioning:**

Using Terraform, we will provision the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster. This will allow for a clear and reproducible infrastructure setup.

1.  Make sure you have installed Terraform alongside AWS CLI on your local machine. If not, you can download it from the official website.

    [AWS CLI Installation guide](https://aws.amazon.com/cli/)

    [Terraform Download](https://www.terraform.io/downloads.html)

2.  Create a new directory for the Terraform configuration files and navigate to it.

        mkdir Socks-Shop_Terraform
        cd Socks-Shop_Terraform

3.  Git clone this repository and navigate to the terraform folder to have the Terraform configuration files and initiate the Terraform project.

        git clone https://github.com/vicsam/socks_shop/terraform

4.  Run the following command to initialize the Terraform project:

        terraform init

5.  Run the following command to create an execution plan:

        terraform plan

6.  Run the following command to apply the changes:

        terraform apply --auto-approve

        #the flag --auto-approve can be added to avoid the prompt for confirmation.

