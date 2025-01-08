<h1>Terraform AWS EC2 Instance Deployment</h1>

<h2>Description</h2>
This project demonstrates the fundamental usage of Terraform for Infrastructure as Code (IaC) by automating the deployment of an AWS EC2 instance. The project covers basic Terraform concepts including provider configuration, resource creation, state management, and infrastructure modifications. It serves as an introductory exercise to understand how Terraform can be used to manage cloud infrastructure through code.
- Key features of the project include:

- Creating an EC2 instance with specified configurations
- Managing instance tags and security groups
- Demonstrating Terraform state management
- Performing infrastructure modifications
- Cleaning up resources using Terraform destroy
<br />


<h2>Languages and Utilities Used</h2>

<b>Terraform (HashiCorp Configuration Language - HCL)
- AWS CLI
- Git Bash
- Visual Code
<b>

<h2>Environments Used </h2>

</b> AWS Cloud Platform
- EC2 (Elastic Compute Cloud)
- IAM (Identity and Access Management)
- VPC Security Groups
- Windows Operating System (though the project can be executed on Linux or MacOS)</b>

<h2>Program walk-through:</h2>

<p align="center">
1. Environment Setup: <br/>
- Install Terraform
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736293415/Screenshot_2025-01-06_202917_rlplzh.png"/>
- Option 1: Using Chocolatey (Windows)
*choco install terraform*

Option 2: Manual installation<br/>
- Download Terraform binary from official website
- Extract to C:\terraform
- Add to system PATH

Install AWS CLI<br/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736293324/Screenshot_2025-01-04_195458_lpferx.png"/>


2. AWS Configuration<br/>
Create IAM User
- Navigate to AWS IAM Console
- Create new user "terra-admin"
- Grant Administrator Access
- Save Access Key and Secret Key

<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736294074/Screenshot_2025-01-07_123041_hywwro.png"/>
<br />
<br />

Configure AWS Credentials<br/>
- Enter Access Key
- Enter Secret Key
- Set region to us-east-1
- Set output format to json

<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736294451/Screenshot_2025-01-07_123536_poepei.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736294556/Screenshot_2025-01-07_124229_othcdk.png"/>
<br />
<br />

3. Project Structure Setup<br/>
- Create Project Directory
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736294699/Screenshot_2025-01-07_124421_akvrdy.png"/>
<br />
<br />

4. Create Terraform Configuration<br/>
- Create First_instance.tf
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736295364/Screenshot_2025-01-07_134228_vv7f6h.png"/>
<br />
<br />

5. Create Supporting AWS Resources<br/>
Create Key Pair

- Navigate to EC2 Console
- Create new key pair 
- Save the .pem file
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736295555/Screenshot_2025-01-07_133606_b060o3.png"/>
<br />
<br />



Create Security Group<br/>

- Create security group "dove-sg"
- Add inbound rule for SSH (port 22)
- Copy security group ID
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736296131/Screenshot_2025-01-07_133824_ngoaib.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736296189/Screenshot_2025-01-07_133854_jwmxuh.png"/>
<br />
<br />

6. Terraform Commands Execution<br/>
- Initialize Terraform
- Validate Configuration
- Format Configuration
- Plan Deployment
- Apply Configuration
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1736318734/Screenshot_2025-01-07_141231_r4opzj.png"/>
