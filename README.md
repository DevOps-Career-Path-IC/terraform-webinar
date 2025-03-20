# Terraform Webinar Demo

This repository contains a comprehensive Terraform configuration that demonstrates key concepts of Infrastructure as Code (IaC) using AWS resources.

## Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/install) installed
- AWS account and configured AWS CLI
- AWS credentials configured (either through AWS CLI or environment variables)

## Project Structure

- `main.tf` - Main Terraform configuration file
- `variables.tf` - Variable definitions
- `outputs.tf` - Output definitions
- `README.md` - This file

## Resources Created

This configuration will create the following AWS resources:
- VPC with CIDR block 10.0.0.0/16
- Public subnet in the VPC
- Internet Gateway
- Route table for the public subnet
- Security group with SSH and HTTP access
- EC2 instance (t2.micro) running Ubuntu 22.04 LTS

## Usage

1. Initialize Terraform:
   ```bash
   terraform init
   ```

2. Review the planned changes:
   ```bash
   terraform plan
   ```

3. Apply the configuration:
   ```bash
   terraform apply
   ```

4. When you're done, destroy the infrastructure:
   ```bash
   terraform destroy
   ```

## Customization

You can customize the configuration by modifying the variables in `variables.tf` or by creating a `terraform.tfvars` file with your desired values.

## Important Notes

- This configuration creates resources in the us-east-1 region by default
- The EC2 instance is created with a t2.micro instance type
- The security group allows SSH (port 22) and HTTP (port 80) access from anywhere
- All resources are tagged with "webinar" prefix for easy identification

## Learning Objectives

This configuration demonstrates:
- Basic Terraform syntax and structure
- AWS provider configuration
- VPC and networking concepts
- Security group configuration
- EC2 instance deployment
- Variable usage
- Output configuration
- Resource dependencies
- Tagging best practices 