# ☁️ AWS setup via Terraform
 
This Repository contains the Terraform's (IaC) code to setup a basic VPC for you in AWS. This VPC will have a public subnet, EC2 instance, IWG - Internet gateway and RouteTables. The RouteTables are also configured to bridge the IWG and subnet.

## 🧑‍💻 Developer setup

### How to Use Terraform for AWS?

To use Terraform for AWS, you need to do the following:

1. **Install Terraform**:
    
    Download and install Terraform on your local machine. You can follow the instructions on [Terraform’s website](https://www.terraform.io/downloads.html).
    
2. **Install and Set up AWS CLI and Credentials**:
    - Install the **AWS CLI** in your local and configure it with your AWS credentials (access key ID and secret access key) (You can get the access ID & Key - Got to AWS dashbord click your AWS id on the top right corner → Security credentials → Under “Access Key section” click Create access key → Click CLI → Click next and Create → There is your ID & Key to copy) .
    - Run `AWS configure` to set your credentials, default region, and output format. Alternatively, you can use environment variables like `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `AWS_REGION`.

4. **Initialize Terraform**:
    In your terminal, navigate to the directory where your `.tf` file is located and run `terraform init` to initialize the configuration and download necessary providers (such as AWS, Azure, etc.).

5. **Plan the Infrastructure**:
    Run `terraform plan` to see what changes Terraform will make to your AWS environment.

6. **Apply the Configuration**:
If you’re satisfied with the plan, run `terraform apply` to apply the changes and provision the resources.

7. To **destroy** the resources when you're done, run `terraform destroy`

### Variables
    - You can give other values to these variable by defining it while running terraform apply.
        Example cmd: terraform apply -var "instance_name=RoshansInstance"
    - Alternatively you can use the terraform.tfvars to set values to the variable defined in your variables.tf file.