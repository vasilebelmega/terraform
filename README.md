# Structure
![image](https://github.com/user-attachments/assets/fce4e257-b086-4253-9007-9e5aae3e13bb)

# Terraform Infrastructure for EC2, DynamoDB

This Terraform project provisions an AWS infrastructure that includes:
- An EC2 instance running a Python application.
- A DynamoDB table for storing meeting data.
- IAM roles and policies to allow the EC2 instance to access DynamoDB.

## **Infrastructure Overview**

### **Resources Created**
1. **EC2 Instance**:
   - Runs a Python application.
   - Configured with a security group to allow HTTP (port 8081) and SSH (port 22) traffic.
   - Uses an IAM instance profile to access DynamoDB.

2. **DynamoDB Table**:
   - Table named `meetings_table` for storing meeting data.
   - Provisioned with read and write capacity.

3. **IAM Roles and Policies**:
   - IAM role for the EC2 instance to access DynamoDB.
   - IAM policy attached to the role to allow DynamoDB actions.

4. **Networking**:
   - Public route table associated with a subnet.
   - Security groups for EC2

note: also a mySql database is created but not used

## **Prerequisites**
1. Install [Terraform](https://www.terraform.io/downloads).


## **Usage**

### **1. Clone the Repository**

git clone https://github.com/vasilebelmega/terraform.git

cd terraform

terraform init

terraform plan

terraform apply


take ip from output e.g:![image](https://github.com/user-attachments/assets/bbac024a-a019-4a22-a3f2-eba9f83968e6) wait until application is running
http://<app_server_ip>:8081


*Destroy after to avoid costs:

terraform destroy



