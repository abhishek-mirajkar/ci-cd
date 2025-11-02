# ci-cd


# AWS S3 Buckets: Create via Console and Delete via CLI

## 📘 Project Overview
This project demonstrates how to **create two Amazon S3 buckets using the AWS Management Console** and then **delete them using the AWS Command Line Interface (CLI)**.  
It is a simple hands-on exercise to understand AWS S3 operations through both GUI and CLI.

---

## 🧠 Learning Objectives
- Understand how to create S3 buckets from the AWS Console.  
- Learn how to configure the AWS CLI and authenticate using IAM credentials.  
- Perform S3 bucket deletion using AWS CLI commands.

---

## 🧰 Prerequisites
Before you begin, ensure you have the following:
1. **AWS Account** – with permissions to manage S3.
2. **IAM User** – with `AmazonS3FullAccess` or equivalent permissions.
3. **AWS CLI Installed** – [Download and install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
4. **Access Keys** – from your IAM user for CLI configuration.

---

## ⚙️ Step 1: Create Two Buckets in AWS Console

1. Log in to your [AWS Management Console](https://aws.amazon.com/console/).
2. Navigate to **S3 → Buckets → Create bucket**.
3. Enter a **unique bucket name**, e.g.:
   - `my-demo-bucket-1`
   - `my-demo-bucket-2`
4. Choose a **region** (e.g., `us-east-1`).
5. Leave other settings default and click **Create bucket**.
6. Verify both buckets appear in your S3 dashboard.

---

## 🧾 Step 2: Configure AWS CLI

Open your terminal or command prompt and run:
```bash
aws configure

AWS Access Key ID: <your_access_key>
AWS Secret Access Key: <your_secret_key>
Default region name: us-east-1
Default output format: json
aws s3 ls
2025-11-02  my-demo-bucket-1
2025-11-02  my-demo-bucket-2

aws s3 rb s3://my-demo-bucket-1 --force
aws s3 rb s3://my-demo-bucket-2 --force

aws s3 ls
