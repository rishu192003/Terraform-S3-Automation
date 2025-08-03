# ☁️ Terraform S3 Static Website Deployment

This project uses **Terraform** to provision an **S3 bucket** and configure it to host a **static website** on AWS. The entire setup — including S3, bucket policies, VPC configuration, and website deployment — is managed via **Infrastructure as Code (IaC)**.

---

## 🌐 Live Website

http://myterraformproject2343.s3-website-us-east-1.amazonaws.com/

---

## 🚀 What This Terraform Project Does

- Creates an AWS S3 bucket
- Sets public access and static website hosting configuration
- Uploads static site files (HTML/CSS/JS) automatically
- Configures bucket policies for public access
- Sets up basic VPC resources (if applicable)
- All done using IaC — no manual AWS Console steps

---

## 📁 Project Structure

terraform-s3-static-site/
├── main.tf # Main Terraform configuration
├── variables.tf # Input variables
├── outputs.tf # Output values like bucket URL
├── s3_website/ # Contains static site files (index.html, etc.)
└── README.md


---

## 🛠️ Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/install)
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) configured (`aws configure`)
- AWS account with IAM permissions to create S3 resources

---

## ⚙️ Usage

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/terraform-s3-static-site.git
cd terraform-s3-static-site

2. Initialize Terraform
terraform init

3. Set Your AWS Region and Bucket Name (Optional)
Edit variables.tf or override via CLI:

terraform apply -var="region=us-east-1" -var="bucket_name=my-static-site-demo"

4. Apply the Configuration
terraform apply

Type yes to confirm

Wait for Terraform to complete provisioning

5. Visit the Website
The output will contain the S3 static site URL. Or use the one below:

➡️ https://your-bucket-name.s3-website-<region>.amazonaws.com

🧼 To Destroy the Resources
terraform destroy

## 📄 License
This project is open-source and available under the MIT License.
