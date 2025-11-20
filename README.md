<h1>Overview</h1>

This project automates the end-to-end deployment of a high-availability web application on AWS by using Terraform (IaC) and GitLab CI/CD.The entire infrastructure — **VPC, public subnets, ALB, security groups, and two EC2 instances across AZs** — is provisioned automatically through version-controlled Terraform code.A multi-stage GitLab pipeline validates, plans, and applies infrastructure changes, ensuring a repeatable, error-free, production-grade deployment workflow.This eliminates manual AWS console work and ensures consistent environments every time.

<img width="130" height="130" alt="image" src="https://github.com/user-attachments/assets/25f435da-7ac3-4df3-820c-0ee5f212cd1d" />  <img width="250" height="230" alt="image" src="https://github.com/user-attachments/assets/57adf094-8ca8-4933-bfa8-b8cef5cc17e7" />  <img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/f076cf64-526e-4085-b7c6-704ee5721caa" />    <img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/7df255da-932d-4065-9962-bc507867d3a6" />  <img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/905800c0-dbef-42bb-972d-cd04039a58f7" />



<h1>Architecture Diagram</h1>

<img width="480" height="1085" alt="Screenshot 2025-11-20 125344" src="https://github.com/user-attachments/assets/4fe0ca55-a861-4a49-96a1-69889e775201" />

Here is the architecture our Terraform code builds automatically:
- VPC: A private, isolated network in the AWS cloud.
- High Availability: We use two Availability Zones (separate physical data centers). If one fails, our application stays online.
- Application Load Balancer (ALB): The public entry point. It provides a single URL and distributes traffic across our servers for performance and reliability.
- EC2 Instances: Two virtual web servers, each in a different Availability Zone. They are automatically configured on startup with a user_data script.
- Security Groups: A virtual firewall that only allows necessary traffic (HTTP and SSH) into our servers.


<h1>CI/CD Pipeline Flowchart</h1>

<img width="735" height="940" alt="Untitled diagram _ Mermaid Chart-2025-08-20-095743" src="https://github.com/user-attachments/assets/d0c11b89-8488-4603-b9aa-82eb6d681d5b" />


<h1>Demo Result</h1>

<img width="1349" height="380" alt="Screenshot 2025-08-20 153923" src="https://github.com/user-attachments/assets/8e647a5f-2e8b-4aee-97e0-d5765a62399b" />

<img width="1351" height="637" alt="Screenshot 2025-08-20 154016" src="https://github.com/user-attachments/assets/3f11c475-5814-4c56-8841-2768668372b9" />

<img width="1352" height="668" alt="image" src="https://github.com/user-attachments/assets/9b35f2ec-953c-4fcd-9e85-501d6820861f" />

<img width="1365" height="681" alt="image" src="https://github.com/user-attachments/assets/da4458d3-0831-4f03-9139-fb813ada17b4" />









