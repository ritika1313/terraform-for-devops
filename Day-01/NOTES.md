# What is Terraform?

Terraform is an Infrastructure as Code (IaC) tool developed by HashiCorp. It allows us to automate infrastructure provisioning using code instead of manually creating cloud resources.

# Advantages of Terraform
- Automates infrastructure creation
- Faster deployment
- Reduces human errors
- Cost-effective
- Efficient resource utilization
- Consistent infrastructure across environments
- Supports multiple cloud providers (AWS, Azure, GCP)

# Difference Between Terraform and Ansible
1. Terraform
- Infrastructure as Code (IaC) tool.
- Used to provision infrastructure.
- Creates cloud resources like EC2, VPC, S3, etc.
2. Ansible
- Configuration Management tool.
- Used to configure servers after they are created.
- Installs software, updates packages, deploys applications, etc.

# Simple line to remember
Terraform creates infrastructure, whereas Ansible configures infrastructure.

# Terraform uses HCL
Terraform code is written in
HCL (HashiCorp Configuration Language).

# Common Terraform Blocks
1. Resource Block
Used to create infrastructure resources.
Example: 
resource "local_file" "my_file" {
  filename = "automate.txt"
  content  = "This is my first file"
}
2. Variable Block
Used to store user input.
variable "instance_type" {}
3. Output Block
Used to display values after execution.
output "file_name" {
  value = local_file.my_file.filename
}

# Terraform Workflow
1. Step 1
terraform init
Initializes Terraform.

- Downloads providers
- Creates .terraform folder
- Creates .terraform.lock.hcl
2. Step 2
terraform validate

- Checks whether the Terraform configuration is syntactically correct.

3. Step 3
terraform plan

- Shows what Terraform is going to create, update, or destroy.

No changes are made.

4. Step 4
terraform apply

- Executes the plan and creates the resources.

5. Step 5
terraform destroy

- Deletes all resources created by Terraform.

# Infrastructure as Code (IaC)
Instead of creating infrastructure manually through the AWS Console, we write code in Terraform, and Terraform automatically creates the infrastructure.
