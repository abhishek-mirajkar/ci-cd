# 🖥️ Deploying a Windows Server in a Public Subnet and Accessing via Local Machine

## 📘 Overview
This project demonstrates how to **deploy a Windows Server in a public subnet** within an AWS Virtual Private Cloud (VPC) and **access it directly from your local machine** using Remote Desktop Protocol (RDP).  
The setup showcases AWS networking fundamentals, instance deployment, and secure access configuration.

## 🎯 Objectives
- Create a **custom VPC** with a public subnet  
- Launch a **Windows Server EC2 instance** in the public subnet  
- Configure **Internet Gateway** and **Route Table** for internet access  
- Set up **Security Groups** and **Key Pairs**  
- Access the Windows Server from your **local system via RDP**

## 🏗️ Steps Demonstrated
1. **Create a VPC**
   - Define a CIDR block (e.g., `10.0.0.0/16`)
   - Create one public subnet (e.g., `10.0.1.0/24`)

2. **Attach Internet Gateway**
   - Create and attach an Internet Gateway to the VPC  
   - Update the route table to allow outbound internet access (`0.0.0.0/0`)

3. **Launch a Windows Server EC2 Instance**
   - Choose **Microsoft Windows Server** AMI  
   - Place it in the **public subnet**  
   - Assign a **public IP address** during launch  
   - Attach the key pair for login credentials

4. **Configure Security Group**
   - Allow **RDP (port 3389)** from your IP address only  
   - Allow **ICMP (ping)** optionally for testing connectivity

5. **Access the Instance**
   - Download and use the **.pem key** to decrypt the Windows password  
   - Use **Remote Desktop Connection (RDP)** on your local machine  
   - Connect using the instance’s **public IP address**

6. **Validation**
   - Verify that you can log in to the Windows Server  
   - Confirm proper public connectivity and security restrictions

## 🧰 Tools & Technologies Used
- **AWS EC2**
- **AWS VPC**
- **AWS IAM**
- **Security Groups**
- **Remote Desktop Protocol (RDP)**

## 🎥 Demonstration Video
[Watch the full video here](#) <!-- Replace '#' with your video link (YouTube or GitHub video file) -->

## 📁 Repository Structure
```
📦 Deploy-WindowsServer-PublicSubnet
 ┣ 📜 README.md
 ┣ 🎥 demo-video.mp4
 ┣ 📄 architecture-diagram.png
 ┗ 🧾 setup-notes.txt
```

## 🧠 Key Learnings
- How to create and configure a public subnet in AWS  
- How to launch and access a Windows Server instance securely  
- Understanding Internet Gateways, route tables, and security groups  

## 🚀 Future Enhancements
- Add a **private subnet** and **bastion host** for secure architectures  
- Automate the deployment using **Terraform** or **CloudFormation**  
- Configure **NAT Gateway** for private subnet internet access  

## 🧑‍💻 Author
**Abhishek Mirajkar**  
Cloud Computing Student | AWS Enthusiast  

🔗 *Connect with me:* [LinkedIn](#) | [GitHub](#)
