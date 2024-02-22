# **Deploying Applications on Docker and Kubernetes with Jenkins CI/CD pipeline using AWS and DevSecOps Practices**

## ****Introduction****
In today's fast-paced world of software, getting applications up and running quickly and 
safely is crucial. This project focuses on making that happen by using Docker, 
Kubernetes, Jenkins CI/CD, and DevSecOps practices to simplify the process while 
keeping everything secure.
We use Kubernetes to organize and manage our applications in containers, making them 
easier to handle and ensuring they run smoothly no matter where they're deployed.
Jenkins CI/CD Pipeline helps us automate the steps of building, testing, and delivering 
our apps. This means less manual work and faster results, so we can get our apps out to 
users more efficiently.
To keep our apps secure, we've added extra tools and practices. Helm helps us manage 
our Kubernetes apps consistently, while Prometheus and Grafana keep an eye on how our 
apps are performing.
We also use SonarQube to check our code for any potential issues early on, and tools like 
Trivy and OWASP to scan our container images for vulnerabilities and make sure they 
meet security standards.
By combining these tools and practices, we're able to automate many parts of the 
deployment process, making it faster, more reliable, and safer. This helps us work together better as a team and deliver better-quality software to our users faster .


## **Benefits** 
1. Streamlined Deployments: Manual interventions are minimized, leading to faster 
releases and shorter feedback loops.
2. Continuous Delivery: New features and bug fixes are delivered frequently, 
enhancing user experience and reducing time-to-market.
3. Enhanced Security: By integrating security throughout the pipeline, 
vulnerabilities are identified and addressed early, minimizing potential security 
breaches.
4. Scalability and High Availability: Kubernetes ensures applications can seamlessly 
scale up or down based on demand, while self-healing capabilities keep them 
running even in case of failures.
5. Cloud-Based Infrastructure: AWS provides a pay-as-you-go model, offering 
flexibility and cost-efficiency.


## **SYSTEM DEVELOPMENT AND DESIGN**
The system architecture comprises two Amazon EC2 instances: a t2.large instance 
hosting Jenkins, OWASP Scan, Docker, Trivy, and Amazon Ubuntu AMI for the base 
operating system, and a t2.medium instance dedicated to hosting Prometheus and Grafana 
for monitoring purposes. Additionally, Amazon Elastic Kubernetes Service (EKS) is 
utilized to orchestrate and manage containerized applications, with Helm for package 
management and ArgoCD for GitOps-based continuous delivery.
Jenkins serves as the CI/CD server, automating the build, test, and deployment processes 
of applications. It integrates seamlessly with Docker and EKS for managing 
containerized deployments. OWASP Scan conducts security scans on applications 
deployed through Jenkins to identify vulnerabilities, while Trivy scans container images 
pre-deployment to ensure secure deployments. Helm streamlines application deployment 
and management on Kubernetes, while ArgoCD automates deployment based on Git 
repository changes, ensuring consistency and reliability.
The integration between components is seamless and efficient. Jenkins orchestrates the 
build, test, and deployment processes, utilizing Docker for containerization and EKS for 
deployment orchestration. Security scanning tools OWASP Scan and Trivy integrate with 
Jenkins to ensure secure deployments through pre-deployment and post-deployment 
vulnerability assessments. Helm and ArgoCD automate the deployment process, ensuring 
consistency and reliability through GitOps practices. Monitoring tools Prometheus and 
Grafana collect and visualize metrics from EKS and other components for continuous 
monitoring and analysis.
The system is designed to be scalable and highly available. Amazon EKS automatically 
scales based on workload demands, ensuring optimal resource utilization.
#### ***System Architecture***

## ![image](https://github.com/C1-80417/finalproject/assets/75259679/33960b97-0518-411b-828e-e982b757358a)

## **Technology used**
#### Amazon EC2
Amazon Elastic Compute Cloud (Amazon EC2) is a web service provided by 
Amazon it allows you to rent virtual servers in the cloud, known as instances, to run 
your applications and workloads. EC2 provides a scalable and flexible infrastructure 
that enables you to quickly deploy and manage virtual servers without the need to 
invest in physical hardware.

***Amazon AWS EC2***
![WhatsApp Image 2024-02-22 at 09 18 25_e475f7ab](https://github.com/C1-80417/finalproject/assets/75259679/13d7e8df-64ef-40c4-9cc9-2affaa1eeeba)

### GIT
Git is a distributed version control system (VCS) designed to manage source code history and facilitate collaborative software development.

### Docker
Docker is an open-source platform that allows you to automate the deployment, 
scaling, and management of applications using containerization. Containers are 
lightweight, portable, and isolated environments that package an application and its 
dependencies together.

***Docker***
![WhatsApp Image 2024-02-22 at 09 18 26_b03dad4d](https://github.com/C1-80417/finalproject/assets/75259679/3ff1cab6-c256-4af0-9bfe-5c906dead3f5)


### Jenkins
Jenkins is an open-source automation server that facilitates the continuous 
integration and continuous delivery (CI/CD) of software projects. It helps automate 
various tasks related to building, testing, and deploying applications, making the 
development and release process more efficient and reliable. 

***jenkins***
![WhatsApp Image 2024-02-22 at 09 18 26_39c84c59](https://github.com/C1-80417/finalproject/assets/75259679/7729912a-b384-446d-b64d-018bea7648e1)

### Amazon EKS
Amazon EKS (Elastic Kubernetes Service) is a managed Kubernetes service offered 
by Amazon Web Services (AWS) that simplifies the deployment, management, and 
scaling of containerized applications using Kubernetes.

### SonarQube
SonarQube is an open-source platform developed by SonarSource for continuous 
inspection of code quality to perform automatic reviews with static analysis of code 
to detect bugs, code smells, and security vulnerabilities on 20+ programming 
languages. It provides a centralized dashboard to view metrics on code quality, 
security vulnerabilities, and overall project health

***SonarQube***
![WhatsApp Image 2024-02-22 at 09 18 26_1e570df5](https://github.com/C1-80417/finalproject/assets/75259679/3a20f3b4-a0ce-452f-840d-3f203efb9fb8)

### OWASP
OWASP (Open Web Application Security Project) provides a variety of resources 
and tools for improving the security of web applications. An OWASP scan typically 
refers to the process of using tools and methodologies provided by OWASP to 
assess the security posture of web applications, identify potential vulnerabilities, and 
address them to enhance overall security. One of the key tools provided by OWASP 
for this purpose is OWASP ZAP (Zed Attack Proxy).

### Trivy 
Trivy is an open-source vulnerability scanner for containers and other artifacts. It is 
primarily used to scan container images to identify vulnerabilities within them. 
Trivy is designed to be fast, simple, and easy to integrate into containerized 
environments.

### Prometheus
Prometheus is an open-source monitoring and alerting toolkit originally built at 
SoundCloud. It is now a standalone open-source project maintained by the Cloud 
Native Computing Foundation (CNCF). Prometheus is designed for monitoring 
highly dynamic containerized environments like those orchestrated by Kubernetes.

***Prometheus***
![WhatsApp Image 2024-02-22 at 09 18 25_f9a799b2](https://github.com/C1-80417/finalproject/assets/75259679/6e0c6cfc-7da8-4ab8-8f25-60c76c65c70d)

### Grafana
Grafana is an open-source analytics and visualization platform primarily focused on 
time-series data. It allows users to query, visualize, and understand metrics from 
various data sources, including databases, cloud monitoring services, and custom 
applications. Grafana is commonly used for monitoring, observability, and data 
exploration in a wide range of domains, including DevOps, IoT, and business 
intelligence.

***Grafana***
![WhatsApp Image 2024-02-22 at 09 18 26_370a2782](https://github.com/C1-80417/finalproject/assets/75259679/21e3140d-9bc4-46ed-84e6-9e7efba399b0)

## Final Output

***Web Application Running***
![WhatsApp Image 2024-02-22 at 09 18 26_6c0b983d](https://github.com/C1-80417/finalproject/assets/75259679/6167bdbe-c7f4-4898-9688-8b83e39ce5dd)

## Conclusion
Hence, we have successfully deployed a highly available and secure web server 
environment on Amazon Web Services (AWS). And ensured the reliability, performance, 
and security of the web application while maintaining efficient development and 
operational processes.
