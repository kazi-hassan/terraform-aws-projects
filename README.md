# Terraform AWS Projects

Hands-on Terraform + AWS infrastructure projects, built while studying for the HashiCorp Terraform Associate certification. Each project focuses on a different core concept, with all infrastructure provisioned and destroyed via `terraform apply` / `terraform destroy`.

## Projects

### Project 1: VPC + EC2 Instance
A foundational network setup: a custom VPC with a public subnet, internet gateway, route table, and a security group allowing SSH access, with a single EC2 instance launched inside it.

**Concepts covered:**
- Provider configuration and the Terraform plugin model
- Data sources (dynamic AMI lookup — always resolves to the latest Amazon Linux image, no hardcoded AMI IDs)
- Resource dependencies and implicit ordering
- VPC networking fundamentals (subnets, internet gateways, route tables)
- Security group ingress/egress rules
- Output values

**Files:** [`project1-vpc-ec2/`](./project1-vpc-ec2)

**Run it:**
```bash
cd project1-vpc-ec2
terraform init
terraform plan
terraform apply
# ... verify, then:
terraform destroy
```

---

*More projects coming soon: multi-tier VPC w